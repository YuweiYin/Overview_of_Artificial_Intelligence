# Embedding

Overview of Artificial Intelligence - [YuweiYin](https://github.com/YuweiYin)

---

## 1. Embedding Introduction

### Video

- [Hung-yi Lee - ML2017 Youtube](https://www.youtube.com/watch?v=X7PH3NuYW0Q)
- [Hung-yi Lee - ML2017 BiliBili](https://www.bilibili.com/video/av10590361/?p=25)

### Paper

- 1986 - G. Hinton - [Learning distributed representations of concepts](https://www.cs.toronto.edu/~hinton/absps/ieee-lre.pdf)
- 2000 - Wei Xu - [Can Artificial Neural Networks Learn Language Models?](http://www.speech.cs.cmu.edu/Communicator/papers/01291.pdf)
- 2003 - Y. Bengio - [A Neural Probabilistic Language Model](http://www.jmlr.org/papers/volume3/bengio03a/bengio03a.pdf)
- 2007 - A. Mnih, G. Hinton - [Three New Graphical Models for Statistical Language Modelling](https://www.cs.toronto.edu/~amnih/papers/threenew.pdf)
- 2008 - A. Mnih, G. Hinton - [A Scalable Hierarchical Distributed Language Model](https://www.cs.toronto.edu/~amnih/papers/hlbl_final.pdf)
- 2008 - C&W - [Natural Language Processing (Almost) from Scratch](http://www.jmlr.org/papers/volume12/collobert11a/collobert11a.pdf)
- 2010 - [Word representations: a simple and general method for semi-supervised learning](http://www.iro.umontreal.ca/~lisa/pointeurs/turian-wordrepresentations-acl10.pdf)
- 2010 - T. Mikolov - [Recurrent neural network based language model](https://www.fit.vutbr.cz/research/groups/speech/publi/2010/mikolov_interspeech2010_IS100722.pdf)
- 2012 - T. Mikolov - [Statistical Language Models based on Neural Networks](https://www.fit.vutbr.cz/~imikolov/rnnlm/thesis.pdf)
- 2012 - Huang - [Improving Word Representations via Global Context and Multiple Word Prototypes](https://nlp.stanford.edu/pubs/HuangACL12.pdf)
- 2013 - T. Mikolov - [Linguistic Regularities in Continuous Space Word Representations](https://www.aclweb.org/anthology/N13-1090.pdf)
- 2015 - [How to Generate a Good Word Embedding?](https://arxiv.org/pdf/1507.05523.pdf)
- 2016 - *Chinese* [Word and Document Embeddings based on Neural Network Approaches](https://arxiv.org/abs/1611.05962)

---

## 2.Word2Vec (Word to Vector)

- [Word2Vec WebPage/Code](https://code.google.com/archive/p/word2vec/)
- [Word2Vec Paper](https://arxiv.org/abs/1301.3781)

### Paper

- 2003 - [A Neural Probabilistic Language Model](http://www.jmlr.org/papers/v3/bengio03a)
- 2013 - (Word2Vec) [Efficient Estimation of Word Representations in Vector Space](https://arxiv.org/abs/1301.3781)
- 2013 - [Distributed Representations of Words and Phrases and their Compositionality](https://arxiv.org/abs/1310.4546)

---

## 3.GloVe (Global Vectors)

- [GloVe WebPage](https://nlp.stanford.edu/projects/glove/)
- [GloVe Paper](https://nlp.stanford.edu/pubs/glove.pdf)
- [GloVe Code](https://github.com/stanfordnlp/GloVe)

---

## 4.Doc2Vec (Document to Vector)

### Paper

- Doc2Vec (Beyond Bag of Words)
	- ICML2014 - [Distributed Representations of Sentences and Documents](https://arxiv.org/abs/1405.4053)
	- 2015 - [A Hierarchical Neural Autoencoder for Paragraphs and Documents](https://arxiv.org/abs/1506.01057.pdf)
	- 2015 - [Skip-Thought Vectors](https://arxiv.org/abs/1506.06726)
- Exploiting other kind of labels
	- 2013 - [Learning Deep Structured Semantic Models for Web Search using Clickthrough Data](https://posenhuang.github.io/papers/cikm2013_DSSM_fullversion.pdf)
	- 2014 - [A Latent Semantic Model with Convolutional-Pooling Structure for Information Retrieval](http://www.iro.umontreal.ca/~lisa/pointeurs/ir0895-he-2.pdf)
	- 2015 - [Improved Semantic Representations From Tree-Structured Long Short-Term Memory Networks](https://arxiv.org/abs/1503.00075)

---

## 5.Neighbor Embedding

### Manifold Learning

- 嵌入在高维欧式空间中的低维超曲面(流形 Manifold)，如果用高维欧式的坐标来表达流形上的点，然后用高维空间的欧式距离来度量这些点上的相似度，其实是不一定有道理的，尤其是当做比对的点距离比较大的时候。
- 比如：嵌入在三维空间的一个被弯曲折叠的二维曲面，因折叠而贴近的两点，并不一定在曲面上的距离很近。
- 形式化地说：要比较点A与点B、点C的谁更相近，在高维空间计算欧式距离发现|AB|>|AC|，却不代表在流形上A一定与B更近、与C更远。
- 如果把这个高维空间投影到一个低维空间，使得原来的超曲面得以“摊平”，这样在低维空间上的距离度量就更能准确地表达超曲面上的点之间距离了。而这种投影的理念，**在 Embedding 中就能体现！**

### Local Linear Embedding (LLE)

- 通过约束使得原高维空间中相似/相近的点，在降维变换后的低维空间中仍然相似/相近。
- JMLR2013 - [Think Globally, Fit Locally: Unsupervised Learning of Low Dimensional Manifolds](http://www.jmlr.org/papers/volume4/saul03a/saul03a.pdf)

### Laplacian Eigenmaps

- 可以用于度量流形上面样本点的光滑度。
- [Laplacian Eigenmaps and Spectral Techniques for Embedding and Clustering](http://web.cse.ohio-state.edu/~belkin.8/papers/LEM_NIPS_01.pdf)
- [Laplacian Eigenmaps for Dimensionality Reduction and Data Representation](http://www2.imm.dtu.dk/projects/manifold/Papers/Laplacian.pdf)
- ICML2008 - [Deep Learning via Semi-Supervised Embedding](http://www.thespermwhale.com/jaseweston/papers/deep_embed.pdf)
- ICLR2017 - [Semi-supervised deep learning by metric embedding](https://arxiv.org/abs/1611.01449.pdf)

### t-SNE (T-distributed Stochastic Neighbor Embedding)

- 简要介绍
	- 前面的做法，但没有约束使得那些在原高维空间中不相似/不相近的点，在降维变换后的低维空间中仍然不相似/不相近。
	- 这就可能会导致不同类别的样本点也相互靠近、耦合堆叠，不利于分类、聚类。而 t-SNE 能够处理这个问题。
	- Trick：一般不会直接在原高维空间做 t-SNE，因为在高维空间计算相似度 $S(x_i, x_j)$ 的计算量很大，所以通常会用比较快的方法(比如PCA)先降到一个较低的维度，然后再用 t-SNE 从这个较低的维度开始继续降维。
	- 由于 t-SNE 只能对一次性对所有输入的样本点进行降维转换，因此如果后来又出现一个新的样本点，是没法在原来的基础上将这个新样本点降维到同一个低维度的。
	- 如果要将这个新样本点降维，那就只能用之前的所有数据加上新数据一起拿出来 **从头重新**运行一遍 t-SNE 的。
	- 因此 t-SNE 不适合于训练集测试集分开的一般情况，它一般用来做数据可视化分析。
- 相似性度量 Similarity Measure
	- 记 $|x|$ 表示 x 的 2-范数(Euclid-Norm)，原高维空间计算相似度的函数为 $S(x_i, x_j) = exp(-| x_i - x_j|)$ 即高斯核/径向基函数，在低维空间 SNE 采用的还是高斯核 $S'(z_i, z_j) = exp(-|z_i - z_j|)$，而 t-SNE 则利用了 t 分布，其计算相似度的函数为 $S'(z_i, z_j) = 1 / (1 + | z_i - z_j|)$
	- t-SNE 这样做的好处在于：（在图像上会看得更直观）
		1. 设原高维空间中两点 $x_i$ 和 $x_j$ 的 S 函数值 $S(x_i, x_j) = k$，那么为了保持 S' 函数值 $S'(z_i, z_j)$ 也等于 $k$，需要低维空间中的两点 $z_i$ 和 $z_j$ 的距离被拉大一些(相比于 $x_i$ 和 $x_j$ 的距离)。
		2. 根据 t-SNE 的低维空间相似性函数的特性：在原高维空间中距离较近的两点(S 函数值较大)，为了在低维空间中的S'函数值仍然保持同等水平，只需被拉开很少的量；而在原高维空间中距离较远的两点(S 函数值较小)的两点，为了在低维空间中的S'函数值仍然保持同等水平，需要被拉开很大的量，这会使得原本就相距较远的两点在低维空间中相距更远了。

---

## Other Idea

- 对 Embedding 的一些更多的理解：
	- 假设词典里有 10^6 个词(Token)，先用 one-hot 编码(或者也可以根据词频采用 Huffman 编码、或者直接实数ID编码、或者二进制数编码等等)，如果使用 one-hot 编码，则会得到一个 10^6 x 10^6 的方阵，十分巨大。而 Embedding 类似于做了一个矩阵分解 Matrix Decomposition / 低秩逼近 Low-Rank Approximation，$[10^6 x 10^6] = [10^6 x 100] x [100 x 10^6]$，假设压缩为 100 维的 Embedding。
	- 而分解开来的两个矩阵分别对应了压缩和解压的功能。以线性变换的角度来看，压缩矩阵实际上是对原方阵的某些行/列的挑选、然后再叠加的操作，那么如果能**挑选出“最重要”的部分**，低秩逼近就会很成功，因此 Embedding 的表示效果也更佳。
	- 这种降维/压缩、挑选重要部分的做法，可以借鉴 PCA 主成分分析的思想。而矩阵分解的思想，可以参考 SVD 奇异值分解、LU 三角分解等。
	- 进一步谈谈 Embedding 的“压缩存储”能力，实际上压缩能力并不如想象中那么惊人。首先，为了避免损失太多信息，一般不会把维度压缩得太低。其次，压缩后每一维存储的是实数，一般需要双精度存储，而原本 one-hot 的每一维只需要一个 bit 位即可。最后，one-hot 编码的向量组成的矩阵是满秩、每一行/列仅有一个元素为 1、其余均为 0，这样的矩阵执行矩阵乘法和矩阵求逆是十分容易的，相较于稠密的实数矩阵而言。
	- 所以，从原文中**抽取重要信息、融合表示上下文信息**，才是词向量的核心意义所在，而非“压缩存储”功能，虽然深度神经网络很需要这个压缩工作，否则会出现“维数灾难”，但这也只是神经网络的众多毛病之一而已。
- Tomas Mikolov (Word2Vec 作者) 解释为何只使用浅层的神经网络(只有一层 hidden layer)，而不采用深层的网络：
	- 1. 在 Mikolov 之前已经有人做了很多 Word2Vec 的尝试，多数都是使用深度神经网络，但是效果一直没能做得很好，而且深层网络会带来大量的计算开销，以至于无法使用大量数据来训练。Mikolov 使用浅层的网络**减少了网络前馈和反馈的计算开销，增大训练数据的量**，使得最终效果很好。
	- 2. Mikolov 的 [Word2Vec 实现](https://code.google.com/archive/p/word2vec/) 中，有很多优化的 trick & skill，是一个**很成功的工程实现**，最终做出了实际可行、效果上佳的 Word2Vec 实现。

---
