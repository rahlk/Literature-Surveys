# Validating XTREE's Plans

## Methods in SE

| Year/Cite | Title | Methods | Results | Remarks | Dataset |
|:-----------:|:----------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------:|
| 2008/Patent | Association Rule Mining To Predict Co-varying Software Metrics | They use Apriori Method (Agrawal94) on CK-Metrics | (See below) | Easy implementation. | CK-Metrics. Not mentioned. |
| 2009/32 | Integrating in-process software defect prediction with association mining to discover defect pattern | +Attributes divided into two categories, top-down algorithmapply the binary partitioning recursively to a whole interval. +Association Rule Based Defect Prediction | Acc-85.71 Rec-81.82 Prec-87.10 Spec-84.62 | +Association rule mining to discover defect patterns and multi-interval discretization to handle the continuous attributes. +Works on discrete/continuous/combo | [here](http://www.sciencedirect.com.prox.lib.ncsu.edu/science/article/pii/S0164121206002603?np=y) |
| 2014/17 | Software defect prediction using relational association rule mining | +DRAR algorithm (Discovery of Relational Association Rules) | [Fig](https://cloud.githubusercontent.com/assets/1433964/13813601/caceaf68-eb58-11e5-8112-4e941c2beed6.png) | +Assosciation rules for NASA datasets. +Readily implemetable | PROMISE |

#### 1. Co-varying Software Metrics
![image](https://cloud.githubusercontent.com/assets/1433964/13811794/4e167ea6-eb4e-11e5-9fae-cfca1fa18ddf.png)

#### 2. DPRAR
![image](https://cloud.githubusercontent.com/assets/1433964/13813601/caceaf68-eb58-11e5-8112-4e941c2beed6.png)

# Proposed Framework
![new doc 3](https://cloud.githubusercontent.com/assets/1433964/13814006/ec0a0b1c-eb5a-11e5-9d5f-66c6b4e86f8d.jpg)

# Challenges:
 - Finding supports, see #4 below for a solution.
 - Baselining against other State-of-the-art methods. See #3 below.
 - Understanding global constrains for transfer learning. Use Inductive process modelling to derive constrains. [Paper](https://scholar.google.com/scholar_url?url=http://citeseerx.ist.psu.edu/viewdoc/download%3Fdoi%3D10.1.1.296.248%26rep%3Drep1%26type%3Dpdf&hl=en&sa=T&oi=gsb-ggp&ct=res&cd=0&ei=TmTpVuv7NcmCmQHUia3oCg&scisig=AAGBfm2r5855c07VJ_TX-WexVxvheMguAw)

## Methods From ML: Planning with k-item sets

| Year/Citations |                                            Title                                           | Methods                                                                                                  | Results                                                       | Remarks                                                                                                                                                                                                                                                                     | Data Sets                        |
|----------------|:------------------------------------------------------------------------------------------:|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| 1994/19392     | Fast Algorithms for Mining Association Rules                                               | +Apriori +ArioriTid +Hybrid                                                                           | Out performs most algorithms.  Highly scaleable.              | Most widely used.  Unsupervised                                                                                                                                                                                                                                             |                                  |
| 2011/92        | Itemset Mining: a Constraint Programming Perspective                                       | Survey of +Frequent Itemset +Closed Itemset +Discriminative Itemset** +Itemset mining  with costs** | Has theorems and properties. No relevant results.             | Discriminative Itemset: Discovery of rules in data in which every transaction is labeled with a (binary) class label. The task is here  to find itemsets that allow one to discriminate the transactions belonging to one class from those belonging to  the other class. |                                  |
| 1999/199       | Detecting Change in Categorical Data: Mining Contrast Sets                                 | +STUCCO                                                                                                 | Not directly relevant, but tiny.cc/me01                       | Surprisingly similar to XTREE! -Modeled as a tree search -Tree built by adding k-item sets to  an empty root node. -Search this tree in a breadth-first,  level-wise manner,                                                                                             | UCI Data base                    |
| 2009/28        | An Efficient Rigorous Approach for Identifying Statistically Significant Frequent Itemsets | +Algorithm that identifies  statistically significant support threshold  for item sets.                 | +Finds thresholds with Type I/II error margin less than 0.05 | +First method to find support. (Most researchers use engg. judgement) +They use a Poisson approximation + It takes into account the entire dataset rather than  individual discoveries                                                                                    | http://fimi.cs.helsinki.fi/data/ |
