# MT - NMT - Pre-training

By [YuweiYin](https://github.com/YuweiYin)

- [Reading-List & Brief Notes](./Reading-List-Brief-Notes.md)

# 1. PLM Introduction

根据大量无监督数据训练一个**语言模型**，这个过程称为**预训练**，得到的模型称为 **预训练语言模型** (Pre-training Language Model, **PLM**)。接下来，对于某个特定任务 (下游任务)，用特定任务的监督数据去增量训练模型 (**fine-tune 精调**)。

PLM 输入词汇 token 输出词向量 embedding vector，目标是**让语义相近的词汇，其词向量(经过度量的结果)也很接近**。

过去往往使用**静态词向量**模型，即每个词汇的词向量对应的词向量是固定的，如 Word2Vec、GloVe、FastText 等，参考 [相应专题](https://github.com/YuweiYin/Overview_of_Artificial_Intelligence/tree/master/NLP/Embedding/Text-Representation.md)。

而对于中文，除了普通的序列建模，还可以用图像处理的方法对**汉字图片**进行特征提取 (例如使用 CNN 等结构)，从而得到其字形上的表征。参考 Tzu-Ray Su, Hung-Yi Lee, *Learning Chinese Word Representations From Glyphs Of Characters*, EMNLP, 2017

---

但是静态词向量没有考虑**语境、上下文** context，同一个词汇 总是输出同一个词向量。然而自然语言又有极多的**一词多义**情况，因此静态词向量的建模效果还不够好。

故提出 **Contextualized Word Embedding**，给模型 (常用 BiLSTM、Self-Attention Layers、Tree-based model / Semantic Parsing Tree) 输入一整句，然后在考虑整句的情况下 获得其中每个词汇的向量表征。

不过语法解析树往往只在 语法结构很清晰的输入上才能效果较好，否则不能明显胜过 不使用语法树的模型。

## PLM 历史

- 预训练模型源于早期的词嵌入（word embedding）工作，比如 Word2Vec。它的训练的结果是词的嵌入，是一个静态的表示。
- 此后 ULMFiT 是第一个使用 RNN 基于 LM 训练的上下文相关的预训练模型；
- CoVe 利用翻译任务来训练编码器-解码器，并使用编码器作为预训练模型；
- ELMo 使用双向 LSTM 合并两个方向的隐状态获得上下文相关表示；
- GPT 采用 LM 进行训练，它是基于 Transformer 的单向预训练模型；
- BERT 是基于 Transformer 的基于掩码的预训练模型；
- MT-DNN 基于 BERT 增加了一些任务进行多任务训练；
- MASS 使用编码-解码器来训练预训练模型；
- UniLM 尝试同时支持语言理解和生成任务。

把预训练模型用于多语言任务：

- XLM 是一种支持多语言的 BERT 模型；
- Unicoder 引入若干新的任务改进了 XLM；
- T5 把多种自然语言任务（比如机器翻译、问答），用了更大的数据，在一个网络训练，同时支持这些任务；
- BART 是一种编码-解码器模型，通过还原损坏的句子训练；
- mBART 将 BART 理念扩展到多语言。

另外还有最新的很多模型。

---

模型的发展趋势是模型规模越来越大 (参数量剧增)、用于训练的数据量越来越多。因此大模型往往只有大公司有能力训练出来，从而也出现了许多对 BERT 等大模型进行**压缩**的方法 (压缩同时尽量保证效果不变差)。常见预训练模型的参数量对比如下 (m: million, b: billion)：

日期 | 公司/机构 | 模型名 | 参数量
:-: | :-: | :-: | :-:
2018 April | AI2 | **ELMo** | 94m
2018 July | OpenAI | **GPT-1** | 110m
2018 October | GoogleAI | **BERT** | 340m
2019 January | AI2 | **Transformer-ELMo** | 465m
2019 February | OpenAI | **GPT-2** | 1.5b
2019 April | Microsoft | **MT-DNN** | 330m
2019 June | Carnegie Mellon University | **XLNet** | 340m
2019 June | FacebookAI | **XLM** | 665m
2019 June | University of Washington | **Grover-Mega** | 1.5b
2019 July | FacebookAI | **RoBERTa** | 355m
2019 August | HuggingFace | **DistilBERT** | 66m
2019 August | NVIDIA | **Megatron** | 8.3b
2020 January | Microsoft | **Turing NLG** | 17b

---

常见的压缩的预训练模型有：

- **Distill BERT** [Sanh, et al., NeurIPSworkshop’s] Victor Sanh, Lysandre Debut, Julien Chaumond, Thomas Wolf, *DistilBERT, a distilled version of BERT: smaller, faster, cheaper and lighter*, NeurIPSworkshop, 2019
- **Tiny BERT** [Jian, et al., arXiv’19] XiaoqiJiao, YichunYin, LifengShang, Xin Jiang, Xiao Chen, LinlinLi, Fang Wang, QunLiu, *TinyBERT: Distilling BERT for Natural Language Understanding*, arXiv, 19
- **Mobile BERT** [Sun, et al., ACL’20] ZhiqingSun, HongkunYu, XiaodanSong, RenjieLiu, YimingYang, Denny Zhou, *MobileBERT: a Compact Task-Agnostic BERT for Resource-Limited Devices*, ACL, 2020
- **Q8BERT** [Zafrir, et al., NeurIPSworkshop 2019] OfirZafrir, Guy Boudoukh, Peter Izsak, Moshe Wasserblat, *Q8BERT: Quantized 8Bit BERT*, NeurIPSworkshop 2019
- **ALBERT** [Lan, et al., ICLR’20]ZhenzhongLan, Mingda Chen, Sebastian Goodman, Kevin Gimpel, Piyush Sharma, Radu Soricut, *ALBERT: A Lite BERT for Self-supervised Learning of Language Representations*, ICLR, 2020

---

常用的压缩方法为：

- 网络剪枝 Network Pruning
- 知识蒸馏 Knowledge Distillation
- 参数量化 Parameter Quantization
- 结构设计 Architecture Design

参考 [All The Ways You Can Compress BERT](http://mitchgordon.me/machine/learning/2019/11/18/all-the-ways-to-compress-BERT.html)

---

预训练网络架构改进

- **Transformer-XL** [Dai, et al., ACL’19] ZihangDai, Zhilin Yang, Yiming Yang, Jaime Carbonell, Quoc V. Le, Ruslan Salakhutdinov, *Transformer-XL: Attentive Language Models Beyond a Fixed-Length Context*, ACL, 2019
	- Transformer-XL 优化：Segment-level recurrence with state reuse。从而可以处理特别长的输入
- **Reformer** [Kitaev, et al., ICLR’20] Nikita Kitaev, Lukasz Kaiser, Anselm Levskaya, *Reformer: The Efficient Transformer*, ICLR, 2020
- **Longformer** [Beltagy, et al., arXiv’20] IzBeltagy, Matthew E. Peters, Arman Cohan, *Longformer: The Long-Document Transformer*, arXiv, 2020
	- Reformer 和 Longformer 优化：Reduce the complexity of self-attention。原本 self-attention 的计算时间复杂度是 $O(n^2)$ 其中 $n$ 为输入序列长度，而 Reformer 和 Longformer 可以缩减此耗时。

---

趣闻：PLM 通常以“芝麻街”里的人物命名，例如：

- **ELMo** (**E**mbeddings from **L**anguage **Mo**dels)
- **BERT** (**B**idirectional **E**ncoder **R**epresentations from **T**ransformers)
- **ERNIE** (**E**nhanced **R**epresentation through K**n**owledge **I**nt**e**gration)
- **Grover** (**G**enerating a**R**ticlesby **O**nly **V**iewing m**E**tadata**R**ecords)
- BERT & **PALs** (**P**rojected **A**ttention **L**ayer**s**)
- [**Big Bird**](https://arxiv.org/abs/2007.14062) Zaheer, et al., *Big Bird: Transformers for Longer Sequences*, arXiv, 20

---

# 2. PLM fine-tune

我们希望在已经训练好的 Pre-trained LM 基础上加一些 task-specific layer 从而处理特定的 NLP 任务。

下面以 BERT 为例，考虑如何使用已经训练好的 PLM 模型。

- 一般而言，NLP 任务的输入有两种类型：one sentence、multi sentences
	- 如果输入是单个句子，则直接将这个句子输入给 BERT 即可
	- 如果输入是多个句子（例如 MRC 任务需要输入 Passage 和 Question，而 NLI 任务需要输入 Premise 和 Hypothesis），则在输入的句子间加上特殊的分隔符 "[SEP]"：该分隔符在 BERT 词表中是一个定值，从而可以表现在整体 embedding 中（在预训练时也得用 "[SEP]" 符号去分隔句子）
- 输出有四种类型：one class、class for each token、copy from input、general sequence
	- 如果输出是单个类别，即是一个句子分类任务。为了解此问题，在输入句子的前面加上一个 "[CLS]" 特殊符号。
		- 在预训练时，句子里的每个 token 位置的输出还是该 token 的词向量，而 "[CLS]" 符号对应的输出就是整个句子的向量表征。将句子向量表征输入给一个分类器（可以是简单的 MLP），即可完成句子分类任务。
		- 如果在预训练时没有使用 "[CLS]" 这个特殊符号，则只利用输入句子经过 BERT 后得到的所有词向量，再输入给一个分类器（可以是简单的 LSTM 处理变长序列），即可完成句子分类任务。
	- 如果需要进行序列标注任务，即给输入句子的每个 token 都进行分类，则只需将 BERT 输出的每个词向量输入给同一个分类器（可以是简单的 MLP 或 LSTM），去决定每个 token 的类别。
	- 如果需要 copy 输入序列中词到输出，解决 Seq2Seq 任务（例如 Extraction-based QA、Summarization、Dialogue）时都有可能直接使用输入的词作为输出。
		- 以区间式答案的 MRC 任务为例，需要预测每一个词 作为起始词 和 作为结束词 的概率。此时 task-specific classifier 只是两个向量，这两个向量各自与 Passage 每个 token 的 BERT 词向量做运算 (例如 内积)，得到的全部结果做 softmax 得到起始/结束概率分布。argmax 得到两个下标 s 和 e 分别表示起始 token 和结束 token，从而确定区间答案。
	- 如果需要输出一个(变长)序列，则有两种常见做法：
		- 1. 只需把 BERT 的输出词向量输入给一个 Decoder 模型，输出得到变长序列。但这样做的话，Decoder 是 task-specific 的，没有被 pre-train 到，输出句子的效果可能不会很好。
		- 2. 直接在 pre-train 过程中把 PLM 作为 Decoder 使用，输入一个句子，其末尾加上一个特殊字符。特殊字符的 BERT 输出再经过一个分类器得到第一时刻的输出单词。然后把该单词放到特殊字符的下一个位置作为输入，又能获得新的 BERT 编码，再经过同样的分类器就得到第二时刻的输出单词。此过程不断迭代，直到输出特殊的句子结束符号 "[EOS]" 为止

---

如果有一些 task-specific 的数据，则可以 fine-tune 精调模型。通常有三种做法：

- **固定住** 已训练好的 Pre-trained LM 的参数，使之只作为特征提取器。仅仅 fine-tune 调整下游的 task-specific 模型参数（下游模型的参数是随机初始化的）
- **不固定** 已训练好的 Pre-trained LM 的参数，训练时 PLM 和 下游模型的全部参数都可调（这种做法往往得到的效果优于上一种方法）
- **逐层解冻**：一开始固定住参数，随着训练进行，逐渐、逐层地放松 PLM 的参数，使之可随着下游模型一起训练

关于微调已训好的 PLM，还有其它策略如 Adaptor：由于联合微调会导致原本的 PLM 参数改变，因此每次针对某个下游任务进行联合微调后都要存储一个很大的模型（PLM 的参数量往往很大），因此 Adaptor 提出仅微调 PLM 的一小部分 layer，参考如下文献：

- [Stickland, et al., ICML’19] Asa Cooper Stickland,Iain Murray, BERT and PALs: Projected Attention Layers for Efficient Adaptation in Multi-Task Learning, ICML, 2019
- [Houlsby, et al., ICML’19] Neil Houlsby,Andrei Giurgiu,Stanislaw Jastrzebski,Bruna Morrone,Quentin de Laroussilhe,Andrea Gesmundo,Mona Attariyan,Sylvain Gelly, Parameter-Efficient Transfer Learning for NLP, ICML, 2019

另外一种可能的实现做法是：对 BERT 每层的输出做一个带参数、可训练的 Self-Attention，作为最终的 BERT 输出表征。这样联合微调时还是固定住 BERT 的参数，只是微调那个 Self-Attention 层而已，这就达到了 Adaptor 的效果。

# 3. PLM pre-train

要预训练一个语言模型，是要给 PLM 输入句子，输出句子中每个 token 的词向量表征，并且希望这些词向量都是考虑过上下文信息的。

CoVe 可能是最早的考虑上下文语义的预训练语言模型，它 pre-training by translation 是在翻译过程中获得输入句子中各 token 的 **上下文向量** (contextualized vector) 的。CoVe 得到的 PLM 即是翻译任务 Seq2Seq 模型中的 Encoder。

CoVe 专门选择了翻译作为 pre-trian 的任务，因为该任务往往需要考虑上下文。但问题在于该方法需要大量的标注数据，而不能无监督地学习，即利用 text without annotation。预训练模型中使用的“无监督”训练方法也往往被称作 **自监督训练**，其 “真值标签” 是从自己(本句话)中产生的。

> Yann LeCun: In **self-supervised learning**, the system learns to predict part of its input from other parts of its input. In other words, a portion of input is used as a supervisory signal to a predictor fed with the remaining portion of the input.

---

自监督训练的经典做法有两种：**自回归** Self-Regression、**自编码** Self-Encoding

> John Rupert Firth: You should know a word by the company it keeps.

因此目前主流认为单词的含义是由其上下文决定的（虽然我认为真实语义不止于此）。

## 3.1. 自回归预训练

自回归的任务是 Predict Next Token 根据(之前的)单词序列 预测下一个词。

使用 (Bi)LSTM 做自回归预训练的著名 PLM 模型有 **ULMFiT** (Universal Language Model Fine-tuning) 和 **ELMo**，参考：

- **ULMFiT** [Howard, et al., ACL’18] Jeremy Howard,Sebastian Ruder, *Universal Language Model Fine-tuning for Text Classification*, ACL, 2018
- **ELMo** [Peters, et al., NAACL’18] Matthew E. Peters, Mark Neumann, MohitIyyer, Matt Gardner, Christopher Clark, Kenton Lee, Luke Zettlemoyer, *Deep contextualized word representations*, NAACL, 2018

使用 (Masked) Self-Attention 做自回归预训练的著名 PLM 模型有 **GPT**、**Megatron**、**Turing NLG**，参考：

- **GPT-1** [Alec, et al., 2018] Alec Radford, KarthikNarasimhan, Tim Salimans, Ilya Sutskever, *Improving Language Understanding by Generative Pre-Training*, 2018
- **GPT-2** [Alec, et al., 2019] Alec Radford, Jeffrey Wu, RewonChild, David Luan, Dario Amodei, Ilya Sutskever, *Language Models are Unsupervised Multitask Learners*, 2019
- **GPT-3** [Brown, et al., 2020] *Language Models are Few-Shot Learners*, 2020
- **Megatron** [Shoeybi, et al., arXiv’19] Mohammad Shoeybi, Mostofa Patwary, Raul Puri, Patrick LeGresley, Jared Casper, Bryan Catanzaro, *Megatron-LM: Training Multi-Billion Parameter Language Models Using Model Parallelism*, arXiv, 19

设计此类自回归预训练模型的一个关键点在于：不能让模型提前预知后面的单词。否则模型会“作弊”，只需要把下个单词作为当前单词预测的 Next Token 即可满分，但这样模型学不到什么有用的东西。

鉴于此，这样的模型往往只是单向的建模，即便序列反向（ELMo 使用双向 LSTM），但那也不是实质上的“双向”：同时考虑上文和下文，预测本单词。

## 3.2. 自编码预训练

而基于自编码的 **BERT** 模型就可以做到同时考虑上下文信息。

BERT 不使用 Predict Next Token 任务，而是使用 MLM (Masked Language Model) 和 NSP (Next Sentence Predict)：

- MLM 任务是以一定概率 (15%) 在随机的位置用特殊字符来掩盖 (或 其它随机 Token 来替换) 输入序列中的某些单词，希望 BERT 模型能输出这些该掩盖/替换的单词；
- NSP 任务是输入两个句子 (以 "[SEP]" 分隔) 给 BERT，希望 BERT 判断后一个句子是否为前一个句子的下一句。

BERT 的基本结构是 Transformer，其中大量用到了 Self-Attention 和 Masked Self-Attention 结构。

BERT 的 MLM 任务和 Word2Vec 中的 CBOW 训练很相似，但 CBOW 用的模型很简单，且窗口大小有限。

但随机掩盖住输入语句中的 token 不一定是最好的方法，因为可能把一个语义单位的中间部分给盖住了，例如中文有很多词是多个汉字组成的。因此有研究提出 **WWM** (Whole Word Masking) 一次盖住一整个词汇，参考 Yiming Cui, Wanxiang Che, Ting Liu, Bing Qin, ZiqingYang, Shijin Wang, GuopingHu, *Pre-Training with Whole Word Masking for Chinese BERT*, arXiv, 2019

也有研究提出 **Phrase-level** 短语级别的 MASK 机制，以及 **Entity-level** 实体级别的 MASK 机制（先要进行 NER 命名实体识别），参考 Yu Sun, Shuohuan Wang, Yukun Li, Shikun Feng, Xuyi Chen, Han Zhang, Xin Tian, Danxiang Zhu, Hao Tian, Hua Wu, *ERNIE: Enhanced Representation through Knowledge Integration*, ACL, 2019

还有一种掩盖方法是 **SpanBERT**，一次掩盖一个区间，区间的长度是从一个预设的概率分布 (掩盖长度越短 概率越大) 中随机选取的，参考 Mandar Joshi, Danqi Chen, Yinhan Liu, Daniel S. Weld, Luke Zettlemoyer, Omer Levy, *SpanBERT: Improving Pre-training by Representing and Predicting Spans*, TACL, 2020

SpanBERT 中还提出了一个 **SBO** (Span Boundary Objective) 训练方法：有一个 SBO 模块，输入被盖住范围左边最靠近的一个 BERT 词向量 和 右边最靠近的一个 BERT 词向量，再输入一个正整数 n，SBO 模块输出被盖住范围的第 n 个单词。

这样的训练方法可以用在 Coreference Resolution 指代消解任务里面。因为该任务希望一个 span 前后两端的词向量 包含整个 span 中每个词的信息。

## 3.3. 排列语言模型

Permute Language Model

**XLNet** 的得名是因为其基本架构为 Transformer-**XL**，其优点是可以跨 segment 获取信息、有 relative 的 positional embedding 等。XLNet 参考 Zhilin Yang, Zihang Dai, Yiming Yang, Jaime Carbonell, Ruslan Salakhutdinov, Quoc V. Le, *XLNet: Generalized Autoregressive Pretrainingfor Language Understanding*, NeurIPS, 2019

XLNet 把输入句子中的 token 顺序随机打乱，有 $n!$ 种不同的排列（$n$ 为输入序列长度）。打乱之后进行常规的 LM 自回归任务：预测下一个单词。

这也可以用 BERT 的 MLM 任务的观点来看，只是 BERT 中利用未被掩盖的所有词 去预测被掩盖的词，而 XLNet 中仅仅(随机地)利用部分未被掩盖的词 去预测被掩盖的词。

另外，在输入方面，BERT 会把 "[MASK]" 特殊字符输入给模型，而 XLNet 不会这样做（这样做有利于 预训练过程 与 真实任务过程 的输入一致）。但即便不输入 "[MASK]" 特殊字符给模型，还是要输入 positional embedding，并且要说明待预测的词是哪个位置的词。（XLNet 为了做到给模型输入 positional information 而不输入 content information，对模型架构进行了特别的设计）

## 3.4. 降噪自编码器

生成句子 (Decoding) 过程往往是 auto-regressive 的过程，即由左到右地逐个生成单词，这对 BERT 有困难。即便可以通过在末尾输入 "[MASK]" 来产生 Decoding 的效果，但这样对 BERT 来说只利用到了 "[MASK]" 单词的左边部分，与 BERT 的 MLM 预训练方法有区别（同时看 "[MASK]" 的左右句子序列），因此效果往往不太好。

所以一般而言 BERT 比较缺乏 generation 的能力，它不太适合作为 Seq2Seq 模型的预训练模型，或者说 BERT 只适合作为 Encoder，而 Decoder 部分则需要根据下游任务从头训练。

**UniLM** 提出了混合的 self-attention masks，包含三种掩码 bidirectional LM, unidirectional LM, and sequence-to-sequence LM。第一个就是全关注，第二个是只关注前面的词 (自回归)，第三个是一部分全关注、另一部分只关注前面的词。

参考 arXiv 1905.03197 - UniLM - Unified Language Model Pre-training for Natural Language Understanding and Generation

---

可以使用 Self-Supervised 方法直接预训练一个 Seq2Seq 模型，其做法是输入句子给 Encoder，经过处理后得到的 Decoder 输出应该与输入的原句相近，即 reconstruct the input sequence。

但一个关键点是需要对输入给 Encoder 的 input sequence 做一定程度的破坏 corrupt，或称 “加噪声” noising。否则 Decoder 只需复制粘贴输入的句子即可满分，但模型学不到任何东西。

加噪声的方法主要有 **MASS** (Masked Sequence to Sequence Pre-training) 和 **BART** (Bidirectional and Auto-Regressive Transformers)，参考：

- **MASS** [Song, et al., ICML’19] KaitaoSong, Xu Tan, Tao Qin, JianfengLu, Tie-Yan Liu, *MASS: Masked Sequence to Sequence Pre-training for Language Generation*, ICML, 2019
- **BART** [Lewis, et al., arXiv’19] Mike Lewis, Yinhan Liu, Naman Goyal, Marjan Ghazvininejad, Abdelrahman Mohamed, Omer Levy, Ves Stoyanov, Luke Zettlemoyer, *BART: Denoising Sequence-to-Sequence Pre-training for Natural Language Generation, Translation, and Comprehension*, arXiv, 2019

### 3.4.1. MASS

- MASS 对 Seq2Seq 模型联合训练（BERT 只训练 Encoder、GPT 只训练 Decoder、XLM 分开训练 Encoder 和 Decoder）
- 它随机掩盖长度为 k 的一整个区间的词 (区间中的每个词都替换成 "[MASK]") 输入给 Encoder，然后把 Encoder 的输出 输入给 Decoder，目标是让 Decoder 输出原句中被掩盖的词。
- 每个时间步输入给 Decoder 的词，是原句的逆 (原来被掩盖的目标词不被掩盖了、未被掩盖的上下文词却被掩盖了，从而让 Decoder 多去利用 Encoder 输出的信息) 往右移位一个单位 (否则就看到答案了)
	- 采用 teacher forcing 方法 (训练时可以慢慢减小 teacher forcing 概率，提升看 Decoder 上一时刻输出的概率)
- 当掩盖区间的窗口大小 k=1 时类似于 BERT、当 k=m 时 (m 为原句长度) 类似 GPT。实验证明 k=0.5 时效果最佳。

---

在 BART 论文里指出 MASS 的缺点：

> MASS is **less effective for discriminative tasks**, because disjoint sets of tokens are fed into the encoder and decoder.

---

**SpanBERT** 也是把一个整个区间的词都替换成 "[MASK]"，但它只作用于 Encoder，而且目标是 (span-boundary objective, SBO 任务) 是仅仅根据区间左右两端 未被掩盖那两个单词 的语义编码 去预测/还原区间中的某个词。(“某个” 是可以通过输入一个区间内序号来指定的)。参考：

1907.10529 - SpanBERT- Improving Pre-training by Representing and Predicting Spans

### 3.4.2. BART

BART (Bidirectional and Auto-Regressive Transformers) 

参考 arXiv 1910.13461 - BART- Denoising Sequence-to-Sequence Pre-training for Natural Language Generation, Translation, and Comprehension

BART 也是直接对 Seq2Seq 模型两大部分联合训练，采用了如下五种 noising 方法 (对 Encoder)：

- **Token Masking**：类似 BERT 的 MLM 任务，随机用 [MASK] 掩盖单词
- **Token Deletion**：随机删除（对模型来说，删除比 MASK 更难，因为模型根据输入 无法直接知道哪个位置缺失了）
- **Text Infilling**：随机掩盖一个或多个区间 (每个区间仅用 **单个 [MASK]** 去掩盖)，区间长度最短为 0 (为 0 时即为插入 [MASK])。区间长度采样自参数 $\lambda=3$ 的 Poisson 分布 (期望和方差均为 $\lambda$)
- **Sentence Permutation**：用句号分隔出多个句子，然后随机打乱其顺序
- **Document Rotation**：从均匀分布中采样 选定一个 token，然后对句子循环移位，让选定的 token 作为句首单词。

实验表明 Text Infilling + Sentence Permutation 效果最佳，尤其是 Text Infilling 效果很好。

## 3.5. 生成判别预训练

2003.10555 - ELECTRA - Pre-training Text Encoders as Discriminators Rather Than Generators

训练时，用一个小的 BERT 类模型作为生成器 G，真正目标训练的模型 ELECTRA 作为判别器 D。

先对原句随机掩盖词，然后让 G 执行 MLM 任务预测被掩盖的词，输出完整的与原句等长的句子。G 的输出 输入给 D，D 对每个位置的词进行二分类判断：是否与原句相应位置词相同

不采用 GAN 中的迭代对抗训练方法，而是直接端到端联合训练，混合损失函数为 MLM 任务和判别任务的加权和（下式中的 $\boldsymbol{x} = [x_1, ..., x_k]$ 为输入序列）：

$$\mathop{\min}\limits_{\theta_{G}, \theta_{D}} \sum_{\boldsymbol{x} \in \mathcal{X}} \mathcal{L}_{MLM} (\boldsymbol{x}, \theta_{G}) + \lambda \mathcal{L}_{Disc} (\boldsymbol{x}, \theta_{D})$$

其中两个损失函数分别为（下式中的 $\boldsymbol{m} = [m_1, ..., m_k]$ 为被掩盖的词下标）

$$\mathcal{L}_{MLM} (\boldsymbol{x}, \theta_{G}) = \mathbb{E} \left( \sum_{i \in \boldsymbol{m}} - \log p_G (x_i | \boldsymbol{x}^{masked}) \right)$$

$$\mathcal{L}_{Disc} (\boldsymbol{x}, \theta_{G}) = \mathbb{E} \left( \sum_{t=1}^{n} - \mathbb{I} (x_{t}^{corrupt} = x_t) \log D(\boldsymbol{x}^{corrupt}, t) - \mathbb{I} (x_{t}^{corrupt} \neq x_t) \log (1 - D(\boldsymbol{x}^{corrupt}, t)) \right)$$

## 3.6. 多语言 PLM

> **mBART** is the **first** method for pre-training a **complete sequence-to-sequence model** by denoising full texts in **multiple languages**, while previous approaches have focused only on the encoder, decoder, or reconstructing parts of the text.

参考 arXiv 2001.08210 - mBART - Multilingual Denoising Pre-training for Neural Machine Translation

mBART 指出 BART 仅关注于 English corpora，而它是首个采用多语言进行完全 Seq2Seq 训练的模型。它考虑了 25 种语言，包括高资源和低资源场景。

此外 mBART 还指出过去的许多预训练模型只考虑了部分应用场景，而 mBART 在句子级 MT、文档级 MT 以及无监督(主要是小样本)任务下都表现出色。（但 mBART 不适合于高资源场景）

---

问题：很多评价都是和 randomly initialized baseline 对比，这只能说明预训练很有效，但是这件事很显然。

## 3.7. 多任务学习 PLM

参考 2010.02523 - MTLmNMT - Multi-task Learning for Multilingual Neural Machine Translation

对预训练+微调范式而言，用 in-domain data 去 fine-tune 后往往导致 general-domain 的模型效果下降，这被称为 catastrophic forgetting effect。

有研究让模型在 general-domain 进行预训练后，知道哪些参数最关键。于是在用 in-domain data 进行微调时，利用 EWC 正则化方法来限制那些关键参数尽量不被修改。参考 2019 NAACL - Overcoming Catastrophic Forgetting During Domain Adaptation of Neural Machine Translation

而且分开的预训练和微调过程，使得 MNMT 系统在引入额外单语语料或新语言时 缺乏灵活性。

本模型以机器翻译任务作为预训练任务，并且与两个辅助任务 (MLM 和 DAE) 联合训练 来辅助提升预训练效果，从而能够在 MNMT 系统中有效地利用单语语料。

### 多任务

- MLM 针对 Encoder 部分，利用与 BERT 类似的自编码机制。
- DAE 针对整个 Seq2Seq 模型，利用了 BART 中的三种 noising 方法。

翻译任务交叉熵损失：

$$\mathcal{L}_{MT} = \mathbb{E}_{(x, y) \sim D_B} [ - \log P(y | x) ]$$

MLM 任务也是交叉熵损失，预测被掩盖的 token

DAE 损失还是交叉熵损失，重构被破坏的句子：

$$\mathcal{L}_{DAE} = \mathbb{E}_{x \sim D_M} [ - \log P(x | D(x)) ]$$

因此联合训练的损失为

$$\mathcal{L} = \mathcal{L}_{MT} + \mathcal{L}_{MLM} + \mathcal{L}_{DAE}$$

### 任务调度

**Dynamic Data Sampling** 处理数据不平衡的情况，多语言的语料库大小不同，因此引入采样率

$$(\frac{|D_l|}{\sum_{k} |D_k|})^{\frac{1}{T}}$$

其中 T 为 sampling temperature。对于第 k 个 epoch 有：

$$T(k) = \min( T_m, (k-1) \frac{T_m - T_0}{N} + T_0 )$$

其中 $T_0$ 和 $T_m$ 分别为 T 的初始值 和 预设的最大值，而 N 是 warm-up 轮数。

---

**Dynamic Noising Ratio** 用于调控 MLM 中的掩盖率 和 DAE 中 Text Infilling 任务的加噪区间数目，越低则任务越简单。逐渐增加任务难度有助于模型训练，因此对于第 k 个 epoch 有：

$$R(k) = \min( R_m, (k-1) \frac{R_m - R_0}{M} + R_0 )$$

类似于 $T(k)$，$R(k)$ 也是从初始值 $R_0$ 开始每轮线性增长，直到 warm-up 轮数 M 达到后 就固定在 $R_m$ 值了。

### 模型评估

在低资源场景下表现好，但在高资源场景下表现不佳。

Back-Translation 很耗时间

在 En->X language pairs 翻译任务上的 BLEU 值 胜过 mBART。

Dynamic Data Sampling 在 En->X 和 X->En 任务上都比固定采样率 T=5 更好。

至于 MLM 和 DAE 的 noising method：

> the model benefits most from the **word-level MLM** and the **span-level Text Infilling** task for DAE

而 Dynamic Noising Ratio 相比于固定的噪声率而言，没有对效果的明显提升。作者怀疑是数据量不足，因此在大规模单语语料场景下重新测试，发现还是动态的更好。

---

mBERT 和 XLM-Roberta 是使用了大量多语言语料训练的 PLM（只使用 MLM 任务预训练），同样大规模的 MNMT 模型（只在 NMT 任务上训练）在 NLU 任务上无法达到 PLM 的性能。但是结合了 MT、MLM、DAE 三种任务的本模型可以胜过 mBERT 和 XLM-Roberta。这体现了多任务联合训练的重要性。
