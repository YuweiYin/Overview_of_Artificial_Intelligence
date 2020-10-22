# Dataset - QAngaroo

By [YuweiYin](https://github.com/YuweiYin)

---

***QAngaroo*** 多段落式数据集

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
