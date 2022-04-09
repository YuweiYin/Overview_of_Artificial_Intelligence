# AI Tasks & Datasets

By [YuweiYin](https://github.com/YuweiYin)

---

<h2 id="yyw-directory">Directory</h2>

- Overview of Artificial Intelligence - AI Tasks & Datasets
  - <a href="#yyw-chapter-dataset-nlp">NLP - Natural Language Processing</a>
    - <a href="#yyw-chapter-dataset-nlp-glue">GLUE - General Language Understanding Evaluation</a>
    - <a href="#yyw-chapter-dataset-nlp-cola">CoLA - The Corpus of Linguistic Acceptability</a>
    - <a href="#yyw-chapter-dataset-nlp-sst">SST - Stanford Sentiment Treebank</a>
    - <a href="#yyw-chapter-dataset-nlp-mrpc">MRPC - Microsoft Research Paraphrase Corpus</a>
    - <a href="#yyw-chapter-dataset-nlp-sst">STS - Semantic Textual Similarity</a>
    - <a href="#yyw-chapter-dataset-nlp-nli">NLI - Natural Language Inference</a>
    - <a href="#yyw-chapter-dataset-nlp-squad">SQuAD - Stanford Question Answering Dataset</a>
    - <a href="#yyw-chapter-dataset-nlp-wikitext">WikiText</a>
    - <a href="#yyw-chapter-dataset-nlp-imdb">IMDb</a>
    - <a href="#yyw-chapter-dataset-nlp-sentiment140">Sentiment140</a>
    - <a href="#yyw-chapter-dataset-nlp-wordnet">WordNet</a>
    - <a href="#yyw-chapter-dataset-nlp-wikipedia">The Wikipedia Corpus</a>
    - <a href="#yyw-chapter-dataset-nlp-blog-authorship">The Blog Authorship Corpus</a>
    - <a href="#yyw-chapter-dataset-nlp-wmt">WMT - Statistical Machine Translation</a>
    - <a href="#yyw-chapter-dataset-nlp-uci-spambase">UCI's Spambase</a>
  - <a href="#yyw-chapter-dataset-cv">CV - Computer Vision</a>
    - <a href="#yyw-chapter-dataset-cv-mnist">MNIST - Modified National Institute of Standards and Technology</a>
    - <a href="#yyw-chapter-dataset-cv-mnist">Fashion-MNIST</a>
    - <a href="#yyw-chapter-dataset-cv-cifar">CIFAR-10 - Canadian Institute For Advanced Research</a>
    - <a href="#yyw-chapter-dataset-cv-imagenet">ImageNet</a>
    - <a href="#yyw-chapter-dataset-cv-open-images">Open Images Dataset V4</a>
    - <a href="#yyw-chapter-dataset-cv-coco">COCO - Common Objects in Context</a>
    - <a href="#yyw-chapter-dataset-cv-vqa">VQA - Visual QA</a>
    - <a href="#yyw-chapter-dataset-cv-visual-genome">Visual Genome</a>
    - <a href="#yyw-chapter-dataset-cv-svhn">SVHN - Street View House Numbers</a>
  - <a href="#yyw-chapter-dataset-speech">Audio & Speech</a>
    - <a href="#yyw-chapter-dataset-speech-librispeech">LibriSpeech</a>
    - <a href="#yyw-chapter-dataset-speech-voxceleb">VoxCeleb</a>
    - <a href="#yyw-chapter-dataset-speech-voxforge">VoxForge</a>
    - <a href="#yyw-chapter-dataset-speech-msd">MSD - Million Song Dataset</a>

---

<h2 id="yyw-chapter-dataset-nlp">NLP - Natural Language Processing</h2>

- <a href="#yyw-directory">Back to Directory</a>
- Sub Chapter
  - <a href="#yyw-chapter-dataset-nlp-glue">GLUE - General Language Understanding Evaluation</a>
  - <a href="#yyw-chapter-dataset-nlp-cola">CoLA - The Corpus of Linguistic Acceptability</a>
  - <a href="#yyw-chapter-dataset-nlp-sst">SST - Stanford Sentiment Treebank</a>
  - <a href="#yyw-chapter-dataset-nlp-mrpc">MRPC - Microsoft Research Paraphrase Corpus</a>
  - <a href="#yyw-chapter-dataset-nlp-sst">STS - Semantic Textual Similarity</a>
  - <a href="#yyw-chapter-dataset-nlp-nli">NLI - Natural Language Inference</a>
  - <a href="#yyw-chapter-dataset-nlp-squad">SQuAD - Stanford Question Answering Dataset</a>
  - <a href="#yyw-chapter-dataset-nlp-wikitext">WikiText</a>
  - <a href="#yyw-chapter-dataset-nlp-imdb">IMDb</a>
  - <a href="#yyw-chapter-dataset-nlp-sentiment140">Sentiment140</a>
  - <a href="#yyw-chapter-dataset-nlp-wordnet">WordNet</a>
  - <a href="#yyw-chapter-dataset-nlp-wikipedia">The Wikipedia Corpus</a>
  - <a href="#yyw-chapter-dataset-nlp-blog-authorship">The Blog Authorship Corpus</a>
  - <a href="#yyw-chapter-dataset-nlp-wmt">WMT - Statistical Machine Translation</a>
  - <a href="#yyw-chapter-dataset-nlp-uci-spambase">UCI's Spambase</a>

<h3 id="yyw-chapter-dataset-nlp-glue">GLUE - General Language Understanding Evaluation</h3>

- <a href="#yyw-directory">Back to Directory</a>
- <a href="#yyw-chapter-dataset-nlp">Back to Chapter Head</a>

DataSet | Full Name | Task
:-: | :-: | :-:
CoLA | Corpus of Linguistic Acceptability | 
SST-2 | Stanford Sentiment Treebank | Sentiment analysis
MRPC | Microsoft Research Paraphrase Corpus | Semantic textual similarity
STS-B | Semantic Textual Similarity | Semantic textual similarity
QQP | Quora Question Pairs | Semantic textual similarity/Paraphrase identification
RTE | Recognizing Texual Entailment | Natural language inference
MNLI | Multi-Genre NLI | Natural language inference
QNLI | Question NLI | Natural language inference
WNLI | Winograd NLI | Natural language inference

- Links:
  - [GLUE paper](https://arxiv.org/pdf/1804.07461.pdf)
  - [GLUE dataset](https://gluebenchmark.com/)
  - [GLUE Download Script](https://gist.github.com/W4ngatang/60c2bdb54d156a41194446737ce03e2e)
  - [SuperGLUE: A Stickier Benchmark for General-Purpose Language Understanding Systems](https://w4ngatang.github.io/static/papers/superglue.pdf)

<h3 id="yyw-chapter-dataset-nlp-cola">CoLA - The Corpus of Linguistic Acceptability</h3>

- <a href="#yyw-directory">Back to Directory</a>
- <a href="#yyw-chapter-dataset-nlp">Back to Chapter Head</a>

CoLA: Given a sentence, judge if its grammar is correct. (Yes or No)

- Paper Link:
  - [CoLA paper](https://arxiv.org/pdf/1805.12471.pdf)
- Dataset Homepage:
  - [CoLA dataset](https://nyu-mll.github.io/CoLA/)
- Dataset Download:
  - [Download: cola_public 1.0](https://www.nyu.edu/projects/bowman/xnli/XNLI-1.0.zip) (260 KB, ZIP)
  - [Download: cola_public 1.1](https://s3.amazonaws.com/xnli/XNLI-MT-1.0.zip) (255 KB, ZIP)

<h3 id="yyw-chapter-dataset-nlp-sst">SST - Stanford Sentiment Treebank</h3>

- <a href="#yyw-directory">Back to Directory</a>
- <a href="#yyw-chapter-dataset-nlp">Back to Chapter Head</a>

SST: Given a sentence, especially a movie comment, decide its sentiment category. (SST-2 has 2 categories, while SST-5 has 5 categories)

- Paper Link:
  - [SST paper](https://nlp.stanford.edu/~socherr/EMNLP2013_RNTN.pdf)
- Dataset Homepage:
  - [SST dataset](https://nlp.stanford.edu/sentiment/index.html)
- Dataset Download:
  - [Download: Main zip file with readme](http://nlp.stanford.edu/~socherr/stanfordSentimentTreebank.zip) (6.4 MB, ZIP)
  - [Download: Dataset raw counts](http://nlp.stanford.edu/~socherr/stanfordSentimentTreebankRaw.zip) (4.8 MB, ZIP)
  - [Download: Train, Dev, Test Splits in PTB Tree Format](https://nlp.stanford.edu/sentiment/trainDevTestTrees_PTB.zip) (790 KB, ZIP)

<h3 id="yyw-chapter-dataset-nlp-mrpc">MRPC - Microsoft Research Paraphrase Corpus</h3>

- <a href="#yyw-directory">Back to Directory</a>
- <a href="#yyw-chapter-dataset-nlp">Back to Chapter Head</a>

MRPC: Given two sentences, judge if they have the same meaning. (5000+ pairs)

- Paper Link:
  - [MRPC paper](https://acl-arc.comp.nus.edu.sg/archives/acl-arc-090501d3/data/pdf/anthology-PDF/C/C04/C04-1051.pdf)
- Dataset Download:
  - [MRPC Download](https://www.microsoft.com/en-us/download/confirmation.aspx?id=52398)

<h3 id="yyw-chapter-dataset-nlp-sst">STS - Semantic Textual Similarity</h3>

- <a href="#yyw-directory">Back to Directory</a>
- <a href="#yyw-chapter-dataset-nlp">Back to Chapter Head</a>

Evaluate the similarity between two sentences by Semantic Textual Similarity (STS).

- Paper Link:
  - [STS paper](https://arxiv.org/pdf/1708.00055.pdf)
- Dataset Download:
  - [STS Download](http://ixa2.si.ehu.es/stswiki/index.php/STSbenchmark)

<h3 id="yyw-chapter-dataset-nlp-nli">NLI - Natural Language Inference</h3>

- <a href="#yyw-directory">Back to Directory</a>
- <a href="#yyw-chapter-dataset-nlp">Back to Chapter Head</a>

- Paper Link:
  - [XNLI paper](https://arxiv.org/pdf/1809.05053.pdf)
  - [MultiNLI paper](http://www.nyu.edu/projects/bowman/multinli/paper.pdf)
  - [SNLI paper](https://nlp.stanford.edu/pubs/snli_paper.pdf)
  - [e-SNLI paper](https://papers.nips.cc/paper/8163-e-snli-natural-language-inference-with-natural-language-explanations.pdf)
  - [MedNLI paper](https://arxiv.org/pdf/1808.06752.pdf)
- Dataset Homepage:
  - [XNLI dataset](https://www.nyu.edu/projects/bowman/xnli/)
  - [MultiNLI dataset](http://www.nyu.edu/projects/bowman/multinli/)
  - [SNLI dataset](https://nlp.stanford.edu/projects/snli/)
  - [MedNLI dataset](https://jgc128.github.io/mednli/)
- Dataset Download:
  - [Download: XNLI 1.0](https://www.nyu.edu/projects/bowman/xnli/XNLI-1.0.zip) (17 MB, ZIP)
  - [Download: XNLI-MT 1.0](https://s3.amazonaws.com/xnli/XNLI-MT-1.0.zip) (445 MB, ZIP)
  - [Download: MultiNLI 1.0](http://www.nyu.edu/projects/bowman/multinli/multinli_1.0.zip) (227 MB, ZIP)
  - [Download: SNLI 1.0](https://nlp.stanford.edu/projects/snli/snli_1.0.zip) (\~100 MB, ZIP)
  - [Download: MedNLI](http://doi.org/10.13026/C2RS98)
- Source Code:
  - [e-SNLI code](https://github.com/OanaMariaCamburu/e-SNLI)
  - [MedNLI code](https://archive.physionet.org/physiotools/mimic-code/mednli/)
  - [MedNLI baseline](https://github.com/jgc128/mednli_baseline)

<h3 id="yyw-chapter-dataset-nlp-squad">SQuAD - Stanford Question Answering Dataset</h3>

- <a href="#yyw-directory">Back to Directory</a>
- <a href="#yyw-chapter-dataset-nlp">Back to Chapter Head</a>

SQuAD: Machine Reading Comprehension (MRC) dataset presented by Stanford University in 2016. Given a passage and several questions, the model needs to answer all the questions. (500+ passages and 100,000+ questions)

- Paper Link:
  - [SQuAD 1](https://arxiv.org/abs/1606.05250)
  - [SQuAD 2](https://arxiv.org/abs/1806.03822)
- Dataset Link:
  - https://rajpurkar.github.io/SQuAD-explorer/

<h3 id="yyw-chapter-dataset-nlp-wikitext">WikiText</h3>

- <a href="#yyw-directory">Back to Directory</a>
- <a href="#yyw-chapter-dataset-nlp">Back to Chapter Head</a>

WikiText: The WikiText Long Term Dependency Language Modeling Dataset. It contains 100 million English words. WikiText-2 is two times the size of Penn Treebank (PTB) and WikiText-103 is 110 times the size of PTB.

- Link:
  - http://metamind.io/research/the-wikitext-long-term-dependency-language-modeling-dataset/
  - https://s3.amazonaws.com/research.metamind.io/wikitext/wikitext-103-raw-v1.zip

<h3 id="yyw-chapter-dataset-nlp-imdb">IMDb</h3>

- <a href="#yyw-directory">Back to Directory</a>
- <a href="#yyw-chapter-dataset-nlp">Back to Chapter Head</a>

- Paper Link:
  - [Learning Word Vectors for Sentiment Analysis](http://ai.stanford.edu/~amaas/papers/wvSent_acl2011.pdf)
- Dataset Homepage:
  - [Large Movie Review Dataset](http://ai.stanford.edu/~amaas/data/sentiment/)
- Dataset Download:
  - [Download: Large Movie Review Dataset v1.0](http://ai.stanford.edu/~amaas/data/sentiment/)
  - IMDb [Link 1](https://www.imdb.com/interfaces/) or [Link 2](https://datasets.imdbws.com/)

<h3 id="yyw-chapter-dataset-nlp-sentiment140">Sentiment140</h3>

- <a href="#yyw-directory">Back to Directory</a>
- <a href="#yyw-chapter-dataset-nlp">Back to Chapter Head</a>

- Paper Link:
  - [Twitter Sentiment Classification using Distant Supervision](https://cs.stanford.edu/people/alecmgo/papers/TwitterDistantSupervision09.pdf)
- Dataset Homepage:
  - [Sentiment140](http://help.sentiment140.com/)
  - [Sentiment140 For Academics](http://help.sentiment140.com/for-students)
- Dataset Download:
  - [Stanford link](http://cs.stanford.edu/people/alecmgo/trainingandtestdata.zip)
  - [Google Drive link](https://docs.google.com/file/d/0B04GJPshIjmPRnZManQwWEdTZjg/edit)

<h3 id="yyw-chapter-dataset-nlp-wordnet">WordNet</h3>

- <a href="#yyw-directory">Back to Directory</a>
- <a href="#yyw-chapter-dataset-nlp">Back to Chapter Head</a>

- WordNet Link:
  - [WordNet An Electronic Lexical Database](https://mitpress.mit.edu/books/wordnet)
- Dataset Homepage:
  - [WordNet](https://wordnet.princeton.edu/)
- Dataset Download:
  - [WordNet current version](https://wordnet.princeton.edu/download/current-version)
  - [WordNet old version](https://wordnet.princeton.edu/download/old-versions)

<h3 id="yyw-chapter-dataset-nlp-wikipedia">The Wikipedia Corpus</h3>

- <a href="#yyw-directory">Back to Directory</a>
- <a href="#yyw-chapter-dataset-nlp">Back to Chapter Head</a>

- Dataset Homepage:
  - [The Wikipedia Corpus](https://www.english-corpora.org/wiki/)
- Dataset Download:
  - [Full-text corpus data](https://www.corpusdata.org/)

<h3 id="yyw-chapter-dataset-nlp-blog-authorship">The Blog Authorship Corpus</h3>

- <a href="#yyw-directory">Back to Directory</a>
- <a href="#yyw-chapter-dataset-nlp">Back to Chapter Head</a>

- Paper Link:
  - [Effects of Age and Gender on Blogging](http://www.cs.biu.ac.il/~schlerj/schler_springsymp06.pdf)
- Dataset Homepage:
  - [The Blog Authorship Corpus](http://u.cs.biu.ac.il/~koppel/BlogCorpus.htm)
- Dataset Download:
  - [Download: The Blog Authorship Corpus](http://www.cs.biu.ac.il/~koppel/blogs/blogs.zip)

<h3 id="yyw-chapter-dataset-nlp-wmt">WMT - Statistical Machine Translation</h3>

- <a href="#yyw-directory">Back to Directory</a>
- <a href="#yyw-chapter-dataset-nlp">Back to Chapter Head</a>

[Statistical Machine Translation](http://www.statmt.org/)

- Dataset Homepage:
  - [WMT 19](http://www.statmt.org/wmt19/)
  - [WMT 20](http://www.statmt.org/wmt20/)
  - [uropean Parliament Proceedings Parallel Corpus 1996-2011](http://statmt.org/europarl/)
- Dataset Download:
  - [Download WMT19](http://www.statmt.org/wmt19/translation-task.html#download)
  - [Download WMT20](http://www.statmt.org/wmt20/translation-task.html#download)

<h3 id="yyw-chapter-dataset-nlp-uci-spambase">UCI's Spambase</h3>

- <a href="#yyw-directory">Back to Directory</a>
- <a href="#yyw-chapter-dataset-nlp">Back to Chapter Head</a>

UCI: a large scale spam email dataset.

- Link: https://archive.ics.uci.edu/ml/datasets/Spambase

---

<h2 id="yyw-chapter-dataset-cv">CV - Computer Vision</h2>

- <a href="#yyw-directory">Back to Directory</a>
- Sub Chapter
  - <a href="#yyw-chapter-dataset-cv-mnist">MNIST - Modified National Institute of Standards and Technology</a>
  - <a href="#yyw-chapter-dataset-cv-mnist">Fashion-MNIST</a>
  - <a href="#yyw-chapter-dataset-cv-cifar">CIFAR-10 - Canadian Institute For Advanced Research</a>
  - <a href="#yyw-chapter-dataset-cv-imagenet">ImageNet</a>
  - <a href="#yyw-chapter-dataset-cv-open-images">Open Images Dataset V4</a>
  - <a href="#yyw-chapter-dataset-cv-coco">COCO - Common Objects in Context</a>
  - <a href="#yyw-chapter-dataset-cv-vqa">VQA - Visual QA</a>
  - <a href="#yyw-chapter-dataset-cv-visual-genome">Visual Genome</a>
  - <a href="#yyw-chapter-dataset-cv-svhn">SVHN - Street View House Numbers</a>

<h3 id="yyw-chapter-dataset-cv-mnist">MNIST - Modified National Institute of Standards and Technology</h3>

- <a href="#yyw-directory">Back to Directory</a>
- <a href="#yyw-chapter-dataset-cv">Back to Chapter Head</a>

MNIST: comes from National Institute of Standards and Technology (NIST). Its training set consists of handwriting digits by 250 different people, including 50% high school students and the staff of the Census Bureau. Its test set is also handwriting digits. (10 categories)

- Links:
  - http://pjreddie.com/projects/mnist-in-csv/
  - http://yann.lecun.com/exdb/mnist/

<h3 id="yyw-chapter-dataset-cv-fashion-mnist">Fashion-MNIST</h3>

- <a href="#yyw-directory">Back to Directory</a>
- <a href="#yyw-chapter-dataset-cv">Back to Chapter Head</a>

Fashion-MNIST: is similar to MNIST and includes 60,000 training images and 10,000 testing images (fashion product images; 10 categories)

- Links:
  - [fashion-mnist Github](https://github.com/zalandoresearch/fashion-mnist)

<h3 id="yyw-chapter-dataset-cv-cifar">CIFAR-10 - Canadian Institute For Advanced Research</h3>

- <a href="#yyw-directory">Back to Directory</a>
- <a href="#yyw-chapter-dataset-cv">Back to Chapter Head</a>

CIFAR-10: includes 60,000 32x32 color images, averagely divided into 10 categories (10 * 6,000). It has 50,000 training images and 10,000 test images.

- Link: https://www.cs.toronto.edu/~kriz/cifar.html

<h3 id="yyw-chapter-dataset-cv-imagenet">ImageNet</h3>

- <a href="#yyw-directory">Back to Directory</a>
- <a href="#yyw-chapter-dataset-cv">Back to Chapter Head</a>

ImageNet: a famous large-scale image dataset and computer vision competition. It has a subset MiniImageNet.

- Link: http://image-net.org/

<h3 id="yyw-chapter-dataset-cv-open-images">Open Images Dataset V4</h3>

- <a href="#yyw-directory">Back to Directory</a>
- <a href="#yyw-chapter-dataset-cv">Back to Chapter Head</a>

- Link: https://github.com/openimages/dataset

<h3 id="yyw-chapter-dataset-cv-coco">COCO - Common Objects in Context</h3>

- <a href="#yyw-directory">Back to Directory</a>
- <a href="#yyw-chapter-dataset-cv">Back to Chapter Head</a>

- Dataset Homepage:
  - [Common Objects in Context](http://cocodataset.org/#home)
- Dataset Download:
  - [Download: Images & Annotations](http://cocodataset.org/#download)
- Source Code:
  - [cocodataset](https://github.com/cocodataset)
  - [cocoapi](https://github.com/cocodataset/cocoapi)

<h3 id="yyw-chapter-dataset-cv-vqa">VQA - Visual QA</h3>

- <a href="#yyw-directory">Back to Directory</a>
- <a href="#yyw-chapter-dataset-cv">Back to Chapter Head</a>

- Paper Link:
  - [Making the V in VQA Matter: Elevating the Role of Image Understanding in Visual Question Answering](https://arxiv.org/pdf/1612.00837.pdf)
- Dataset Homepage:
  - [Visual QA](https://visualqa.org/)
- Dataset Download:
  - [Download: VQA v1](https://visualqa.org/vqa_v1_download.html)
  - [Download: VQA v2](https://visualqa.org/download.html)

<h3 id="yyw-chapter-dataset-cv-visual-genome">Visual Genome</h3>

- <a href="#yyw-directory">Back to Directory</a>
- <a href="#yyw-chapter-dataset-cv">Back to Chapter Head</a>

Visual Genome: an image dataset with 100,000 images. Its images contain more details compared to the images of ImageNet.

- Link: http://visualgenome.org/

<h3 id="yyw-chapter-dataset-cv-svhn">SVHN - Street View House Numbers</h3>

- <a href="#yyw-directory">Back to Directory</a>
- <a href="#yyw-chapter-dataset-cv">Back to Chapter Head</a>

- Paper Link:
  - [Reading Digits in Natural Images with Unsupervised Feature Learning](http://ufldl.stanford.edu/housenumbers/nips2011_housenumbers.pdf)
- Dataset Homepage:
  - [The Street View House Numbers (SVHN) Dataset](http://ufldl.stanford.edu/housenumbers/)
- Dataset Download:
  - Format 1: Full Numbers
    - [Download: train.tar.gz](http://ufldl.stanford.edu/housenumbers/train.tar.gz)
    - [Download: test.tar.gz](http://ufldl.stanford.edu/housenumbers/test.tar.gz)
    - [Download: extra.tar.gz](http://ufldl.stanford.edu/housenumbers/extra.tar.gz)
  - Format 2: Cropped Digits
    - [Download: train_32x32.mat](http://ufldl.stanford.edu/housenumbers/train_32x32.mat)
    - [Download: test_32x32.mat](http://ufldl.stanford.edu/housenumbers/test_32x32.mat)
    - [Download: extra_32x32.mat](http://ufldl.stanford.edu/housenumbers/extra_32x32.mat)

---

<h2 id="yyw-chapter-dataset-speech">Audio & Speech</h2>

- <a href="#yyw-directory">Back to Directory</a>
- Sub Chapter
  - <a href="#yyw-chapter-dataset-speech-librispeech">LibriSpeech</a>
  - <a href="#yyw-chapter-dataset-speech-voxceleb">VoxCeleb</a>
  - <a href="#yyw-chapter-dataset-speech-voxforge">VoxForge</a>
  - <a href="#yyw-chapter-dataset-speech-msd">MSD - Million Song Dataset</a>

<h3 id="yyw-chapter-dataset-speech-librispeech">LibriSpeech</h3>

- <a href="#yyw-directory">Back to Directory</a>
- <a href="#yyw-chapter-dataset-speech">Back to Chapter Head</a>

LibriSpeech: a large-scale speech dataset with 1,000 hours Englsih audio.

- Paper Link:
  - [LibriSpeech: an ASR corpus based on public domain audio books](http://www.danielpovey.com/files/2015_icassp_librispeech.pdf)
- Dataset Homepage:
  - [Open Speech and Language Resources](http://www.openslr.org/)
  - [LibriSpeech ASR corpus](http://www.openslr.org/12/)
- Dataset Download:
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

<h3 id="yyw-chapter-dataset-speech-voxceleb">VoxCeleb</h3>

- <a href="#yyw-directory">Back to Directory</a>
- <a href="#yyw-chapter-dataset-speech">Back to Chapter Head</a>

- Paper Link:
  - [VoxCeleb: a large-scale speaker identification dataset](https://www.robots.ox.ac.uk/~vgg/publications/2017/Nagrani17/nagrani17.pdf)
- Dataset Homepage:
  - [VoxCeleb](http://www.robots.ox.ac.uk/~vgg/data/voxceleb/)
- Dataset Download:
  - [VoxCeleb1](http://www.robots.ox.ac.uk/~vgg/data/voxceleb/vox1.html)
  - [VoxCeleb2](http://www.robots.ox.ac.uk/~vgg/data/voxceleb/vox2.html)

<h3 id="yyw-chapter-dataset-speech-voxforge">VoxForge</h3>

- <a href="#yyw-directory">Back to Directory</a>
- <a href="#yyw-chapter-dataset-speech">Back to Chapter Head</a>

VoxForge: a speech dataset. Its audio contains accents from different people.

- Link: http://www.voxforge.org/

<h3 id="yyw-chapter-dataset-speech-msd">MSD - Million Song Dataset</h3>

- <a href="#yyw-directory">Back to Directory</a>
- <a href="#yyw-chapter-dataset-speech">Back to Chapter Head</a>

- Paper Link:
  - [The Million Song Dataset Challenge](https://www.deepdyve.com/lp/association-for-computing-machinery/the-million-song-dataset-challenge-C1ThXUlRZH)
- Dataset Homepage:
  - [Million Song Dataset](http://millionsongdataset.com/)
- Dataset Download:
  - [Download: MSD](http://millionsongdataset.com/pages/getting-dataset/)

---

- **TODO**
  - More detailed dataset description. (e.g., the amount of data entries, sample data, etc.)
  - Related classical and the state-of-the-art models (with performance table).
