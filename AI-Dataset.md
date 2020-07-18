# AI Tasks & Datasets

By [YuweiYin](https://yuweiyin.github.io/)

# 自然语言处理 NLP - Natural Language Processing

## GLUE - General Language Understanding Evaluation

DataSet | Full Name | Task | In Chinese
:-: | :-: | :-: | :-:
CoLA | Corpus of Linguistic Acceptability |  | 句子语言性判断
SST-2 | Stanford Sentiment Treebank | Sentiment analysis | 情感分析
MRPC | Microsoft Research Paraphrase Corpus | Semantic textual similarity | 语义相似
STS-B | Semantic Textual Similarity | Semantic textual similarity | 语义相似
QQP | Quora Question Pairs | Semantic textual similarity/Paraphrase identification | 语义文本相似性/问题对是否等价/释义识别
RTE | Recognizing Texual Entailment | Natural language inference | 自然语言推断  文本蕴涵
MNLI | Multi-Genre NLI | Natural language inference | 自然语言推断  多类型 NLI
QNLI | Question NLI | Natural language inference | 自然语言推断  问答
WNLI | Winograd NLI | Natural language inference | 自然语言推断  文本蕴涵

- 相关链接：
	- [GLUE paper](https://arxiv.org/pdf/1804.07461.pdf)
	- [GLUE dataset](https://gluebenchmark.com/)
	- [GLUE Download Script](https://gist.github.com/W4ngatang/60c2bdb54d156a41194446737ce03e2e)
	- [SuperGLUE: A Stickier Benchmark for General-Purpose Language Understanding Systems](https://w4ngatang.github.io/static/papers/superglue.pdf)

## CoLA - The Corpus of Linguistic Acceptability

CoLA 是纽约大学发布的有关语法的数据集，该任务主要是对一个给定句子，判定其是否语法正确，因此 CoLA 属于单个句子的文本二分类任务。

- 原论文链接：
	- [CoLA paper](https://arxiv.org/pdf/1805.12471.pdf)
- 数据集首页：
	- [CoLA dataset](https://nyu-mll.github.io/CoLA/)
- 数据集下载：
	- [Download: cola_public 1.0](https://www.nyu.edu/projects/bowman/xnli/XNLI-1.0.zip) (260 KB, ZIP)
	- [Download: cola_public 1.1](https://s3.amazonaws.com/xnli/XNLI-MT-1.0.zip) (255 KB, ZIP)

## SST - Stanford Sentiment Treebank

SST 是斯坦福大学发布的一个情感分析数据集，主要针对电影评论来做情感分类，因此SST属于单个句子的文本分类任务。其中 SST-2 是二分类，SST-5 是五分类，SST-5 的情感极性区分的更细致。

- 原论文链接：
	- [SST paper](https://nlp.stanford.edu/~socherr/EMNLP2013_RNTN.pdf)
- 数据集首页：
	- [SST dataset](https://nlp.stanford.edu/sentiment/index.html)
- 数据集下载：
	- [Download: Main zip file with readme](http://nlp.stanford.edu/~socherr/stanfordSentimentTreebank.zip) (6.4 MB, ZIP)
	- [Download: Dataset raw counts](http://nlp.stanford.edu/~socherr/stanfordSentimentTreebankRaw.zip) (4.8 MB, ZIP)
	- [Download: Train, Dev, Test Splits in PTB Tree Format](https://nlp.stanford.edu/sentiment/trainDevTestTrees_PTB.zip) (790 KB, ZIP)

## MRPC - Microsoft Research Paraphrase Corpus

MRPC 由微软发布，判断两个给定句子是否具有相同的语义，属于句子对的文本二分类任务。MRPC 提供 5081 对英文句子，这些句子是从网络上的新闻源中提取的，还有人工注释，指示每对是否捕获了释义/语义等价关系。从任何给定的新闻文章中提取的句子不超过1个。我们已作出协调一致的努力，正确地将每个句子信息与其出处以及有关其作者的任何相关信息相关联。

- 原论文链接：
	- [MRPC paper](https://acl-arc.comp.nus.edu.sg/archives/acl-arc-090501d3/data/pdf/anthology-PDF/C/C04/C04-1051.pdf)
- 数据集下载：
	- [MRPC Download](https://www.microsoft.com/en-us/download/confirmation.aspx?id=52398)

## STS - Semantic Textual Similarity

使用语义文本相似性（STS）来衡量句子的意义相似性。

- 原论文链接：
	- [STS paper](https://arxiv.org/pdf/1708.00055.pdf)
- 数据集下载：
	- [STS Download](http://ixa2.si.ehu.es/stswiki/index.php/STSbenchmark)

## NLI - Natural Language Inference

- 原论文链接：
	- [XNLI paper](https://arxiv.org/pdf/1809.05053.pdf)
	- [MultiNLI paper](http://www.nyu.edu/projects/bowman/multinli/paper.pdf)
	- [SNLI paper](https://nlp.stanford.edu/pubs/snli_paper.pdf)
	- [e-SNLI paper](https://papers.nips.cc/paper/8163-e-snli-natural-language-inference-with-natural-language-explanations.pdf)
	- [MedNLI paper](https://arxiv.org/pdf/1808.06752.pdf)
- 数据集首页：
	- [XNLI dataset](https://www.nyu.edu/projects/bowman/xnli/)
	- [MultiNLI dataset](http://www.nyu.edu/projects/bowman/multinli/)
	- [SNLI dataset](https://nlp.stanford.edu/projects/snli/)
	- [MedNLI dataset](https://jgc128.github.io/mednli/)
- 数据集下载：
	- [Download: XNLI 1.0](https://www.nyu.edu/projects/bowman/xnli/XNLI-1.0.zip) (17 MB, ZIP)
	- [Download: XNLI-MT 1.0](https://s3.amazonaws.com/xnli/XNLI-MT-1.0.zip) (445 MB, ZIP)
	- [Download: MultiNLI 1.0](http://www.nyu.edu/projects/bowman/multinli/multinli_1.0.zip) (227 MB, ZIP)
	- [Download: SNLI 1.0](https://nlp.stanford.edu/projects/snli/snli_1.0.zip) (\~100 MB, ZIP)
	- [Download: MedNLI](http://doi.org/10.13026/C2RS98)
- 相关源码：
	- [e-SNLI code](https://github.com/OanaMariaCamburu/e-SNLI)
	- [MedNLI code](https://archive.physionet.org/physiotools/mimic-code/mednli/)
	- [MedNLI baseline](https://github.com/jgc128/mednli_baseline)

## SQuAD

SQuAD 是斯坦福大学于 2016 年推出的机器阅读理解（Machine Reading Comprehension, MRC）数据集。输入一篇文章以及相应一些问题，需要模型输出问题的答案。此数据集所有文章选自 Wikipedia 维基百科，数据集的量为当今其他数据集（例如 WikiQA）的几十倍之多。一共有 107,785 问题，以及配套的 536 篇文章。

- 原论文链接：
	- [SQuAD 1](https://arxiv.org/abs/1606.05250)
	- [SQuAD 2](https://arxiv.org/abs/1806.03822)
- 数据集链接：
	- https://rajpurkar.github.io/SQuAD-explorer/

## WikiText

WikiText 英语词库数据（The WikiText Long Term Dependency Language Modeling Dataset）是一个包含 一亿个词汇的英文词库数据，这些词汇是从 Wikipedia 的优质文章和标杆文章中提取得到，包括 WikiText-2 和 WikiText-103 两个版本，相比于著名的 Penn Treebank (PTB) 词库中的词汇数量，前者是其 2 倍，后者是其 110 倍。每个词汇还同时保留产生该词汇的原始文章，这尤其适合当需要长时依赖（longterm dependency）自然语言建模的场景。

- 相关链接：
	- http://metamind.io/research/the-wikitext-long-term-dependency-language-modeling-dataset/
	- https://s3.amazonaws.com/research.metamind.io/wikitext/wikitext-103-raw-v1.zip

## IMDB

- 原论文链接：
	- [Learning Word Vectors for Sentiment Analysis](http://ai.stanford.edu/~amaas/papers/wvSent_acl2011.pdf)
- 数据集首页：
	- [Large Movie Review Dataset](http://ai.stanford.edu/~amaas/data/sentiment/)
- 数据集下载：
	- [Download: Large Movie Review Dataset v1.0](http://ai.stanford.edu/~amaas/data/sentiment/)

## Sentiment140

- 原论文链接：
	- [Twitter Sentiment Classification using Distant Supervision](https://cs.stanford.edu/people/alecmgo/papers/TwitterDistantSupervision09.pdf)
- 数据集首页：
	- [Sentiment140](http://help.sentiment140.com/)
	- [Sentiment140 For Academics](http://help.sentiment140.com/for-students)
- 数据集下载：
	- [Stanford link](http://cs.stanford.edu/people/alecmgo/trainingandtestdata.zip)
	- [Google Drive link](https://docs.google.com/file/d/0B04GJPshIjmPRnZManQwWEdTZjg/edit)

## WordNet

- WordNet 链接：
	- [WordNet An Electronic Lexical Database](https://mitpress.mit.edu/books/wordnet)
- 数据集首页：
	- [WordNet](https://wordnet.princeton.edu/)
- 数据集下载：
	- [WordNet current version](https://wordnet.princeton.edu/download/current-version)
	- [WordNet old version](https://wordnet.princeton.edu/download/old-versions)

## The Wikipedia Corpus

- 数据集首页：
	- [The Wikipedia Corpus](https://www.english-corpora.org/wiki/)
- 数据集下载：
	- [Full-text corpus data](https://www.corpusdata.org/)

## The Blog Authorship Corpus

- 原论文链接：
	- [Effects of Age and Gender on Blogging](http://www.cs.biu.ac.il/~schlerj/schler_springsymp06.pdf)
- 数据集首页：
	- [The Blog Authorship Corpus](http://u.cs.biu.ac.il/~koppel/BlogCorpus.htm)
- 数据集下载：
	- [Download: The Blog Authorship Corpus](http://www.cs.biu.ac.il/~koppel/blogs/blogs.zip)

## WMT - Statistical Machine Translation

[Statistical Machine Translation](http://www.statmt.org/)

- 数据集首页：
	- [WMT 19](http://www.statmt.org/wmt19/)
	- [WMT 20](http://www.statmt.org/wmt20/)
	- [uropean Parliament Proceedings Parallel Corpus 1996-2011](http://statmt.org/europarl/)
- 数据集下载：
	- [Download WMT19](http://www.statmt.org/wmt19/translation-task.html#download)
	- [Download WMT20](http://www.statmt.org/wmt20/translation-task.html#download)

## UCI’s Spambase

来自 UCI 的经典垃圾电子邮件数据集。这是一个大型垃圾邮件数据集，用于垃圾邮件过滤。

链接：https://archive.ics.uci.edu/ml/datasets/Spambase

---

# 计算机视觉 CV - Computer Vision

## MNIST

MNIST 数据集来自美国国家标准与技术研究所，National Institute of Standards and Technology (NIST)。训练集 (training set) 由来自 250 个不同人手写的数字构成，其中 50% 是高中学生，50% 来自人口普查局 (the Census Bureau) 的工作人员。测试集(test set) 也是同样比例的手写数字数据。

- 相关链接：
	- http://pjreddie.com/projects/mnist-in-csv/
	- http://yann.lecun.com/exdb/mnist/

## Fashion-MNIST

Fashion-MNIST 包含 60,000个训练图像和 10,000 个测试图像，它是一个类似 MNIST 的时尚产品数据库。开发人员认为 MNIST 已被过度使用，因此他们将其作为该数据集的直接替代品。每张图片都以灰度显示，并与10个类别的标签相关联。

- 相关链接：
	- [fashion-mnist Github](https://github.com/zalandoresearch/fashion-mnist)

## CIFAR-10

CIFAR-10 数据集由 10 个类的 60000 张 32x32 彩色图像组成，每个类有 6000 张图像。其中含有 50000 张训练图像和 10000 张测试图像。数据集分为五个训练批次和一个测试批次，每个批次有 10000 张图像。测试批次包含来自每个类别的恰好 1000 个随机选择的图像。训练批次以随机顺序包含剩余图像，但一些训练批次可能包含来自一个类别的图像比另一个更多。总体来说，五个训练集之和包含来自每个类的 5000 张图像。

- 相关链接：https://www.cs.toronto.edu/~kriz/cifar.html

## ImageNet

图像处理界最有名的图像数据集之一，一般情况下只用子数据集（如 MiniImageNet）就可以。ImageNet 数据集是为了促进计算机图像识别技术的发展而设立的一个大型图像数据集。其图片数量最多，分辨率最高，含有的类别更多，有上千个图像类别。每年 ImageNet 的项目组织都会举办一场ImageNet大规模视觉识别竞赛，从而会诞生许多图像识别模型。

- 相关链接：http://image-net.org/

## Open Images Dataset V4

- 相关链接：https://github.com/openimages/dataset

## COCO - Common Objects in Context

- 数据集首页：
	- [Common Objects in Context](http://cocodataset.org/#home)
- 数据集下载：
	- [Download: Images & Annotations](http://cocodataset.org/#download)
- 相关源码：
	- [cocodataset](https://github.com/cocodataset)
	- [cocoapi](https://github.com/cocodataset/cocoapi)

## VQA - Visual QA

- 原论文链接：
	- [Making the V in VQA Matter: Elevating the Role of Image Understanding in Visual Question Answering](https://arxiv.org/pdf/1612.00837.pdf)
- 数据集首页：
	- [Visual QA](https://visualqa.org/)
- 数据集下载：
	- [Download: VQA v1](https://visualqa.org/vqa_v1_download.html)
	- [Download: VQA v2](https://visualqa.org/download.html)

## Visual Genome

非常详细的视觉知识库，并带有 100K 图像的深字幕。相较于 ImageNet 数据集，这个数据集每张图片所包含的信息更加丰富，将对象、属性之间的关系做注解，是这套数据集的核心。Visual Genome 数据集采用了微软 COCO 的图片库，用极丰富的细节对这十万张图片做了注解。

- 相关链接：http://visualgenome.org/

## SVHN - Street View House Numbers

- 原论文链接：
	- [Reading Digits in Natural Images with Unsupervised Feature Learning](http://ufldl.stanford.edu/housenumbers/nips2011_housenumbers.pdf)
- 数据集首页：
	- [The Street View House Numbers (SVHN) Dataset](http://ufldl.stanford.edu/housenumbers/)
- 数据集下载：
	- Format 1: Full Numbers
		- [Download: train.tar.gz](http://ufldl.stanford.edu/housenumbers/train.tar.gz)
		- [Download: test.tar.gz](http://ufldl.stanford.edu/housenumbers/test.tar.gz)
		- [Download: extra.tar.gz](http://ufldl.stanford.edu/housenumbers/extra.tar.gz)
	- Format 2: Cropped Digits
		- [Download: train_32x32.mat](http://ufldl.stanford.edu/housenumbers/train_32x32.mat)
		- [Download: test_32x32.mat](http://ufldl.stanford.edu/housenumbers/test_32x32.mat)
		- [Download: extra_32x32.mat](http://ufldl.stanford.edu/housenumbers/extra_32x32.mat)

---

# 语音 Speech

## LibriSpeech

该数据集是包含大约 1000 小时的英语语音的大型语料库。这些数据来自 LibriVox 项目的有声读物。它已被分割并正确对齐，如果你正在寻找一个起点，请查看已准备好的声学模型，这些模型在 kaldi-asr.org 和语言模型上进行了训练，适合评估。

- 原论文链接：
	- [LibriSpeech: an ASR corpus based on public domain audio books](http://www.danielpovey.com/files/2015_icassp_librispeech.pdf)
- 数据集首页：
	- [Open Speech and Language Resources](http://www.openslr.org/)
	- [LibriSpeech ASR corpus](http://www.openslr.org/12/)
- 数据集下载：
	- [dev-clean.tar.gz](http://www.openslr.org/resources/12/dev-clean.tar.gz) [337M]   (development set, "clean" speech )   Mirrors: [China](http://cn-mirror.openslr.org/resources/12/dev-clean.tar.gz)
	- [dev-other.tar.gz](http://www.openslr.org/resources/12/dev-other.tar.gz) [314M]   (development set, "other", more challenging, speech )   Mirrors: [China](http://cn-mirror.openslr.org/resources/12/dev-other.tar.gz)
	- [test-clean.tar.gz](http://www.openslr.org/resources/12/test-clean.tar.gz) [346M]   (test set, "clean" speech )   Mirrors: [China](http://cn-mirror.openslr.org/resources/12/test-clean.tar.gz)
	- [test-other.tar.gz](http://www.openslr.org/resources/12/test-other.tar.gz) [328M]   (test set, "other" speech )   Mirrors: [China](http://cn-mirror.openslr.org/resources/12/test-other.tar.gz)
	- [train-clean-100.tar.gz](http://www.openslr.org/resources/12/train-clean-100.tar.gz) [6.3G]   (training set of 100 hours "clean" speech )   Mirrors: [China](http://cn-mirror.openslr.org/resources/12/train-clean-100.tar.gz)
	- [train-clean-360.tar.gz](http://www.openslr.org/resources/12/train-clean-360.tar.gz) [23G]   (training set of 360 hours "clean" speech )   Mirrors: [China](http://cn-mirror.openslr.org/resources/12/train-clean-360.tar.gz)
	- [train-other-500.tar.gz](http://www.openslr.org/resources/12/train-other-500.tar.gz) [30G]   (training set of 500 hours "other" speech )   Mirrors: [China](http://cn-mirror.openslr.org/resources/12/train-other-500.tar.gz)
	- [intro-disclaimers.tar.gz](http://www.openslr.org/resources/12/intro-disclaimers.tar.gz) [695M]   (extracted LibriVox announcements for some of the speakers )   Mirrors: [China](http://cn-mirror.openslr.org/resources/12/intro-disclaimers.tar.gz)
	- [original-mp3.tar.gz](http://www.openslr.org/resources/12/original-mp3.tar.gz) [87G]   (LibriVox mp3 files, from which corpus' audio was extracted )   Mirrors: [China](http://cn-mirror.openslr.org/resources/12/original-mp3.tar.gz)
	- [original-books.tar.gz](http://www.openslr.org/resources/12/original-books.tar.gz) [297M]   (Project Gutenberg texts, against which the audio in the corpus was aligned )   Mirrors: [China](http://cn-mirror.openslr.org/resources/12/original-books.tar.gz)
	- [raw-metadata.tar.gz](http://www.openslr.org/resources/12/raw-metadata.tar.gz) [33M]   (Some extra meta-data produced during the creation of the corpus )   Mirrors: [China](http://cn-mirror.openslr.org/resources/12/raw-metadata.tar.gz)
	- [md5sum.txt](http://www.openslr.org/resources/12/md5sum.txt) [600 bytes]   (MD5 checksums for the archive files )   Mirrors: [China](http://cn-mirror.openslr.org/resources/12/md5sum.txt)

## VoxCeleb

- 原论文链接：
	- [VoxCeleb: a large-scale speaker identification dataset](https://www.robots.ox.ac.uk/~vgg/publications/2017/Nagrani17/nagrani17.pdf)
- 数据集首页：
	- [VoxCeleb](http://www.robots.ox.ac.uk/~vgg/data/voxceleb/)
- 数据集下载：
	- [VoxCeleb1](http://www.robots.ox.ac.uk/~vgg/data/voxceleb/vox1.html)
	- [VoxCeleb2](http://www.robots.ox.ac.uk/~vgg/data/voxceleb/vox2.html)

## VoxForge

带口音英语的清晰语音数据集。如果你需要有强大的不同口音、语调识别能力，会比较有用，可以提高系统的鲁棒性。

- 相关链接：http://www.voxforge.org/

## MSD - Million Song Dataset

- 原论文链接：
	- [The Million Song Dataset Challenge](https://www.deepdyve.com/lp/association-for-computing-machinery/the-million-song-dataset-challenge-C1ThXUlRZH)
- 数据集首页：
	- [Million Song Dataset](http://millionsongdataset.com/)
- 数据集下载：
	- [Download: MSD](http://millionsongdataset.com/pages/getting-dataset/)

- **TODO**
	- 数据集描述（数据量级、样例数据）
	- 相关经典、SOTA 模型，及其效果分数表格
