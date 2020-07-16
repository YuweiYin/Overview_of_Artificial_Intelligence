# MRC - Machine Reading Comprehension

By [YuweiYin](https://github.com/YuweiYin)

---

## 1. MRC 概述

**Book**: Reading for Understanding. Towards an R&D Program in Reading Comprehension

- Author: Catherine Snow, Chair
- [Paper Download](https://www.academia.edu/download/38406216/Reading_for_understanding_Toward_an_R_D_program_in_reading_comprehension.pdf)

```
@techreport{snow2002reading,
  title={Reading for Understanding. Towards an R\&D Program in Reading Comprehension},
  author={Snow, Catherine},
  year={2002},
  institution={RAND CORP SANTA MONICA CA}
}
```

---

**paper**: Revisiting Unreasonable Effectiveness of Data in Deep Learning Era

- Author: Chen Sun, Abhinav Shrivastava, Saurabh Singh, Abhinav Gupta
- [Paper Download](http://openaccess.thecvf.com/content_ICCV_2017/papers/Sun_Revisiting_Unreasonable_Effectiveness_ICCV_2017_paper.pdf)

```
@inproceedings{sun2017revisiting,
  title={Revisiting unreasonable effectiveness of data in deep learning era},
  author={Sun, Chen and Shrivastava, Abhinav and Singh, Saurabh and Gupta, Abhinav},
  booktitle={Proceedings of the IEEE international conference on computer vision},
  pages={843--852},
  year={2017}
}
```

---

## 2. MRC 效果测评

### 2.1. MRC 的答案形式

- **多项选择式**：模型需要从给定的若干选项中选出正确答案。
- **完形填空式**：在原文中除去若干关键词，需要模型填入正确的单词或短语。
- **区间答案式**：答案限定是文章中的一个子句，需要模型在文章中表明正确的答案起始位置和终止位置。
- **自由回答式**：不限定模型生成答案的形式，允许模型自有生成语句。
- **无答案/无法回答**(unanswerable)：一个问题在当前给定文章中没有答案。

多项选择 和 完形填空 属于客观类答案，测评时可以将模型答案直接与正确答案进行比较，并以**准确率**作为评测指标，因此相对易于计算。

区间式答案属于半客观类答案，可以将模型答案直接以字符串形式与标准答案进行比较。完全相同时得分为 1，否则为 0，这种衡量标准被称为 **精确匹配**(exact match)。除了精确匹配外，还有 **F1** 衡量标准，它是 **准确率**(precision) 和 **召回率**(recall) 的调和平均数，即 $ F_1 = 2 \times \frac{p \times r}{p + r} $。如果需要侧重准确率或者侧重召回率，可以采用加权的 F1 指数。

自由回答式答案是其中最为灵活的一种答案形式。理想的测评指标是：模型答案与标准答案的 **语义** 完全相同时得满分，否则部分得分 或者 不得分。但是语义的表征与比较本身就是自然语言处理领域的核心难题之一，没有很好的解决方案。而如果完全采用人工评分，效率又太低，而且标准难以统一。因此，一般采用单词水平的匹配率作为自由式答案的评分标准，常见的标准有 ROUGE、BLEU 和 METEOR 等。

**人类水平** 往往指的是单个人类在数据集问题上的得分（或者是多个人各自测试的得分均值）。而 **满分答案** 往往是指多个人类(协同解题)的答案集合或投票结果。绝对正确的完美答案往往是无法获得的。所以机器模型“超越人类水平”往往是指超越了某个(或某几个)标注者，而不是胜过全人类。

### 2.2. MRC 评估指标

***Rouge***

**paper**: Rouge: A Package for Automatic Evaluation of Summaries

- Author: Chin-Yew Lin
- [Paper Download](https://www.aclweb.org/anthology/W04-1013.pdf)

```
@inproceedings{lin2004rouge,
  title={Rouge: A package for automatic evaluation of summaries},
  author={Lin, Chin-Yew},
  booktitle={Text summarization branches out},
  pages={74--81},
  year={2004}
}
```

---

***BLEU***

**paper**: BLEU: a Method for Automatic Evaluation of Machine Translation

- Author: Kishore Papineni, Salim Roukos, Todd Ward, Wei-Jing Zhu
- [Paper Download](https://www.aclweb.org/anthology/P02-1040.pdf)

```
@inproceedings{papineni2002bleu,
  title={BLEU: a method for automatic evaluation of machine translation},
  author={Papineni, Kishore and Roukos, Salim and Ward, Todd and Zhu, Wei-Jing},
  booktitle={Proceedings of the 40th annual meeting of the Association for Computational Linguistics},
  pages={311--318},
  year={2002}
}
```

---

***METEOR***

**paper**: Meteor Universal: Language Specific Translation Evaluation for Any Target Language

- Author: Michael Denkowski, Alon Lavie
- Meteor website: [Meteor Homeapge](http://www.cs.cmu.edu/~alavie/METEOR/) [Meteor 1.5](http://www.cs.cmu.edu/~alavie/METEOR/README.html)
- [Paper Download](https://www.aclweb.org/anthology/W14-3348.pdf)

```
@inproceedings{denkowski2014meteor,
  title={Meteor universal: Language specific translation evaluation for any target language},
  author={Denkowski, Michael and Lavie, Alon},
  booktitle={Proceedings of the ninth workshop on statistical machine translation},
  pages={376--380},
  year={2014}
}
```

### 2.3. MRC 评估相关文章

**paper**: Adversarial Examples for Evaluating Reading Comprehension Systems

- Author: Robin Jia, Percy Liang
- Paper Link: [arXiv](https://arxiv.org/abs/1707.07328)
- Paper Download: [arXiv](https://arxiv.org/pdf/1707.07328.pdf)

```
@article{jia2017adversarial,
  title={Adversarial examples for evaluating reading comprehension systems},
  author={Jia, Robin and Liang, Percy},
  journal={arXiv preprint arXiv:1707.07328},
  year={2017}
}
```

---

**paper**: Prerequisite Skills for Reading Comprehension: Multi-Perspective Analysis of MCTest Datasets and Systems

- Author: Saku Sugawara, Hikaru Yokono, Akiko Aizawa
- Paper Link: [AAAI2017](https://www.aaai.org/ocs/index.php/AAAI/AAAI17/paper/viewPaper/14614)
- Paper Download: [AAAI2017](https://www.aaai.org/ocs/index.php/AAAI/AAAI17/paper/download/14614/14082) [AAAI2017 Preview](https://www.aaai.org/ocs/index.php/AAAI/AAAI17/paper/view/14614/14082)

```
@inproceedings{sugawara2017prerequisite,
  title={Prerequisite skills for reading comprehension: Multi-perspective analysis of mctest datasets and systems},
  author={Sugawara, Saku and Yokono, Hikaru and Aizawa, Akiko},
  booktitle={Thirty-First AAAI Conference on Artificial Intelligence},
  year={2017}
}
```

此文指出机器阅读理解模型应该具有如下 10 种基本技能：

技能 | 解释
:-: | :-:
枚举和列举 | 追踪、记录并列出文章中重要概念和实体
数学运算 | 基本数学运算和几何理解能力
指代消除 | 理解文章中的指代关系
逻辑推理 | 归纳、推理、条件识别
类比和比喻 | 理解语言中的比喻和暗喻
时空关系 | 分析事件和物体的时间和空间关系
因果关系 | 理解事件之间的因果逻辑关系
常识推理 | 根据各种常识进行推演分析
修辞理解 | 理解各种分句和从句
特殊语言结构 | 理解语言形式、构造、标点等的含义

## 3. MRC 数据集

### 3.1. 单段落式数据集

***RACE***

- Info
	- 提出年份：2017 年
	- 提出机构：CMU 大学
	- 文本语种：English 英文
	- 数据来源：中国中学生的英语考试题目
		- RACE-M 是初中生题目
		- RACE-H 是高中生题目
		- 采集过程中使用了 OCR 光学字符识别技术
	- 文本量级：28,000 篇文章
	- 问题量级：近 10 万多个多项选择题
	- 问题类型：多项选择式
- **paper**
	- RACE: Large-scale ReAding Comprehension Dataset From Examinations
	- Author: Guokun Lai, Qizhe Xie, Hanxiao Liu, Yiming Yang, Eduard Hovy
	- [Paper Download](https://arxiv.org/pdf/1704.04683.pdf)

```
@article{lai2017race,
  title={Race: Large-scale reading comprehension dataset from examinations},
  author={Lai, Guokun and Xie, Qizhe and Liu, Hanxiao and Yang, Yiming and Hovy, Eduard},
  journal={arXiv preprint arXiv:1704.04683},
  year={2017}
}
```

---

***NewsQA***

- Info
	- 提出年份：2016 年
	- 提出机构：Maluuba 公司
	- 文本语种：English 英文
	- 数据来源：CNN 新闻稿
	- 文本量级：12,000 多篇新闻稿
	- 问题量级：近 12 万个人工编辑的问题
	- 问题类型：区间答案式 + 无法回答型
	- 其它：考察模型的推理和归纳能力，从多个不同位置获取信息
- **paper**
	- NewsQA: A Machine Comprehension Dataset
	- Author: Adam Trischler, Tong Wang, Xingdi Yuan, Justin Harris, Alessandro Sordoni, Philip Bachman, Kaheer Suleman
	- [Paper Download](https://arxiv.org/pdf/1611.09830.pdf)

```
@article{trischler2016newsqa,
  title={Newsqa: A machine comprehension dataset},
  author={Trischler, Adam and Wang, Tong and Yuan, Xingdi and Harris, Justin and Sordoni, Alessandro and Bachman, Philip and Suleman, Kaheer},
  journal={arXiv preprint arXiv:1611.09830},
  year={2016}
}
```

---

***CNN/Daily Mail***

- Info
	- 提出年份：2015 年
	- 提出机构：DeepMind 公司
	- 文本语种：English 英文
	- 数据来源：媒体 CNN 和 Daily Mail
	- 数据规模：1,400,000 个样例，每个样例含一篇文章、一个问题和相应答案
	- 问题类型：完形填空式
	- 其它：为了使模型更关注于对语义的理解，文章中的实体信息(如人名、地名等)均用编号代替。模型需要根据问题从文章中选出正确的实体编号填入 `@placeholder` 处。
- **paper**
	- Teaching Machines to Read and Comprehend
	- Author: Karl Moritz Hermann, Tomas Kocisky, Edward Grefenstette, Lasse Espeholt, Will Kay, Mustafa Suleyman, Phil Blunsom
	- [Paper Link](http://papers.nips.cc/paper/5945-teaching-machines-to-read-and-comprehend)
	- [Paper Download](http://117.128.6.29/cache/papers.nips.cc/paper/5945-teaching-machines-to-read-and-comprehend.pdf?ich_args2=470-23133105046735_6342ef062d4b126cdf21b3e261ca4b88_10001002_9c896d2edfcaf1d29739518939a83798_5e800ede6545a884fb21b29f9423936c)

```
@inproceedings{hermann2015teaching,
  title={Teaching machines to read and comprehend},
  author={Hermann, Karl Moritz and Kocisky, Tomas and Grefenstette, Edward and Espeholt, Lasse and Kay, Will and Suleyman, Mustafa and Blunsom, Phil},
  booktitle={Advances in neural information processing systems},
  pages={1693--1701},
  year={2015}
}
```

---

***SQuAD***

- [SQuAD Homepage](https://rajpurkar.github.io/SQuAD-explorer/)
- SQuAD 1
	- Info
		- 提出年份：2016 年
		- 提出机构：Stanford 大学
		- 文本语种：English 英文
		- 数据来源：Wikipedia 维基百科
		- 文本量级：536 篇维基百科文章
		- 问题量级：10 万多个问题
		- 问题类型：区间答案式 + 无法回答型
		- 其它：SQuAD 规模大、质量高，因此备受关注
	- **paper**
		- SQuAD: 100,000+ Questions for Machine Comprehension of Text
		- Author: Pranav Rajpurkar, Jian Zhang, Konstantin Lopyrev, Percy Liang
		- [Paper Link](https://arxiv.org/abs/1606.05250)
- SQuAD 2
	- Info
		- 提出年份：2018 年
		- 提出机构：Stanford 大学
		- 文本语种：English 英文
		- 数据来源：Wikipedia 维基百科
		- 文本量级：
		- 问题量级：15 万多个问题
		- 问题类型：区间答案式 + 无法回答型
		- 其它：相较于 SQuAD 1，增加了大量无法回答型问题
	- **paper**
		- Know What You Don't Know: Unanswerable Questions for SQuAD
		- Author: Pranav Rajpurkar, Robin Jia, Percy Liang
		- [Paper Link](https://arxiv.org/abs/1806.03822)

```
@article{rajpurkar2016squad,
  title={Squad: 100,000+ questions for machine comprehension of text},
  author={Rajpurkar, Pranav and Zhang, Jian and Lopyrev, Konstantin and Liang, Percy},
  journal={arXiv preprint arXiv:1606.05250},
  year={2016}
}
```

```
@article{rajpurkar2018know,
  title={Know what you don't know: Unanswerable questions for SQuAD},
  author={Rajpurkar, Pranav and Jia, Robin and Liang, Percy},
  journal={arXiv preprint arXiv:1806.03822},
  year={2018}
}
```

---

***CoQA***

- Info
	- 提出年份：2018 年
	- 提出机构：Stanford 大学
	- 文本语种：English 英文
	- 数据来源：
	- 文本量级：8,000 多个段落，平均每个段落有 15 轮问答
	- 问题量级：12 万多个问题
	- 问题类型：区间答案式 + 无法回答型 + 是/否型判断 + 少量自由式回答
	- 其它：CoQA 是多轮对话式机器阅读理解竞赛，其最大特点是在问答过程中加入了上下文，即对每个段落提出多轮问题，模型需要理解上下文。
- **paper**
	- CoQA: A Conversational Question Answering Challenge
	- Author: Siva Reddy, Danqi Chen, Christopher D. Manning
	- [Paper Link](https://www.mitpressjournals.org/doi/full/10.1162/tacl_a_00266)
	- [Paper Download](https://www.mitpressjournals.org/doi/pdf/10.1162/tacl_a_00266)

```
@article{reddy2019coqa,
  title={Coqa: A conversational question answering challenge},
  author={Reddy, Siva and Chen, Danqi and Manning, Christopher D},
  journal={Transactions of the Association for Computational Linguistics},
  volume={7},
  pages={249--266},
  year={2019},
  publisher={MIT Press}
}
```

### 3.2. 多段落式数据集

***MS MARCO***

- Info
	- 提出年份：2016 年
	- 提出机构：Microsoft 公司
	- 文本语种：English 英文
	- 数据来源：问题来自真实用户提交的问题、相关的多个段落来自 Bing 搜索引擎对查询的(排名靠前的)检索结果
	- 文本量级：800 万多篇文章
	- 问题量级：100 万多个问题
	- 问题类型：自由回答式
	- 其它：MS MARCO 提供了 3 个竞赛任务
		- 判断是否可以从给定段落的信息中得到问题的答案
		- 生成答案语句
		- 按照与问题的相关性对给定的多个段落进行排序
- **paper**
	- MS MARCO: A Human Generated MAchine Reading COmprehension Dataset
	- Author: Payal Bajaj, Daniel Campos, Nick Craswell, Li Deng, Jianfeng Gao, Xiaodong Liu, Rangan Majumder, Andrew McNamara, Bhaskar Mitra, Tri Nguyen, Mir Rosenberg, Xia Song, Alina Stoica, Saurabh Tiwary, Tong Wang
	- Paper Link: [ICLR2017](https://openreview.net/forum?id=Hk1iOLcle&noteId=Hk1iOLcle) [arXiv]((https://arxiv.org/abs/1611.09268)
	- Paper Download: [ICLR2017](https://openreview.net/pdf?id=Hk1iOLcle) [arXiv](https://arxiv.org/pdf/1611.09268.pdf)

```
@article{nguyen2016ms,
  title={Ms marco: A human-generated machine reading comprehension dataset},
  author={Nguyen, Tri and Rosenberg, Mir and Song, Xia and Gao, Jianfeng and Tiwary, Saurabh and Majumder, Rangan and Deng, Li},
  year={2016}
}
```

---

***DuReader***

- Info
	- 提出年份：2017 年
	- 提出机构：百度 Baidu 公司
	- 文本语种：中文 Chinese
	- 数据来源：Baidu 搜索引擎的用户查询和相关文档
	- 数据规模：20 万个问题和 100 万篇相关文档
	- 问题类型：自由回答式 + 是/否型判断
	- 其它：
		- 与 MS MARCO 其中一个不同点在于：DuReader 给出的文章是检索到的全文，而不是像 MS MARCO 一样给出各个段落。这加大了模型处理的难度。
		- 另外，由于文章的立场的观点不尽相同，DuReader 对一些问题提供了多个标准答案，这更符合真实的问答情景。
- **paper**
	- DuReader: a Chinese Machine Reading Comprehension Dataset from Real-world Applications
	- Author: Wei He, Kai Liu, Jing Liu, Yajuan Lyu, Shiqi Zhao, Xinyan Xiao, Yuan Liu, Yizhong Wang, Hua Wu, Qiaoqiao She, Xuan Liu, Tian Wu, Haifeng Wang
	- Paper Link: [arXiv](https://arxiv.org/abs/1711.05073)
	- Paper Download: [arXiv](https://arxiv.org/pdf/1711.05073.pdf)

```
@article{he2017dureader,
  title={Dureader: a chinese machine reading comprehension dataset from real-world applications},
  author={He, Wei and Liu, Kai and Liu, Jing and Lyu, Yajuan and Zhao, Shiqi and Xiao, Xinyan and Liu, Yuan and Wang, Yizhong and Wu, Hua and She, Qiaoqiao and others},
  journal={arXiv preprint arXiv:1711.05073},
  year={2017}
}
```

---

***QAngaroo***

- Info
	- 提出年份：2017 年
	- 提出机构：UoL 伦敦大学
	- 文本语种：English 英文
	- 数据来源
		- WikiHop 来源于维基百科
		- MedHop 来源于医疗论文库 PubMed 的论文摘要
	- 数据规模：5 万多个问题和相关文档
	- 问题类型：多项选择式
	- 其它：QAngaroo 是多文档推理阅读理解数据集，其最大特点是问题的答案并不能仅从一个段落中单独得出，其中的线索分散在多个段落中，需要寻找线索并进行 **多跳推理** (multi-hop reasoning)。
- **paper**
	- Constructing Datasets for Multi-hop Reading Comprehension Across Documents
	- Author: Johannes Welbl, Pontus Stenetorp, Sebastian Riedel
	- Paper Link: [The MIT Press Journals](https://www.mitpressjournals.org/doi/abs/10.1162/tacl_a_00021)
	- Paper Download: [The MIT Press Journals](https://www.mitpressjournals.org/doi/pdf/10.1162/tacl_a_00021)

```
@article{welbl2018constructing,
  title={Constructing datasets for multi-hop reading comprehension across documents},
  author={Welbl, Johannes and Stenetorp, Pontus and Riedel, Sebastian},
  journal={Transactions of the Association for Computational Linguistics},
  volume={6},
  pages={287--302},
  year={2018},
  publisher={MIT Press}
}
```

---

***HotpotQA***

- Info
	- 提出年份：2018 年
	- 提出机构：CMU 大学、Stanford 大学、Montréal 蒙特利尔大学、Google 公司
	- 文本语种：English 英文
	- 数据来源：
	- 数据规模：11 万个问题和相关的维基百科段落
	- 问题类型：区间答案式
	- 其它：HotpotQA 是多段落推理阅读理解数据集。与 QAngaroo 类似，需要模型能够在多个文档中寻找线索并经过多步推理得出答案。
- **paper**
	- HotpotQA: A Dataset for Diverse, Explainable Multi-hop Question Answering
	- Author: Zhilin Yang, Peng Qi, Saizheng Zhang, Yoshua Bengio, William W. Cohen, Ruslan Salakhutdinov, Christopher D. Manning
	- Paper Link: [arXiv](https://arxiv.org/abs/1809.09600)
	- Paper Download: [arXiv](https://arxiv.org/pdf/1809.09600.pdf)

```
@article{yang2018hotpotqa,
  title={Hotpotqa: A dataset for diverse, explainable multi-hop question answering},
  author={Yang, Zhilin and Qi, Peng and Zhang, Saizheng and Bengio, Yoshua and Cohen, William W and Salakhutdinov, Ruslan and Manning, Christopher D},
  journal={arXiv preprint arXiv:1809.09600},
  year={2018}
}
```

### 3.3. 文本库式数据集

***ARC***: AI2 Reasoning Challenge

- Info
	- 提出年份：2018 年
	- 提出机构：Allen Institute for AI 艾伦人工智能研究院
	- 文本语种：English 英文
	- 数据来源：美国三到九年级学生的科学课试题
	- 数据规模：7800 道关于科学知识的问题 及其答案
	- 问题类型：多项选择式
	- 其它：数据集中还提供了一个大型科学文本库，来源于搜索引擎对科学问题的查询结果，共包含 1400 多万个句子。模型可以使用文本库中的信息回答问题，也可以通过其他途径获得相关信息。
- **paper**
	- Think you have Solved Question Answering? Try ARC, the AI2 Reasoning Challenge
	- Author: Peter Clark, Isaac Cowhey, Oren Etzioni, Tushar Khot, Ashish Sabharwal, Carissa Schoenick, Oyvind Tafjord
	- Paper Link: [arXiv](https://arxiv.org/abs/1803.05457)
	- Paper Download: [arXiv](https://arxiv.org/pdf/1803.05457.pdf)

```
@article{clark2018think,
  title={Think you have solved question answering? try arc, the ai2 reasoning challenge},
  author={Clark, Peter and Cowhey, Isaac and Etzioni, Oren and Khot, Tushar and Sabharwal, Ashish and Schoenick, Carissa and Tafjord, Oyvind},
  journal={arXiv preprint arXiv:1803.05457},
  year={2018}
}
```

## 4. MRC 技术

### 4.1. 编码

***BPE***: 字节对编码 Byte Pair Encoder

**paper**: Neural Machine Translation of Rare Words with Subword Units

- Author: Rico Sennrich, Barry Haddow, Alexandra Birch
- Paper Link: [arXiv](https://arxiv.org/abs/1508.07909)
- Paper Download: [arXiv](https://arxiv.org/pdf/1508.07909.pdf)

```
@article{sennrich2015neural,
  title={Neural machine translation of rare words with subword units},
  author={Sennrich, Rico and Haddow, Barry and Birch, Alexandra},
  journal={arXiv preprint arXiv:1508.07909},
  year={2015}
}
```

---

***Word2Vec***: Word to Vector Encoding

**paper**: Distributed Representations of Words and Phrases and their Compositionality

- Author: Tomas Mikolov, Ilya Sutskever, Kai Chen, Greg S. Corrado, Jeff Dean
- Paper Link: [NIPS2013](http://papers.nips.cc/paper/5021-distributed-representations-of-words-and-phrases-and)
- Paper Download: [NIPS2013](https://papers.nips.cc/paper/5021-distributed-representations-of-words-and-phrases-and-their-compositionality.pdf)

```
@inproceedings{mikolov2013distributed,
  title={Distributed representations of words and phrases and their compositionality},
  author={Mikolov, Tomas and Sutskever, Ilya and Chen, Kai and Corrado, Greg S and Dean, Jeff},
  booktitle={Advances in neural information processing systems},
  pages={3111--3119},
  year={2013}
}
```

---

***Word2Vec***: Word to Vector Encoding

**paper**: Distributed Representations of Words and Phrases and their Compositionality

- Author: Tomas Mikolov, Ilya Sutskever, Kai Chen, Greg S. Corrado, Jeff Dean
- Paper Link: [NIPS2013](http://papers.nips.cc/paper/5021-distributed-representations-of-words-and-phrases-and)
- Paper Download: [NIPS2013](https://papers.nips.cc/paper/5021-distributed-representations-of-words-and-phrases-and-their-compositionality.pdf)
- word2vec code: [Google code](https://code.google.com/archive/p/word2vec/)
- Trained w2v: [using Google News data](https://github.com/mmihaltz/word2vec-GoogleNews-vectors) 

```
@inproceedings{mikolov2013distributed,
  title={Distributed representations of words and phrases and their compositionality},
  author={Mikolov, Tomas and Sutskever, Ilya and Chen, Kai and Corrado, Greg S and Dean, Jeff},
  booktitle={Advances in neural information processing systems},
  pages={3111--3119},
  year={2013}
}
```

### 4.2. 语言模型

语言模型 (Language Model) 是给合法语句赋予较大的出现概率，而给罕见的或者不会出现的语句赋予很小的出现概率。

语言模型建立了语句的概率模型，其评测标准即为在真实文本数据集上最大化实际出现的语句的概率。

当前最好的语言模型(如下论文)可以做到 35.8 左右的 Perplexity (困惑度)，越低越好。

**paper**: Language Models are Unsupervised Multitask Learners

- Author: Alec Radford, Jeffrey Wu, Rewon Child, David Luan, Dario Amodei, Ilya Sutskever
- [Paper Download](https://www.ceid.upatras.gr/webpages/faculty/zaro/teaching/alg-ds/PRESENTATIONS/PAPERS/2019-Radford-et-al_Language-Models-Are-Unsupervised-Multitask-%20Learners.pdf)

```
@article{radford2019language,
  title={Language models are unsupervised multitask learners},
  author={Radford, Alec and Wu, Jeffrey and Child, Rewon and Luan, David and Amodei, Dario and Sutskever, Ilya},
  journal={OpenAI Blog},
  volume={1},
  number={8},
  pages={9},
  year={2019}
}
```

### 其它技巧

**拷贝-生成机制** copy-generate mechanism

**paper**: Incorporating Copying Mechanism in Sequence-to-Sequence Learning

- Author: Jiatao Gu, Zhengdong Lu, Hang Li, Victor O.K. Li
- Paper Link: [arXiv](https://arxiv.org/abs/1603.06393)
- Paper Download: [arXiv](https://arxiv.org/pdf/1603.06393.pdf)

```
@article{gu2016incorporating,
  title={Incorporating copying mechanism in sequence-to-sequence learning},
  author={Gu, Jiatao and Lu, Zhengdong and Li, Hang and Li, Victor OK},
  journal={arXiv preprint arXiv:1603.06393},
  year={2016}
}
```

---

**高速路网络**

**paper**: Highway Networks

- Author: Rupesh Kumar Srivastava, Klaus Greff, Jürgen Schmidhuber
- Paper Link: [arXiv](https://arxiv.org/abs/1505.00387)
- Paper Download: [arXiv](https://arxiv.org/pdf/1505.00387.pdf)

```
@article{srivastava2015highway,
  title={Highway networks},
  author={Srivastava, Rupesh Kumar and Greff, Klaus and Schmidhuber, J{\"u}rgen},
  journal={arXiv preprint arXiv:1505.00387},
  year={2015}
}
```


## 5. 预训练模型

### 5.1. CoVe

***CoVe***: Contextualized Vector

**paper**: Learned in Translation: Contextualized Word Vectors

- Author: Bryan McCann, James Bradbury, Caiming Xiong, Richard Socher
- Paper Link: [NIPS 2017](http://papers.nips.cc/paper/7209-learned-in-translation-contextualized-word-vectors)
- Paper Download: [NIPS 2017](https://papers.nips.cc/paper/7209-learned-in-translation-contextualized-word-vectors.pdf)
- Open Source Code: [GitHub](https://github.com/salesforce/cove)

```
@inproceedings{mccann2017learned,
  title={Learned in translation: Contextualized word vectors},
  author={McCann, Bryan and Bradbury, James and Xiong, Caiming and Socher, Richard},
  booktitle={Advances in Neural Information Processing Systems},
  pages={6294--6305},
  year={2017}
}
```

### 5.2. ELMo

***ELMo***

**paper**: Deep contextualized word representations

- Author: Matthew E. Peters, Mark Neumann, Mohit Iyyer, Matt Gardner, Christopher Clark, Kenton Lee, Luke Zettlemoyer
- Paper Link: [arXiv](https://arxiv.org/abs/1802.05365)
- Paper Download: [arXiv](https://arxiv.org/pdf/1802.05365.pdf)
- Open Source Code: [GitHub](https://github.com/allenai/allennlp)

```
@article{peters2018deep,
  title={Deep contextualized word representations},
  author={Peters, Matthew E and Neumann, Mark and Iyyer, Mohit and Gardner, Matt and Clark, Christopher and Lee, Kenton and Zettlemoyer, Luke},
  journal={arXiv preprint arXiv:1802.05365},
  year={2018}
}
```

### 5.3. Transformer

***Transformer***

**paper**: Attention is All you Need

- Author: Ashish Vaswani, Noam Shazeer, Niki Parmar, Jakob Uszkoreit, Llion Jones, Aidan N. Gomez, Łukasz Kaiser, Illia Polosukhin
- Paper Link: [NIPS 2017](http://papers.nips.cc/paper/7181-attention-is-all-you-need)
- Paper Download: [NIPS 2017](https://papers.nips.cc/paper/7181-attention-is-all-you-need.pdf)
- Transformer-based Models in Pytorch and TensorFlow 2.0: [GitHub](https://github.com/huggingface/transformers)

```
@inproceedings{vaswani2017attention,
  title={Attention is all you need},
  author={Vaswani, Ashish and Shazeer, Noam and Parmar, Niki and Uszkoreit, Jakob and Jones, Llion and Gomez, Aidan N and Kaiser, {\L}ukasz and Polosukhin, Illia},
  booktitle={Advances in neural information processing systems},
  pages={5998--6008},
  year={2017}
}
```

### 5.4. GPT

***GPT***: Generative Pre-Training

**paper**: Improving Language Understanding by Generative Pre-Training

- Author: Alec Radford, Karthik Narasimhan, Tim Salimans, Ilya Sutskever
- Paper Download: [arXiv](https://www.cs.ubc.ca/~amuham01/LING530/papers/radford2018improving.pdf)
- Open Source Code: [GitHub gpt-2](https://github.com/openai/gpt-2)
- OpenAI Hempage: [Homepage](https://openai.com/)
- OpenAI GitHub: [Git Homepage](https://github.com/openai)

```
@misc{radford2018improving,
  title={Improving language understanding by generative pre-training},
  author={Radford, Alec and Narasimhan, Karthik and Salimans, Tim and Sutskever, Ilya},
  year={2018}
}
```

### 5.5. BERT

***BERT***

**paper**: BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding

- Author: Jacob Devlin, Ming-Wei Chang, Kenton Lee, Kristina Toutanova
- Paper Link: [arXiv](https://arxiv.org/abs/1810.04805)
- Paper Download: [arXiv](https://arxiv.org/pdf/1810.04805.pdf)
- Open Source Code: [GitHub](https://github.com/google-research/bert)
- Google Research GitHub: [Git Homepage](https://github.com/google-research)
- Google Research Repo: [Git Repo](https://github.com/google-research/google-research)

```
@article{devlin2018bert,
  title={Bert: Pre-training of deep bidirectional transformers for language understanding},
  author={Devlin, Jacob and Chang, Ming-Wei and Lee, Kenton and Toutanova, Kristina},
  journal={arXiv preprint arXiv:1810.04805},
  year={2018}
}
```

### 5.6. XLNet

***XLNet***

**paper**: XLNet: Generalized Autoregressive Pretraining for Language Understanding

- Author: Zhilin Yang, Zihang Dai, Yiming Yang, Jaime Carbonell, Ruslan Salakhutdinov, Quoc V. Le
- Paper Link: [arXiv](https://arxiv.org/abs/1906.08237)  [NIPS 2019](http://papers.nips.cc/paper/8812-xlnet-generalized-autoregressive-pretraining-for-language-understanding)
- Paper Download: [arXiv](https://arxiv.org/pdf/1906.08237.pdf)  [NIPS 2019](https://papers.nips.cc/paper/8812-xlnet-generalized-autoregressive-pretraining-for-language-understanding.pdf)

```
@inproceedings{yang2019xlnet,
  title={Xlnet: Generalized autoregressive pretraining for language understanding},
  author={Yang, Zhilin and Dai, Zihang and Yang, Yiming and Carbonell, Jaime and Salakhutdinov, Russ R and Le, Quoc V},
  booktitle={Advances in neural information processing systems},
  pages={5753--5763},
  year={2019}
}
```

## 6. MRC 模型

### 6.1. BiDAF

**paper**: Bidirectional Attention Flow for Machine Comprehension

- Author: Minjoon Seo, Aniruddha Kembhavi, Ali Farhadi, Hannaneh Hajishirzi
- Paper Link: [arXiv](https://arxiv.org/abs/1611.01603)
- Paper Download: [arXiv](https://arxiv.org/pdf/1611.01603.pdf)

```
@article{seo2016bidirectional,
  title={Bidirectional attention flow for machine comprehension},
  author={Seo, Minjoon and Kembhavi, Aniruddha and Farhadi, Ali and Hajishirzi, Hannaneh},
  journal={arXiv preprint arXiv:1611.01603},
  year={2016}
}
```

### 6.2. R-net

**paper**: Gated Self-Matching Networks for Reading Comprehension and Question Answering

- Author: Wenhui Wang, Nan Yang, Furu Wei, Baobao Chang, Ming Zhou
- Paper Download: [ACL 2017](https://www.aclweb.org/anthology/P17-1018.pdf)

```
@inproceedings{wang2017gated,
  title={Gated self-matching networks for reading comprehension and question answering},
  author={Wang, Wenhui and Yang, Nan and Wei, Furu and Chang, Baobao and Zhou, Ming},
  booktitle={Proceedings of the 55th Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers)},
  pages={189--198},
  year={2017}
}
```

### 6.3. FusionNet

**paper**: FusionNet: Fusing via Fully-Aware Attention with Application to Machine Comprehension

- Author: Hsin-Yuan Huang, Chenguang Zhu, Yelong Shen, Weizhu Chen
- Paper Link: [arXiv](https://arxiv.org/abs/1711.07341)
- Paper Download: [arXiv](https://arxiv.org/pdf/1711.07341.pdf)

```
@article{huang2017fusionnet,
  title={Fusionnet: Fusing via fully-aware attention with application to machine comprehension},
  author={Huang, Hsin-Yuan and Zhu, Chenguang and Shen, Yelong and Chen, Weizhu},
  journal={arXiv preprint arXiv:1711.07341},
  year={2017}
}
```

### 6.4. ET-RR

**paper**: Learning to Attend On Essential Terms: An Enhanced Retriever-Reader Model for Open-domain Question Answering

- Author: Jianmo Ni, Chenguang Zhu, Weizhu Chen, Julian McAuley
- Paper Link: [arXiv](https://arxiv.org/abs/1808.09492)
- Paper Download: [arXiv](https://arxiv.org/pdf/1808.09492.pdf)

```
@article{ni2018learning,
  title={Learning to attend on essential terms: An enhanced retriever-reader model for open-domain question answering},
  author={Ni, Jianmo and Zhu, Chenguang and Chen, Weizhu and McAuley, Julian},
  journal={arXiv preprint arXiv:1808.09492},
  year={2018}
}
```

### 6.5. SDNet

**paper**: SDNet: Contextualized Attention-based Deep Network for Conversational Question Answering

- Author: Chenguang Zhu, Michael Zeng, Xuedong Huang
- Paper Link: [arXiv](https://arxiv.org/abs/1812.03593)
- Paper Download: [arXiv](https://arxiv.org/pdf/1812.03593.pdf)
- Open Source Code: [GitHub](https://github.com/microsoft/SDNet)
- Microsoft Research GitHub: [Git Homepage](https://github.com/microsoft)

```
@article{zhu2018sdnet,
  title={Sdnet: Contextualized attention-based deep network for conversational question answering},
  author={Zhu, Chenguang and Zeng, Michael and Huang, Xuedong},
  journal={arXiv preprint arXiv:1812.03593},
  year={2018}
}
```
