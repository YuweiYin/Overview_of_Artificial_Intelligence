# Dataset - DuReader

By [YuweiYin](https://github.com/YuweiYin)

---

***DuReader*** 多段落式数据集

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
