# MT - WMT Winners

By [YuweiYin](https://github.com/YuweiYin)

---

- [WMT 2019](#wmt19)
- [WMT 2018](#wmt18)
- [WMT 2017](#wmt17)
- [WMT 2016](#wmt16)

---

[WMT](http://www.statmt.org/wmt19/) is the most important annual international competition on machine translation. We collect the [competition results](http://matrix.statmt.org) on the news translation task since WMT 2016 (the First Conference of Machine Translation) and summarize the techniques used in the systems with the top performance. Currently, we focus on four directions: ZH-EN, EN-ZH, DE-EN, and EN-DE. The summarized algorithms might be incomplete; your suggestions are welcome!

<h1 id="wmt19">WMT 2019</h1>

* The winner of [ZH-EN](http://matrix.statmt.org/matrix/systems_list/1901), [DE-EN](http://matrix.statmt.org/matrix/systems_list/1902) and [EN-DE](http://matrix.statmt.org/matrix/systems_list/1909): **Microsoft**
    * **System report**: Yingce Xia, Xu Tan, Fei Tian, Fei Gao, Di He, Weicong Chen, Yang Fan, Linyuan Gong, Yichong Leng, Renqian Luo, Yiren Wang, Lijun Wu, Jinhua Zhu, Tao Qin and Tie-Yan Liu. 2019. [Microsoft Research Asia’s Systems for WMT19](http://www.statmt.org/wmt19/pdf/WMT0048.pdf). In *Proceedings of the Fourth Conference on Machine Translation: Shared Task Papers*.
    * **News**: [Microsoft Research Asia (MSRA) leads in 2019 WMT international machine translation competition](https://news.microsoft.com/apac/2019/05/22/microsoft-research-asia-msra-leads-in-2019-wmt-international-machine-translation-competition/)
    * **Techniques**:
        * Yiren Wang, Yingce Xia, Tianyu He, Fei Tian, Tao Qin, ChengXiang Zhai, and Tie-Yan Liu. 2019. [Multi-Agent Dual Learning](https://openreview.net/pdf?id=HyGhN2A5tm). In *Proceedings of ICLR 2019*.
        * Kaitao Song, Xu Tan, Tao Qin, Jianfeng Lu, and Tie-Yan Liu. 2019. [MASS: Masked Sequence to Sequence Pre-training for Language Generation](https://arxiv.org/pdf/1905.02450). In *Proceedings of ICML 2019*.
        * Renqian Luo, Fei Tian, Tao Qin, Enhong Chen, and Tie-Yan Liu. 2018. [Neural Architecture Optimization](https://papers.nips.cc/paper/8007-neural-architecture-optimization.pdf). In *Proceedings of NeurIPS 2018*.
        * Jinhua Zhu, Fei Gao, Lijun Wu, Yingce Xia, Tao Qin, Wengang Zhou, Xueqi Cheng, Tie-Yan Liu. 2019. [Soft Contextual Data Augmentation for Neural Machine Translation](https://arxiv.org/pdf/1905.10523.pdf). In *Proceedings of ACL 2019*.

* The winner of [EN-ZH](http://matrix.statmt.org/matrix/systems_list/1908): **PATECH**
    * **System report**: Coming soon...
    * **Techniques**: Transformer + Back-Translation + Reranking + Ensemble

<h1 id="wmt18">WMT 2018</h1>

* The winner of [ZH-EN](http://matrix.statmt.org/matrix/systems_list/1892): **Tencent**
    * **System report**: Mingxuan Wang, Li Gong, Wenhuan Zhu, Jun Xie, and Chao Bian. 2018. [Tencent Neural Machine Translation Systems for WMT18](https://www.aclweb.org/anthology/W18-6429). In *Proceedings of the Third Conference on Machine Translation: Shared Task Papers*.
    * **Techniques**: RNMT + Transformer + BPE + Rerank ensemble outputs with 48 features (including t2t R2l, t2t L2R, rnn L2R, rnn R2L etc.) + Back Translation + Joint Train with English to Chinese systems + Fine-tuning with selected data + Knowledge distillation
    
* The winner of [EN-ZH](http://matrix.statmt.org/matrix/systems_list/1893): **GTCOM**
    * **System report**: Chao Bei, Hao Zong, Yiming Wang, Baoyong Fan, Shiqi Li, and Conghu Yuan. 2018. [An Empirical Study of Machine Translation for the Shared Task of WMT18](https://www.aclweb.org/anthology/W18-6404). In *Proceedings of the Third Conference on Machine Translation: Shared Task Papers*.
    * **Techniques**: Transformer + Back-Translation + Data Filtering by rules, language models and translation models + BPE + Greedy Ensemble Decoding + Fine-Tuning with newstest2017 back translation
    
* The winner of [DE-EN](http://matrix.statmt.org/matrix/systems_list/1880): **RWTH Aachen University**
    * **System report**: Julian Schamper, Jan Rosendahl, Parnia Bahar, Yunsu Kim, Arne Nix, and Hermann Ney. 2018. [The RWTH Aachen University Supervised Machine Translation Systems for WMT 2018](https://www.aclweb.org/anthology/W18-6426). In *Proceedings of the Third Conference on Machine Translation: Shared Task Papers*.
    * **Techniques**: Ensemble of 3-strongest Transformer models + Data Selection + BPE + Fine-Tuning + Important Hyperparameters (batch size and model dimension)
    
* The winner of [EN-DE](http://matrix.statmt.org/matrix/systems_list/1881): **Microsoft**
    * **System report**: Marcin Junczys-Dowmunt. 2018. [Microsoft’s Submission to the WMT2018 News Translation Task: How I Learned to Stop Worrying and Love the Data](https://www.aclweb.org/anthology/W18-6415). In *Proceedings of the Third Conference on Machine Translation: Shared Task Papers*.
    * **Techniques**: Marian + Transformer-big + BPE + Ensemble + Data Filtering + Domain-Weighted {ParaCrawl, original data} + Decoder-time ensemble with in-domain Transformer-style language model + Reranking with Right-to-left Transformer-big models

<h1 id="wmt17">WMT 2017</h1>

* The winner of [ZH-EN](http://matrix.statmt.org/matrix/systems_list/1878): **Sogou**
    * **System report**: Yuguang Wang, Shanbo Cheng, Liyang Jiang, Jiajun Yang, Wei Chen, Muze Li, Lin Shi, Yanfeng Wang, and Hongtao Yang. 2017. [Sogou Neural Machine Translation Systems for WMT17](https://www.aclweb.org/anthology/W17-4742). In *Proceedings of the Second Conference on Machine Translation: Shared Task Papers*.
    * **Techniques**: Encoder-Decoder with Attention + BPE + Reranking (R2L, T2S, N-gram language models) + Tagging Model + Name Entity Translation + Ensemble

* The winner of [EN-ZH](http://matrix.statmt.org/matrix/systems_list/1879), [DE-EN](http://matrix.statmt.org/matrix/systems_list/1868) and [EN-DE](http://matrix.statmt.org/matrix/systems_list/1869): **University of Edinburgh**  
    * **System report**: Rico Sennrich, Alexandra Birch, Anna Currey, Ulrich Germann, Barry Haddow, Kenneth Heafield, Antonio Valerio Miceli Barone, and Philip Williams. 2017. [The University of Edinburgh’s Neural MT Systems for WMT17](https://www.aclweb.org/anthology/W17-4739). In *Proceedings of the Second Conference on Machine Translation: Shared Task Papers*. 
    * **Techniques**: Encoder-Decoder with Attention + Deep Model + Layer Normalization + Weight Tying + Back-Translation + BPE + Reranking(L2R, R2L) + Ensemble

<h1 id="wmt16">WMT 2016</h1>

* The winner of [DE-EN](http://matrix.statmt.org/matrix/systems_list/1846): **University of Regensburg**
    * **System report**: Failed to find it
    * **Techniques**: Failed to find it
    
* The winner of [EN-DE](http://matrix.statmt.org/matrix/systems_list/1846): **University of Edinburgh**
    * **System report**: [Edinburgh Neural Machine Translation Systems for WMT 16](http://www.aclweb.org/anthology/W16-2323). In *Proceedings of the First Conference on Machine Translation: Shared Task Papers*.
    * **Techniques**: Encoder-Decoder with Attention + Back-Translation + BPE + Reranking(R2L) + Ensemble
