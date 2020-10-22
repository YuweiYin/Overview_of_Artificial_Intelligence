# MT - Statistical Machine Translation

By [YuweiYin](https://github.com/YuweiYin)

---

- [Tutorials](#smt_tutorials)
- [Word-based Models](#word_based_models)
- [Phrase-based Models](#phrase_based_models)
- [Syntax-based Models](#syntax_based_models)
- [Discriminative Training](#discriminative_training)
- [System Combination](#system_combination)
- [Human-centered SMT](#human_centered_smt)
    - [Interactive SMT](#interactive)
    - [Adaptation](#adaptation_smt)

<h1 id="smt_tutorials">Tutorials</h1>

* Philipp Koehn. 2006. [Statistical Machine Translation: the Basic, the Novel, and the Speculative](http://homepages.inf.ed.ac.uk/pkoehn/publications/tutorial2006.pdf). *EACL 2006 Tutorial*. ([Citation](https://scholar.google.com.hk/scholar?cites=226053141145183075&as_sdt=2005&sciodt=0,5&hl=en): 10)
* Adam Lopez. 2008. [Statistical Machine Translation](http://delivery.acm.org/10.1145/1390000/1380586/a8-lopez.pdf?ip=101.5.129.50&id=1380586&acc=ACTIVE%20SERVICE&key=BF85BBA5741FDC6E%2E587F3204F5B62A59%2E4D4702B0C3E38B35%2E4D4702B0C3E38B35&__acm__=1546058891_981e84a24804f2dbc0549b9892a2ea1d). *ACM Computing Surveys*. ([Citation](https://scholar.google.com.hk/scholar?cites=13327711981648149476&as_sdt=2005&sciodt=0,5&hl=en): 373)


<h1 id="word_based_models">Word-based Models</h1>

* Peter E. Brown, Stephen A. Della Pietra, Vincent J. Della Pietra, and Robert L. Mercer. 1993. [The Mathematics of Statistical Machine Translation: Parameter Estimation](http://aclweb.org/anthology/J93-2003). *Computational Linguistics*. ([Citation](https://scholar.google.com/scholar?cites=2259057253133260714&as_sdt=2005&sciodt=0,5&hl=en): 4,965)
* Stephan Vogel, Hermann Ney, and Christoph Tillmann. 1996. [HMM-Based Word Alignment in Statistical Translation](http://aclweb.org/anthology/C96-2141). In *Proceedings of COLING 1996*. ([Citation](https://scholar.google.com.hk/scholar?cites=6742027174667056165&as_sdt=2005&sciodt=0,5&hl=en): 940)
* Franz Josef Och and Hermann Ney. 2003. [A Systematic Comparison of Various Statistical Alignment Models](http://aclweb.org/anthology/J03-1002). *Computational Linguistics*. ([Citation](https://scholar.google.com.hk/scholar?cites=7906670690027479083&as_sdt=2005&sciodt=0,5&hl=en): 3,980)
* Percy Liang, Ben Taskar, and Dan Klein. 2006. [Alignment by Agreement](https://cs.stanford.edu/~pliang/papers/alignment-naacl2006.pdf). In *Proceedings of NAACL 2006*. ([Citation](https://scholar.google.com.hk/scholar?cites=10766838746666771394&as_sdt=2005&sciodt=0,5&hl=en): 452)
* Chris Dyer, Victor Chahuneau, and Noah A. Smith. 2013. [A Simple, Fast, and Effective Reparameterization of IBM Model 2](http://www.aclweb.org/anthology/N13-1073). In *Proceedings of NAACL 2013*. ([Citation](https://scholar.google.com.hk/scholar?cites=13560076980956479370&as_sdt=2005&sciodt=0,5&hl=en): 310)

<h1 id="phrase_based_models">Phrase-based Models</h1>

* Philipp Koehn, Franz J. Och, and Daniel Marcu. 2003. [Statistical Phrase-Based Translation](http://aclweb.org/anthology/N03-1017). In *Proceedings of NAACL 2003*. ([Citation](https://scholar.google.com.hk/scholar?cites=11796378766060939113&as_sdt=2005&sciodt=0,5&hl=en): 3,516)
* Michel Galley and Christopher D. Manning. 2008. [A Simple and Effective Hierarchical Phrase Reordering Model](https://nlp.stanford.edu/pubs/emnlp08-lexorder.pdf). In *Proceedings of EMNLP 2008*. ([Citation](https://scholar.google.com.hk/scholar?cites=14572547803642015856&as_sdt=2005&sciodt=0,5&hl=en): 275)

<h1 id="syntax_based_models">Syntax-based Models</h1>

* Dekai Wu. 1997. [Stochastic Inversion Transduction Grammars and Bilingual Parsing of Parallel Corpora](http://aclweb.org/anthology/J97-3002). *Computational Linguistics*. ([Citation](https://scholar.google.com.hk/scholar?cites=7926725626202301933&as_sdt=2005&sciodt=0,5&hl=en): 1,009)
* Michel Galley, Jonathan Graehl, Kevin Knight, Daniel Marcu, Steve DeNeefe, Wei Wang, and Ignacio Thayer. 2006. [Scalable Inference and Training of Context-Rich Syntactic Translation Models](http://aclweb.org/anthology/P06-1121). In *Proceedings of COLING/ACL 2006*. ([Citation](https://scholar.google.com.hk/scholar?cites=2650671041278094269&as_sdt=2005&sciodt=0,5&hl=en): 475)
* Yang Liu, Qun Liu, and Shouxun Lin. 2006. [Tree-to-String Alignment Template for Statistical Machine Translation](http://aclweb.org/anthology/P06-1077). In *Proceedings of COLING/ACL 2006*. ([Citation](https://scholar.google.com.hk/scholar?cites=8683308453323663525&as_sdt=2005&sciodt=0,5&hl=en): 391)
* Deyi Xiong, Qun Liu, and Shouxun Lin. 2006. [Maximum Entropy Based Phrase Reordering Model for Statistical Machine Translation](https://aclanthology.info/pdf/P/P06/P06-1066.pdf). In *Proceedings of COLING/ACL 2006*. ([Citation](https://scholar.google.com.hk/scholar?cites=11896300896063367737&as_sdt=2005&sciodt=0,5&hl=en): 299)
* David Chiang. 2007. [Hierarchical Phrase-Based Translation](http://aclweb.org/anthology/J07-2003). *Computational Linguistics*. ([Citation](https://scholar.google.com.hk/scholar?cites=17074501474509484516&as_sdt=2005&sciodt=0,5&hl=en): 1,192)
* Liang Huang and David Chiang. 2007. [Forest Rescoring: Faster Decoding with Integrated Language Models](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.88.5058&rep=rep1&type=pdf). In *Proceedings of ACL 2007*. ([Citation](https://scholar.google.com.hk/scholar?cites=2826188279623417237&as_sdt=2005&sciodt=0,5&hl=en): 280)
* Haitao Mi, Liang Huang, and Qun Liu. 2008. [Forest-based Translation](http://aclweb.org/anthology/P08-1023). *In Proceedings of ACL 2008*. ([Citation](https://scholar.google.com.hk/scholar?cites=11263493281241243162&as_sdt=2005&sciodt=0,5&hl=en): 239)
* Min Zhang, Hongfei Jiang, Aiti Aw, Haizhou Li, Chew Lim Tan, and Sheng Li. 2008. [A Tree Sequence Alignment-based Tree-to-Tree Translation Model](http://www.aclweb.org/anthology/P08-1064). In *Proceedings of ACL 2008*. ([Citation](https://scholar.google.com.hk/scholar?cites=4828105603038412208&as_sdt=2005&sciodt=0,5&hl=en): 124)
* Libin Shen, Jinxi Xu, and Ralph Weischedel. 2008. [A New String-to-Dependency Machine Translation Algorithm with a Target Dependency Language Model](http://aclweb.org/anthology/P08-1066). In *Proceedings of ACL 2008*. ([Citation](https://scholar.google.com.hk/scholar?cites=15082517325172081801&as_sdt=2005&sciodt=0,5&hl=en): 278)
* Haitao Mi and Liang Huang. 2008. [Forest-based Translation Rule Extraction](http://aclweb.org/anthology/D08-1022). In *Proceedings of EMNLP 2008*. ([Citation](https://scholar.google.com.hk/scholar?cites=11263493281241243162&as_sdt=2005&sciodt=0,5&hl=en): 239)
* Yang Liu, Yajuan Lü, and Qun Liu. 2009. [Improving Tree-to-Tree Translation with Packed Forests](http://aclweb.org/anthology/P09-1063). In *Proceedings of ACL/IJNLP 2009*. ([Citation](https://scholar.google.com.hk/scholar?cites=3907324274083528908&as_sdt=2005&sciodt=0,5&hl=en): 93)
* David Chiang. 2010. [Learning to Translate with Source and Target Syntax](http://aclweb.org/anthology/P10-1146). In *Proceedings of ACL 2010*. ([Citation](https://scholar.google.com.hk/scholar?cites=18270412258769590027&as_sdt=2005&sciodt=0,5&hl=en): 118)

<h1 id="discriminative_training">Discriminative Training</h1>

* Franz Josef Och and Hermann Ney. 2002. [Discriminative Training and Maximum Entropy Models for Statistical Machine Translation](http://aclweb.org/anthology/P02-1038). In *Proceedings of ACL 2002*. ([Citation](https://scholar.google.com.hk/scholar?cites=2845378992177918439&as_sdt=2005&sciodt=0,5&hl=en): 1,258)
* Franz Josef Och. 2003. [Minimum Error Rate Training in Statistical Machine Translation](http://aclweb.org/anthology/P03-1021). In *Proceedings of ACL 2003*. ([Citation](https://scholar.google.com.hk/scholar?cites=15358949031331886708&as_sdt=2005&sciodt=0,5&hl=en): 2,984)
* Taro Watanabe, Jun Suzuki, Hajime Tsukada, and Hideki Isozaki. 2007. [Online Large-Margin Training for Statistical Machine Translation](http://aclweb.org/anthology/D07-1080). In *Proceedings of EMNLP-CoNLL 2007*. ([Citation](https://scholar.google.com.hk/scholar?cites=6690339336101573833&as_sdt=2005&sciodt=0,5&hl=en): 197)
* David Chiang, Kevin Knight, and Wei Wang. 2009. [11,001 New Features for Statistical Machine Translation](http://aclweb.org/anthology/N09-1025). In *Proceedings of NAACL 2009*. ([Citation](https://scholar.google.com.hk/scholar?cites=14062409519286340147&as_sdt=2005&sciodt=0,5&hl=en): 251)

<h1 id="system_combination">System Combination</h1>

* Antti-Veikko Rosti, Spyros Matsoukas, and Richard Schwartz. 2007. [Improved Word-Level System Combination for Machine Translation](http://aclweb.org/anthology/P07-1040). In *Proceedings of ACL 2007*. ([Citation](https://scholar.google.com.hk/scholar?cites=13310846375895519088&as_sdt=2005&sciodt=0,5&hl=en): 144)
* Xiaodong He, Mei Yang, Jianfeng Gao, Patrick Nguyen, and Robert Moore. 2008. [Indirect-HMM-based Hypothesis Alignment for Combining Outputs from Machine Translation Systems](http://aclweb.org/anthology/D08-1011). In *Proceedings of EMNLP 2008*. ([Citation](https://scholar.google.com.hk/scholar?cites=5843300493006970528&as_sdt=2005&sciodt=0,5&hl=en): 96)

<h1 id="human_centered_smt">Human-centered SMT</h1>

<h2 id="interactive">Interactive SMT</h2>

* George Foster, Pierre Isabelle and Pierre Plamondon. 1997. [Target-text mediated interactive machine translation](https://sci-hub.tw/10.2307/40009035). *Machine Translation*. ([Citation](https://scholar.google.com/scholar?cites=17084037882064721827&as_sdt=2005&sciodt=0,5): 116)
* Philippe Langlais, Guy Lapalme and Marie Lorange. 2002. [TransType: Development-Evaluation Cycles to Boost Translator’s Productivity](https://sci-hub.tw/10.2307/40007093). *Machine Translation*. ([Citation](https://scholar.google.com/scholar?cites=7892155138946158318&as_sdt=2005&sciodt=0,5): 74)
* Jesús Tomas and Francisco Casacuberta. 2006. [Statistical phrase-based models for interactive computer-assisted translation](http://aclweb.org/anthology/P06-2107). In *Proceedings of COLING/ACL*. ([Citation](https://scholar.google.com/scholar?cites=2242179645100420046&as_sdt=2005&sciodt=0,5): 31)
* Enrique Vidal, Francisco Casacuberta, Luis Rodríguez-Ruiz, Jorge Civera, Carlos D. Martínez-Hinarejos. 2006. [Computer-Assisted Translation Using Speech Recognition](https://ieeexplore.ieee.org/document/1621206). *IEEE Transaction on Audio, Speech and Language Processing*. ([Citation](https://scholar.google.com/scholar?cites=32625184311110830&as_sdt=2005&sciodt=0,5): 62)
* Shahram Khadivi and Hermann Ney. 2008. [Integration of Speech Recognition and Machine Translation in Computer-Assisted Translation](https://sci-hub.tw/10.1109/tasl.2008.2004301). *IEEE Transaction on Audio, Speech and Language Processing*. ([Citation](https://scholar.google.com/scholar?cites=1690852455408892756&as_sdt=2005&sciodt=0,5): 30)
* Sergio Barrachina, Oliver Bender, Francisco Casacuberta, Jorge Civera, Elsa Cubel, Shahram Khadivi, Antonio L. Lagarda, Hermann Ney, Jesús Tomás and Enrique Vidal. 2009. [Statistical approaches to computer-assisted translation](https://www.mitpressjournals.org/doi/abs/10.1162/coli.2008.07-055-R2-06-29). *Computational Linguistics*. ([Citation](https://scholar.google.com/scholar?cites=17691637682117292572&as_sdt=2005&sciodt=0,5): 207)
* Francisco Casacuberta, Jorge Civera, Elsa Cubel, Antonio L. Lagarda, Guy Lapalme, Elliott Macklovitch, Enrique Vidal. 2009. [Human interaction for high quality machine translation](https://sci-hub.tw/10.1145/1562764.1562798). *Communications of the ACM*. ([Citation](https://scholar.google.com/scholar?cites=6184654159576071790&as_sdt=2005&sciodt=0,5): 49)
* Vicent Alabau, Alberto Sanchis and Francisco Casacuberta. 2014. [Improving on-line handwritten recognition in interactive machine translation](sci-hub.tw/10.1016/j.patcog.2013.09.035). *Pattern Recognition*. ([Citation](https://scholar.google.com/scholar?cites=11987123133913382404&as_sdt=2005&sciodt=0,5): 18)
* Shanbo Cheng, Shujian Huang, Huadong Chen, Xin-Yu Dai and  Jiajun Chen. 2016. [PRIMT: A Pick-Revise Framework for Interactive Machine Translation](http://www.aclweb.org/anthology/N16-1148). In *Proceedings of NAACL 2016*. ([Citation](https://scholar.google.com/scholar?cites=3643727460542665178&as_sdt=2005&sciodt=0,5): 9)
* Miguel Domingo, Álvaro Peris and Francisco Casacuberta. 2018. [Segment-based interactive-predictive machine translation](https://www.researchgate.net/publication/322275484_Segment-based_interactive-predictive_machine_translation). *Machine Translation*. ([Citation](https://scholar.google.com/scholar?cites=4148585683672959462&as_sdt=2005&sciodt=0,5): 2)

<h2 id="adaptation_smt">Adaptation</h2>

* Pascual Martínez-Gómez, Germán Sanchis-Trilles and Francisco Casacuberta. 2012. [Online adaptation strategies for statistical machine translation in post-editing scenarios](https://sci-hub.tw/10.1016/j.patcog.2012.01.011). *Pattern Recognition*. ([Citation](https://scholar.google.com/scholar?cites=9143628035426486873&as_sdt=2005&sciodt=0,5): 40)
* Jesús González-Rubio and Francisco Casacuberta. 2014. [Cost-Sensitive Active Learning for Computer-Assisted Translation](https://sci-hub.tw/10.1016/j.patrec.2013.06.007). *Pattern Recognition Letters*. ([Citation](https://scholar.google.com/scholar?cites=13196627956841822823&as_sdt=2005&sciodt=0,5): 11)
* Antonio L. Lagarda, Daniel Ortiz-Martínez, Vicent Alabau and Francisco Casacuberta. 2015. [Translating without in-domain corpus: Machine translation post-editing with online learning techniques](https://sci-hub.tw/10.1016/j.csl.2014.10.004). *Computer Speech & Language*. ([Citation](https://scholar.google.com/scholar?cites=6721510771212778605&as_sdt=2005&sciodt=0,5): 10)
* Germán Sanchis-Trilles, Francisco Casacuberta. 2015. [Improving translation quality stability using Bayesian predictive adaptation](https://sci-hub.tw/10.1016/j.csl.2015.03.001). *Computer Speech & Language*. ([Citation](https://scholar.google.com/scholar?q=Improving+translation+quality+stability+using+Bayesian+predictive+adaptation): 1)
* Daniel Ortiz-Martínez. 2016. [Online Learning for Statistical Machine Translation](https://www.mitpressjournals.org/doi/full/10.1162/COLI_a_00244). *Computational Linguistics*. ([Citation](https://scholar.google.com/scholar?cites=4979468821667106694&as_sdt=2005&sciodt=0,5): 13)
