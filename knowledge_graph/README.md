# Paper List

在学习过程中看了很多paper或教程，都存到了自己的文件夹里，但放久了自己都忘了哪篇对应哪个算法了。因此整理起来放到这里。这个列表会随着我的学习不断更新。

## 知识图谱介绍

* [知识图谱入门笔记](https://zhuanlan.zhihu.com/c_211846834)    
* [从零开始构建知识图谱](https://zhuanlan.zhihu.com/c_1018901137012928512)    
* [徐增林_知识图谱技术综述](https://www.jianguoyun.com/p/DafFvLcQq_6CBxi-6XM)    
* [知识图谱构建技术综述](https://www.jianguoyun.com/p/Da-sCUcQq_6CBxjB6XM)

## RDF 语法

* JSON-LD[A JSON-based Serialization for Linked Data](https://json-ld.org/)    
* Turtle [ RDF 1.1 Turtle Terse RDF Triple Language](https://www.w3.org/TR/turtle/)    
* Turtle中文翻译(自己翻译的，仅供参考)[RDF 1.1 Turtle 中文翻译](https://zhuanlan.zhihu.com/p/44381615)

## 结构化数据的知识抽取
从结构化数据如MYSQL等数据库获取知识得到三元组。

* 直接映射，W3C的[ A Direct Mapping of Relational Data to RDF  ](https://www.w3.org/TR/rdb-direct-mapping/)    
* R2RML[R2RML: RDB to RDF Mapping Language](https://www.w3.org/TR/r2rml/)    
* D2RQ [D2RQ Accessing Relational Databases as Virtual RDF Graphs](http://d2rq.org/)

## 半结构化文本的知识抽取

* [面向半结构化文本的知识抽取研究](https://www.jianguoyun.com/p/DaJwJnsQq_6CBxiy6XM)    
* [抽取 Web 信息的包装器归纳学习构造](https://www.jianguoyun.com/p/DfkkQ3QQq_6CBxiz6XM)    
* 中文百科类知识图谱的构建 zhishi.me [Zhishi.me - Weaving Chinese Linking Open Data](https://www.jianguoyun.com/p/DbFQAPoQq_6CBxi06XM)    
* [Wikipedia Mining Wikipedia as a Corpus for Knowledge Extraction](https://www.jianguoyun.com/p/DUUsSxoQq_6CBxi26XM)    
* [Mining Type Information from Chinese Online Encyclopedias](https://www.jianguoyun.com/p/DcSjsMYQq_6CBxi36XM)    
* Depedia 的构建 [DBpedia A Nucleus for a Web of Open Data](https://www.jianguoyun.com/p/DZYAPMIQq_6CBxi46XM)    
* [DBpedia A Multilingual Cross-Domain Knowledge Base](https://www.jianguoyun.com/p/DZm_Ym8Qq_6CBxi56XM)    
* [DBpedia - A crystallization point for the Web of Data ](https://www.jianguoyun.com/p/DROkjWoQq_6CBxi66XM)    
* [DBpedia - A Large-scale, MultilingualKnowledge Base Extracted from Wikipedia](https://www.jianguoyun.com/p/DRS78wIQq_6CBxi86XM)

## 非结构化文本知识抽取

### 命名实体识别

* [CRF++的使用](https://taku910.github.io/crfpp/#download)    
* [使用CRF++做词性标注等序列化任务](https://github.com/Pelhans/ZNLP/tree/master/lexical_analysis/crfpos%2B%2B)    
* 使用深度学习做命名实体识别[Neural Architectures for Named Entity Recognition](https://www.jianguoyun.com/p/Df6Up8kQq_6CBxi663M)    
* [Bidirectional LSTM-CRF Models for Sequence Tagging](https://www.jianguoyun.com/p/DVPq0SgQq_6CBxi563M)    

### 关系抽取

#### 无监督方法

* 基于模板类的实体关系抽取，最简单的是[基于触发词的匹配](http://pelhans.com/2018/03/19/xiaoxiangkg-note3/#%E5%9F%BA%E4%BA%8E%E8%A7%A6%E5%8F%91%E8%AF%8D%E7%9A%84pattern)   
* 复杂一点的如基于依存句法匹配的,该方法对输入的单据进行依存分析，通过依存分析输出的依存弧判断单句是否为动词谓语句，如果是则结合中文语法启发式规则抽取关系表述。根据距离确定论元位置，对三元组进行评估，输出符合条件的三元组  [基于依存分析的开放式中文实体关系抽取方法](https://www.jianguoyun.com/p/DcmCTjAQq_6CBxjS63M)    
* 基于核的方法典型的为编辑距离核、字符串核、卷积树核等。基于卷积树核的方法以最短路径包含树作为关系实例的结构化表示形式，以卷积树核作为树相似度的计算方法，采用分层聚类方法进行无监督中文实体关系抽取。[基于卷积树核的无指导中文实体关系抽取研究](https://www.jianguoyun.com/p/DWHoHEgQq_6CBxjU63M)    
* 基于聚类的方法，如对共现的实体及它们的上下文进行聚类，最后标记每一个类簇，以核心词汇作为关系表述。如[无监督关系抽取方法研究](http://xueshu.baidu.com/s?wd=paperuri%3A%2838e36a4d56216693db5923975f0b36e4%29&filter=sc_long_sign&tn=SE_xueshusource_2kduw22v&sc_vurl=http%3A%2F%2Fwww.doc88.com%2Fp-1177286175360.html&ie=utf-8&sc_us=11379075570837652647)    

####  半监督方法

* 标签传播算法[标签传播算法理论及其应用研究综述](https://www.jianguoyun.com/p/DZWOPZIQq_6CBxie7HM)    
* 标签传播算法论文[Relation Extraction Using Label Propagation Based Semi-supervisedLearning](https://www.jianguoyun.com/p/DT1Rn2QQq_6CBxig7HM)    
* 协同训练[基于弱监督学习的海量网络数据关系抽取](https://www.jianguoyun.com/p/DXGXUkUQq_6CBxim7HM)    
* Boot Strapping 算法[基于Boot Strapping的中文实体关系自动生成](https://www.jianguoyun.com/p/DRbjl-gQq_6CBxip7HM)    
* 远程监督 [Distant supervision for relation extraction without labeled data](https://www.jianguoyun.com/p/DbBDsOkQq_6CBxis7HM)   

#### 监督学习

ONGOING
