---
marp: true
theme: gaia
_class: lead
paginate: true
backgroundColor: #fff
backgroundImage: url('https://marp.app/assets/hero-background.svg')
---



# 知识图谱构建与应用最佳实践

关键词：知识图谱、图数据库、数据模型、MLOps、知识提取、图表征

2021.10.18
苏锦华

Presetation available at: https://github.com/SmartDataLab/KG-Share

Written with Marp and Mermaid on Markdown

---

# 引子

> One hidden layer Perception with non-linear activation function       -- Logistic Regression

知识图谱、图神经网络概念火热，国内有成熟的知识图谱产品吗？

<!-- _class: lead -->
:satisfied:


知识图谱技术落地需要 **表子好看，里子实在**。


---

# 商业智能-行业数据库-知识挖掘

![bg drop-shadow h:280 bottom:80%](https://img1.baidu.com/it/u=2361940023,59105053&fm=26&fmt=auto)

![bg drop-shadow h:280](https://img2.baidu.com/it/u=2505796721,2593407729&fm=26&fmt=auto)

![bg drop-shadow h:220](https://memect.cn/img/%E6%96%87%E5%9B%A0%E4%BA%92%E8%81%94%E7%99%BD%E5%AD%97logo.svg)

<!-- todo: use html and css language to make align the picture -->

---

# 背后依托的技术



1. 知识挖掘：用户交互以及NLP
2. 数据存储：图数据库 :smile:
3. 数据分析：图算法及可视化技术 :smile:
4. 图谱应用：图表征以及图神经网络

```mermaid
graph TD;
    A[知识挖掘]-->B[图数据库];
    B-->C[数据分析];
    B-->D[图谱应用];
    C-->D;
```

![bg right:40% drop-shadow 50%](chart1.png)

---

# 知识图谱产品架构

- MLOps System
	- Kubernetes
	- Jenkins X: MLOps [Quickstarts](https://jenkins-x.io/v3/mlops/mlquickstarts/)
	- General ML Deployment: ONNX 
- EIS: Expert Interact System
	- Human Labelling & Heuristic Algorithm
	- Monitoring & Back-testing
	- Quality: Bad Cases in KG

![bg right:40% drop-shadow 60%](chart2.png)

---

# 知识图谱产品架构 cont.

- KES: Knowledge Extraction System
	- Transfer from RDBS
	- Entity Recoginition
		- Node presentation
		- Breadth first priority search
	- Link Prediction
		- shortest path
		- NLP semantic distance
	- Attribution Extration

![bg right:30% drop-shadow 80%](chart2.png)

---

# 知识图谱产品架构 cont.

- DMP: Data Manage Platform
	- DataHub to manage the dirty data
	- Graph Database
- API Platform
	- Graph Visualization
	- Node Representation
	- Prediction Tasks
		- intelligent search(google page rank)
		- KG-based Q&A (NLP)

![bg right:30% drop-shadow 80%](chart2.png)

---

# Expert Interact System

- Brat (labelling tool) [link](http://brat.nlplab.org)

![drop-shadow w:550](http://brat.nlplab.org/img/frontpage/008-relation-annotation-example.png)

---

# 为什么要MLOps

<!-- _class: lead -->
Machine Learning: The High Interest Credit Card of Technical Debt
A paper in NIPS 2014 workshop

![w:600 drop-shadow](mlops-1.png)

Rules of Machine Learning: Best Practices for ML Engineering [link](https://developers.google.com/machine-learning/guides/rules-of-ml/#training-serving_skew)


**training-serving skew** :smile:

---

# MLOps(low level)

![w:1150 drop-shadow](mlops-continuous-delivery-and-automation-pipelines-in-machine-learning-2-manual-ml.svg)

---


# MLOps(high level)

![w:800 drop-shadow](mlops-continuous-delivery-and-automation-pipelines-in-machine-learning-4-ml-automation-ci-cd.svg)

---

# MLOps Tools(support gpu)

![bg h:200 drop-shadow](https://logowik.com/content/uploads/images/301_docker.jpg)
![bg h:200 drop-shadow](https://i0.wp.com/softwareengineeringdaily.com/wp-content/uploads/2019/01/Kubernetes_New.png?resize=730%2C389&ssl=1)
![bg h:200 drop-shadow](jenkinsx.png)
![bg h:200 drop-shadow](https://img1.baidu.com/it/u=1796289449,737951261&fm=26&fmt=auto)

---

# Surprise?

Data Version Control(Boom!)

Continuous Training Pipeline


![bg right h:450 drop-shadow](iterative_ai.png)

---

# Knowledge Extraction System

A structure from CSDN(author: coder_oyang)

![drop-shadow w:750](https://img-blog.csdnimg.cn/20190310120120976.JPG?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2NvZGVyX295YW5n,size_16,color_FFFFFF,t_70)

---



# 构建工具

推荐[OpenKG](http://www.openkg.cn/)(浙大),网站整理了大量工具和相关技术文章

- 中文NLP工具:([哈工大LTP](http://ltp.ai/)，车万翔)
- 知识提取工具:[DeepKE](https://github.com/zjunlp/DeepKE)(浙大，结合prompt，适合few-shot场景)

![drop-shadow w:600](architectures.png)

<!-- _class: lead -->

---

# LightNER [arXiv](https://arxiv.org/pdf/2109.00720.pdf)



![w:850 drop-shadow](LightNER.png)

---

# LightRE [github](https://github.com/zjunlp/DeepKE/tree/test_new_deepke/tutorial-notebooks/re/few-shot)

![w:850 drop-shadow](LightRE.png)

---


# Data Manage Platform

思考:thinking:关系型数据库(RDBMS)与NoSQL的发展和知识图谱有什么联系

> Web2.0进入了“可读可写”模式，交互内容的急剧增加，RDBMS在超大规模数据的高并发处理力不从心,NoSQL应运而生。


![bg h:300 vertical right drop-shadow](https://pic3.zhimg.com/80/v2-1d0978287a4a88e7e4bead39955cdf7e_720w.jpg)
![bg h:300  drop-shadow](https://pic4.zhimg.com/80/v2-05ecbec555a42ea0199f810a78b4ba8f_720w.jpg)

---

# 图数据库的选择


![bg h:300 drop-shadow](gdb_rank.png)
![bg h:300 drop-shadow](https://img0.baidu.com/it/u=735505223,2214078686&fm=26&fmt=auto)

---

# Neo4j生态

![bg h:400 drop-shadow](neo4j_eco.png)
![bg h:400 drop-shadow](neo4j_product.png)

---

# Transfer from RDBMS

![bg h:400 drop-shadow](https://dist.neo4j.com/wp-content/uploads/relational_org_chart.jpg)
![bg h:400 drop-shadow](https://dist.neo4j.com/wp-content/uploads/graph_org_chart.jpg)

---

# Schema: Model Design

![bg h:300 drop-shadow](https://dist.neo4j.com/wp-content/uploads/matrix_whiteboard_model2.png)
![bg h:300 drop-shadow](https://dist.neo4j.com/wp-content/uploads/matrix_whiteboard_model3.png)

---

# Complex Case 1: 


> Property vs Relationship

```
//find which movies share genres
MATCH (m1:Movie), (m2:Movie)
WHERE any(x IN m1.genre WHERE x IN m2.genre)
AND m1 <> m2
RETURN m1, m2;
```


![h:200 drop-shadow](https://dist.neo4j.com/wp-content/uploads/modeling_genre_node.jpg)

![bg h:200 vertical right drop-shadow](https://dist.neo4j.com/wp-content/uploads/modeling_genre_property.jpg)

![bg h:300  drop-shadow](https://pic4.zhimg.com/80/v2-05ecbec555a42ea0199f810a78b4ba8f_720w.jpg)


---

# Complex Case 2: 

> Hyperedges or Intermediate Nodes


**Cypher Target**:Coappearance

```
MATCH (a:Moment)--(b:Role) WHERE b.name == "Alias"
WITH a as a1
MATCH (a:Moment)--(b:Role) WHERE b.name == "Person"
WITH a as a2
WITH apoc.coll.intersection(a1, a2) as a3
RETURN a3
```

```
MATCH (c:Appearance = "Alias-Person")
```

![bg h:300 vertical right drop-shadow](https://dist.neo4j.com/wp-content/uploads/modeling_marvel_hyperedge_appearance.jpg)
![bg h:300  drop-shadow](https://pic4.zhimg.com/80/v2-05ecbec555a42ea0199f810a78b4ba8f_720w.jpg)

---

# Complex Case 3: 


> Property vs Relationship


**Cypher Target**:Flight Date

![h:200 drop-shadow](https://dist.neo4j.com/wp-content/uploads/modeling_airport_flight_dates.jpg)

![bg h:200 vertical right drop-shadow](https://dist.neo4j.com/wp-content/uploads/modeling_airport_flights.jpg)

![bg h:300  drop-shadow](https://pic4.zhimg.com/80/v2-05ecbec555a42ea0199f810a78b4ba8f_720w.jpg)


---

# My Bad Case&A Good Case: 

**False Litigation**

![bg right h:450 drop-shadow](law_graph.jpeg)


**Salesman Outlier Dection**


---

# 图谱应用工具

- 知识表示：[清华大学OpenKE]()
	- RESCAL
	- DistMult, ComplEx, Analogy
	- TransE, TransH, TransR, TransD
	- SimplE
	- RotatE
- 可视化工具
	- Boom(Neo4j Lab)
	- Echarts(Baidu)


---

<!-- _class: lead -->

# Thanks