# Dataset - CNN/Daily Mail

By [YuweiYin](https://github.com/YuweiYin)

---

***CNN/Daily Mail*** 单段落式数据集

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
