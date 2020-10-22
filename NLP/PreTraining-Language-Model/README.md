# PLM - PreTraining Language Model

By [YuweiYin](https://github.com/YuweiYin)

---

- PreTraining Language Model
	- [CoVe](./CoVe.md)
	- [ELMo](./ELMo.md)
	- [Transformer](./Transformer.md)
	- [GPT](./GPT.md)
	- [BERT](./BERT.md)
	- [Transformer-XL](./Transformer-XL.md)
	- [XLM](./XLM.md)
	- [ERNIE](./ERNIE.md)
	- [XLNet](./XLNet.md)
	- [RoBERTa](./RoBERTa.md)
	- [MMBET](./MMBET.md)
	- [CTRL](./CTRL.md)
	- [ALBERT](./ALBERT.md)
	- [DistilBERT](./DistilBERT.md)
	- [T5](./T5.md)
	- [BART](./BART.md)
	- [DialoGPT](./DialoGPT.md)
	- [XLM-RoBERTa](./XLM-RoBERTa.md)
	- [CamemBERT](./CamemBERT.md)
	- [FlauBERT](./FlauBERT.md)
	- [ELECTRA](./ELECTRA.md)

# 1. 语言模型

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

# 2. 预训练模型

## 2.1. CoVe

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

## 2.2. ELMo

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

## 2.3. Transformer

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

## 2.4. GPT

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

---

***GPT-2***

---

***GPT-3***

## 2.5. BERT

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

## 2.6. Transformer-XL

***Transformer-XL***

**paper**: Transformer-XL: Attentive Language Models Beyond a Fixed-Length Context

- Author: Zihang Dai, Zhilin Yang, Yiming Yang, Jaime Carbonell, Quoc V. Le, Ruslan Salakhutdinov
- Paper Link: [arXiv](https://arxiv.org/abs/1901.02860)
- Paper Download: [arXiv](https://arxiv.org/pdf/1901.02860)

```
@article{dai2019transformer,
  title={Transformer-xl: Attentive language models beyond a fixed-length context},
  author={Dai, Zihang and Yang, Zhilin and Yang, Yiming and Carbonell, Jaime and Le, Quoc V and Salakhutdinov, Ruslan},
  journal={arXiv preprint arXiv:1901.02860},
  year={2019}
}
```

## 2.7. XLM

***XLM***

**paper**: Cross-lingual Language Model Pretraining

- Author: Guillaume Lample, Alexis Conneau
- Paper Link: [arXiv](https://arxiv.org/abs/1901.07291)
- Paper Download: [arXiv](https://arxiv.org/pdf/1901.07291)

```
@article{lample2019cross,
  title={Cross-lingual language model pretraining},
  author={Lample, Guillaume and Conneau, Alexis},
  journal={arXiv preprint arXiv:1901.07291},
  year={2019}
}
```

## 2.8. ERNIE

***ERNIE***

**paper**: ERNIE: Enhanced Representation through Knowledge Integration

- Author: Yu Sun, Shuohuan Wang, Yukun Li, Shikun Feng, Xuyi Chen, Han Zhang, Xin Tian, Danxiang Zhu, Hao Tian, Hua Wu
- Paper Link: [arXiv](https://arxiv.org/abs/1904.09223)
- Paper Download: [arXiv](https://arxiv.org/pdf/1904.09223)

```
@article{sun2019ernie,
  title={Ernie: Enhanced representation through knowledge integration},
  author={Sun, Yu and Wang, Shuohuan and Li, Yukun and Feng, Shikun and Chen, Xuyi and Zhang, Han and Tian, Xin and Zhu, Danxiang and Tian, Hao and Wu, Hua},
  journal={arXiv preprint arXiv:1904.09223},
  year={2019}
}
```

## 2.9. XLNet

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

## 2.10. RoBERTa

***RoBERTa***

**paper**: RoBERTa: A Robustly Optimized BERT Pretraining Approach

- Author: Yinhan Liu, Myle Ott, Naman Goyal, Jingfei Du, Mandar Joshi, Danqi Chen, Omer Levy, Mike Lewis, Luke Zettlemoyer, Veselin Stoyanov
- Paper Link: [arXiv](https://arxiv.org/abs/1907.11692)
- Paper Download: [arXiv](https://arxiv.org/pdf/1907.11692)

```
@article{liu2019roberta,
  title={Roberta: A robustly optimized bert pretraining approach},
  author={Liu, Yinhan and Ott, Myle and Goyal, Naman and Du, Jingfei and Joshi, Mandar and Chen, Danqi and Levy, Omer and Lewis, Mike and Zettlemoyer, Luke and Stoyanov, Veselin},
  journal={arXiv preprint arXiv:1907.11692},
  year={2019}
}
```

## 2.11. MMBET

***MMBET***

**paper**: Supervised Multimodal Bitransformers for Classifying Images and Text

- Author: Douwe Kiela, Suvrat Bhooshan, Hamed Firooz, Davide Testuggine
- Paper Link: [arXiv](https://arxiv.org/abs/1909.02950)
- Paper Download: [arXiv](https://arxiv.org/pdf/1909.02950)

```
@article{kiela2019supervised,
  title={Supervised multimodal bitransformers for classifying images and text},
  author={Kiela, Douwe and Bhooshan, Suvrat and Firooz, Hamed and Testuggine, Davide},
  journal={arXiv preprint arXiv:1909.02950},
  year={2019}
}
```

## 2.12. CTRL

***CTRL***

**paper**: CTRL: A Conditional Transformer Language Model for Controllable Generation

- Author: Nitish Shirish Keskar, Bryan McCann, Lav R. Varshney, Caiming Xiong, Richard Socher
- Paper Link: [arXiv](https://arxiv.org/abs/1909.05858)
- Paper Download: [arXiv](https://arxiv.org/pdf/1909.05858)

```
@article{keskar2019ctrl,
  title={Ctrl: A conditional transformer language model for controllable generation},
  author={Keskar, Nitish Shirish and McCann, Bryan and Varshney, Lav R and Xiong, Caiming and Socher, Richard},
  journal={arXiv preprint arXiv:1909.05858},
  year={2019}
}
```

## 2.13. ALBERT

***ALBERT***

**paper**: ALBERT: A Lite BERT for Self-supervised Learning of Language Representations

- Author: Zhenzhong Lan, Mingda Chen, Sebastian Goodman, Kevin Gimpel, Piyush Sharma, Radu Soricut
- Paper Link: [arXiv](https://arxiv.org/abs/1909.11942)
- Paper Download: [arXiv](https://arxiv.org/pdf/1909.11942)

```
@article{lan2019albert,
  title={Albert: A lite bert for self-supervised learning of language representations},
  author={Lan, Zhenzhong and Chen, Mingda and Goodman, Sebastian and Gimpel, Kevin and Sharma, Piyush and Soricut, Radu},
  journal={arXiv preprint arXiv:1909.11942},
  year={2019}
}
```

## 2.14. DistilBERT

***DistilBERT***

**paper**: DistilBERT, a distilled version of BERT: smaller, faster, cheaper and lighter

- Author: Victor Sanh, Lysandre Debut, Julien Chaumond, Thomas Wolf
- Paper Link: [arXiv](https://arxiv.org/abs/1910.01108)
- Paper Download: [arXiv](https://arxiv.org/pdf/1910.01108.pdf)

```
@article{sanh2019distilbert,
  title={DistilBERT, a distilled version of BERT: smaller, faster, cheaper and lighter},
  author={Sanh, Victor and Debut, Lysandre and Chaumond, Julien and Wolf, Thomas},
  journal={arXiv preprint arXiv:1910.01108},
  year={2019}
}
```

## 2.15. T5

***T5***

**paper**: Exploring the Limits of Transfer Learning with a Unified Text-to-Text Transformer

- Author: Colin Raffel, Noam Shazeer, Adam Roberts, Katherine Lee, Sharan Narang, Michael Matena, Yanqi Zhou, Wei Li, Peter J. Liu
- Paper Link: [arXiv](https://arxiv.org/abs/1910.10683)
- Paper Download: [arXiv](https://arxiv.org/pdf/1910.10683)

```
@article{raffel2019exploring,
  title={Exploring the limits of transfer learning with a unified text-to-text transformer},
  author={Raffel, Colin and Shazeer, Noam and Roberts, Adam and Lee, Katherine and Narang, Sharan and Matena, Michael and Zhou, Yanqi and Li, Wei and Liu, Peter J},
  journal={arXiv preprint arXiv:1910.10683},
  year={2019}
}
```

## 2.16. BART

***BART***

**paper**: BART: Denoising Sequence-to-Sequence Pre-training for Natural Language Generation, Translation, and Comprehension

- Author: Mike Lewis, Yinhan Liu, Naman Goyal, Marjan Ghazvininejad, Abdelrahman Mohamed, Omer Levy, Ves Stoyanov, Luke Zettlemoyer
- Paper Link: [arXiv](https://arxiv.org/abs/1910.13461)
- Paper Download: [arXiv](https://arxiv.org/pdf/1910.13461)

```
@article{lewis2019bart,
  title={Bart: Denoising sequence-to-sequence pre-training for natural language generation, translation, and comprehension},
  author={Lewis, Mike and Liu, Yinhan and Goyal, Naman and Ghazvininejad, Marjan and Mohamed, Abdelrahman and Levy, Omer and Stoyanov, Ves and Zettlemoyer, Luke},
  journal={arXiv preprint arXiv:1910.13461},
  year={2019}
}
```

## 2.17. DialoGPT

***DialoGPT***

**paper**: DialoGPT: Large-Scale Generative Pre-training for Conversational Response Generation

- Author: Yizhe Zhang, Siqi Sun, Michel Galley, Yen-Chun Chen, Chris Brockett, Xiang Gao, Jianfeng Gao, Jingjing Liu, Bill Dolan
- Paper Link: [arXiv](https://arxiv.org/abs/1911.00536)
- Paper Download: [arXiv](https://arxiv.org/pdf/1911.00536)

```
@article{zhang2019dialogpt,
  title={Dialogpt: Large-scale generative pre-training for conversational response generation},
  author={Zhang, Yizhe and Sun, Siqi and Galley, Michel and Chen, Yen-Chun and Brockett, Chris and Gao, Xiang and Gao, Jianfeng and Liu, Jingjing and Dolan, Bill},
  journal={arXiv preprint arXiv:1911.00536},
  year={2019}
}
```

## 2.18. XLM-RoBERTa

***XLM-RoBERTa***

**paper**: Unsupervised Cross-lingual Representation Learning at Scale

- Author: Alexis Conneau, Kartikay Khandelwal, Naman Goyal, Vishrav Chaudhary, Guillaume Wenzek, Francisco Guzmán, Edouard Grave, Myle Ott, Luke Zettlemoyer, Veselin Stoyanov
- Paper Link: [arXiv](https://arxiv.org/abs/1911.02116)
- Paper Download: [arXiv](https://arxiv.org/pdf/1911.02116)

```
@article{conneau2019unsupervised,
  title={Unsupervised cross-lingual representation learning at scale},
  author={Conneau, Alexis and Khandelwal, Kartikay and Goyal, Naman and Chaudhary, Vishrav and Wenzek, Guillaume and Guzm{\'a}n, Francisco and Grave, Edouard and Ott, Myle and Zettlemoyer, Luke and Stoyanov, Veselin},
  journal={arXiv preprint arXiv:1911.02116},
  year={2019}
}
```

## 2.19. CamemBERT

***CamemBERT***

**paper**: CamemBERT: a Tasty French Language Model

- Author: Louis Martin, Benjamin Muller, Pedro Javier Ortiz Suárez, Yoann Dupont, Laurent Romary, Éric Villemonte de la Clergerie, Djamé Seddah, Benoît Sagot
- Paper Link: [arXiv](https://arxiv.org/abs/1911.03894)
- Paper Download: [arXiv](https://arxiv.org/pdf/1911.03894)

```
@article{martin2019camembert,
  title={Camembert: a tasty french language model},
  author={Martin, Louis and Muller, Benjamin and Su{\'a}rez, Pedro Javier Ortiz and Dupont, Yoann and Romary, Laurent and de la Clergerie, {\'E}ric Villemonte and Seddah, Djam{\'e} and Sagot, Beno{\^\i}t},
  journal={arXiv preprint arXiv:1911.03894},
  year={2019}
}
```

## 2.20. FlauBERT

***FlauBERT***

**paper**: FlauBERT: Unsupervised Language Model Pre-training for French

- Author: Hang Le, Loïc Vial, Jibril Frej, Vincent Segonne, Maximin Coavoux, Benjamin Lecouteux, Alexandre Allauzen, Benoît Crabbé, Laurent Besacier, Didier Schwab
- Paper Link: [arXiv](https://arxiv.org/abs/1912.05372)
- Paper Download: [arXiv](https://arxiv.org/pdf/1912.05372)

```
@article{le2019flaubert,
  title={Flaubert: Unsupervised language model pre-training for french},
  author={Le, Hang and Vial, Lo{\"\i}c and Frej, Jibril and Segonne, Vincent and Coavoux, Maximin and Lecouteux, Benjamin and Allauzen, Alexandre and Crabb{\'e}, Beno{\^\i}t and Besacier, Laurent and Schwab, Didier},
  journal={arXiv preprint arXiv:1912.05372},
  year={2019}
}
```

## 2.21. ELECTRA

***ELECTRA***

**paper**: ELECTRA: Pre-training Text Encoders as Discriminators Rather Than Generators

- Author: Kevin Clark, Minh-Thang Luong, Quoc V. Le, Christopher D. Manning
- Paper Link: [arXiv](https://arxiv.org/abs/2003.10555)
- Paper Download: [arXiv](https://arxiv.org/pdf/2003.10555)

```
@article{clark2020electra,
  title={Electra: Pre-training text encoders as discriminators rather than generators},
  author={Clark, Kevin and Luong, Minh-Thang and Le, Quoc V and Manning, Christopher D},
  journal={arXiv preprint arXiv:2003.10555},
  year={2020}
}
```
