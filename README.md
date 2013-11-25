Kloud Kd Tree (KdKdT)
=====================

[project link](https://github.com/yvesx/KDKDTree).

Introduction
------------
Kloud Kd Tree implements Kd Tree in a map reduce framework. Details are in [this](http://www.vision.caltech.edu/malaa/publications/aly11distributed.pdf) paper.

Two implementations
-------------------

* under `./MapReduceKDT/`

* Independent Kd Trees

* Distributed Kd Trees

Index operations
----------------

* Run `./ikdt_index.sh` or `./dkdt_index.sh` under `./MapReduceKDT/`

* Index trees are stored in `ikdt_index_output.py` as a python variable.

Query operations
----------------

* Run `./ikdt_query.sh` or `./dkdt_query.sh` under `./MapReduceKDT/`

* Output stored in `ikdt_query_output.py` as a python variable.

Benchmarking
------------

* `./generate.py` provides basic functionality to generate test data with various rows/dimensions/distributions.

* `./index.py` can perform single machine Kd tree tests.

* `./index_lsh.py` can perform single machine indexing using E2LSH [scheme](http://www.mit.edu/~andoni/LSH/).

Eyra
====

[project link](https://github.com/yvesx/eyra).

Eyra Search: avdanced way to discover walls and handles

using underlying knowledge graphs to discover related Facebook walls and @handles. 

The Problem
-----------

* Currently, search on Facebook using descriptive query is not effective in returning wall pages. For example, the query "Luxury department store" returns a single Australian page for a US-based user.
![alt tag](https://raw.github.com/yvesx/projects/master/eyra_imgs/5.png)

Sample @handle Search Sessions
------------------------------

* WSJ
![alt tag](https://raw.github.com/yvesx/projects/master/eyra_imgs/WSJ.png)

* Vacation
![alt tag](https://raw.github.com/yvesx/projects/master/eyra_imgs/vacation.png)

* TV
![alt tag](https://raw.github.com/yvesx/projects/master/eyra_imgs/TV.png)

* Travel
![alt tag](https://raw.github.com/yvesx/projects/master/eyra_imgs/travel.png)

* Starwood
![alt tag](https://raw.github.com/yvesx/projects/master/eyra_imgs/starwood.png)

* Affluence
![alt tag](https://raw.github.com/yvesx/projects/master/eyra_imgs/rich.png)

* Retailers
![alt tag](https://raw.github.com/yvesx/projects/master/eyra_imgs/retail.png)

* Politicians
![alt tag](https://raw.github.com/yvesx/projects/master/eyra_imgs/politicians.png)

* NBA
![alt tag](https://raw.github.com/yvesx/projects/master/eyra_imgs/NBA.png)

* Journalists
![alt tag](https://raw.github.com/yvesx/projects/master/eyra_imgs/journalist.png)

* IndyCar
![alt tag](https://raw.github.com/yvesx/projects/master/eyra_imgs/indycar.png)

* Diet
![alt tag](https://raw.github.com/yvesx/projects/master/eyra_imgs/diet.png)

* Couture
![alt tag](https://raw.github.com/yvesx/projects/master/eyra_imgs/chanel.png)


Basic Idea and Methodology
--------------------------

![alt tag](https://raw.github.com/yvesx/projects/master/eyra_imgs/0.png)
![alt tag](https://raw.github.com/yvesx/projects/master/eyra_imgs/2.png)
![alt tag](https://raw.github.com/yvesx/projects/master/eyra_imgs/3.png)
![alt tag](https://raw.github.com/yvesx/projects/master/eyra_imgs/4.png)


Ibex
====

[project link](https://github.com/yvesx/ibex).

label propagation, transfer learning, collaborative filtering

* Unlike Facebook pages, Twitter @handles lack default category. 
* Official API lacks good support for finding:
 * *verified, most followed @handles related to NBA* ``GET``
 * *@handles in both Golf and Fashion* ``GET``
 * *top 3 categories that @elonmusk should be in* ``ASSIGN``
 * *Similar @handles to @BarackObama* ``FIND``
 * *@handles matching \_arbitrary\_description_* ``SEARCH`` (Not just string match but semantic,relational match as well)


Basic Idea and Methodology
--------------------------

![alt tag](https://raw.github.com/yvesx/projects/master/ibex_imgs/1.png)
![alt tag](https://raw.github.com/yvesx/projects/master/ibex_imgs/2.png)
![alt tag](https://raw.github.com/yvesx/projects/master/ibex_imgs/3.png)
![alt tag](https://raw.github.com/yvesx/projects/master/ibex_imgs/4.png)
![alt tag](https://raw.github.com/yvesx/projects/master/ibex_imgs/5.png)
![alt tag](https://raw.github.com/yvesx/projects/master/ibex_imgs/6.png)

Silverback
===========



[code ](https://github.com/yvesx/Silverback) for our Silverback paper on efficient probabilistic association mining and a lightweight 
distribution framework. 

We address the problem of large scale probabilistic association rules mining and consider the trade-offs between accuracy of the mining results and quest of scalability on modest hardware infrastructure. We demonstrate how extensions and adaptations of research findings can be integrated in an industrial application, and we present the commercially deployed Silverback framework, developed at Voxsup Inc. Silverback tackles the storage efficiency by proposing a probabilistic columnar infrastructure and using Bloom filters and reservoir sampling techniques. In addition, a probabilistic pruning technique has been introduced based on Apriori for mining frequent item-sets. The proposed target-driven technique yields a significant reduction on the size of the frequent item-set candidates. We present extensive experimental evaluations which demonstrate the benefits of a context-aware incorporation of infrastructure limitations into corresponding research techniques. The experiments indicate that, when compared to traditional Hadoop-based approach for improving scalability by adding more hosts, Silverback – which has been commercially deployed and developed at Voxsup Inc. since May 2011 – has much better run-time performance with negligible accuracy sacrifices.

Two publications that describe our system:
* ``30th IEEE ICDE 2014`` Yusheng Xie, Diana Palsetia, Ankit Agrawal, Goce Trajcevski, and Alok Choudhary. *Silverback: Scalable Association Mining For Massive temporal Data in Columnar Probabilistic Databases*
* ``NU-EECS-13-06`` Yusheng Xie, Diana Palsetia, Kunpeng Zhang, Ankit Agrawal, Goce Trajcevski, Alok Choudhary: *Silverback: Scalable Association Mining For Massive Temporal Data in Columnar Probabilistic Databases*


Methodology
-----------

* Use a columnar, probabilistic storage for transactions.
![alt tag](https://raw.github.com/yvesx/projects/master/silverback_imgs/1.png)
* Frequent item-sets mining using Bloom Filter operations.
![alt tag](https://raw.github.com/yvesx/projects/master/silverback_imgs/2.png)
![alt tag](https://raw.github.com/yvesx/projects/master/silverback_imgs/3.png)
* Min-hash based prunning technique for drastically reducing candidate item-sets.
![alt tag](https://raw.github.com/yvesx/projects/master/silverback_imgs/4.png)

Distributed Framework
---------------------

* A distributed Framework for multi-node scalability ([Ill.](http://blog.andresteingress.com/2010/10/14/happy-messaging-with-activemq-and-si-part-1/))
![alt tag](https://raw.github.com/yvesx/projects/master/silverback_imgs/8.png)

Results and Performance
-----------------------

* False-positive impact introduced by using Bloom Filters
![alt tag](https://raw.github.com/yvesx/projects/master/silverback_imgs/5.png)
* The dots perfectly lining up with the red line would imply there is no error introduced through Bloom Filters. The plots below show that Bloom Fitler introduces marginal errors.
![alt tag](https://raw.github.com/yvesx/projects/master/silverback_imgs/6.png)
* Multi-node scalability and performance
![alt tag](https://raw.github.com/yvesx/projects/master/silverback_imgs/7.png)

Usage
-----

config file available upon request.

silverback core: core implementatation of mining algorithms and distributed framework. data source-independent code.

silverback fb/tw: data-dependent implementation of communication services. Different data sources may require different sets of allowable operations.

Please see the README file in each folder. To use, 

``$ mkdir silverback_deployment``
``$ cp silverback_core/*.* silverback_deployment/``
``$ cp locality_sensitivy_hashing/*.* silverback_deployment/``
``$ cp silverback_twitter_module/*.* silverback_deployment/ #(or facebook_module)``
``$ #then create a config.py in silverback_deployment/``

Good packages for minHash
* https://github.com/embr/lsh
* https://github.com/go2starr/lshhdc
* https://github.com/rahularora/MinHash

MuSES
=====

[MuSES](https://github.com/yvesx/muses): Multilingual Sentiment Elicitation System for Social Media Data


MuSES consists of three different sentiment identification algorithms. Our first algorithm augments previous compositional semantic rules by adding social media-specific rules. In the second algorithm, we define a scoring function that measures the degree of a sentiment, instead of simply classifying a sentiment into binary polarities. All such scores are calculated based on a large volume of customer reviews. Due to the special characteristics of social media texts, we propose a third algorithm, which takes emoticons, negation word position, and domain-specific words into account. In addition, we propose a label-free process to transfer multilingual sentiment knowledge between different languages. We conduct our experiments on user comments from Facebook, tweets from Twitter, and multilingual product reviews from Amazon.


* Publication ``IEEE Intelligent Systems Magazine`` Yusheng Xie, Zhengzhang Chen, Yu Cheng, Kunpeng Zhang, Daniel K. Honbo, Ankit Agrawal, Wei-keng Liao, and Alok Choudhary. *MuSES: a Multilingual Sentiment Elicitation System for Social Media Data*

Main Challenges
---------------

* The web is multilingual. A recent study  shows that more than 50% of the conversions on Facebook are non-English; yet most of the infrastructural works on sentiment analysis (e.g., NLTK, WordNet) focus primarily on English.
* Labeling process for a "new" language can be really expensive.
* Unlike traditional documents such as Newspaper articles, Internet languages possess a lot of quirky traits such as the lack of strict grammar, heavy usage of emoticons, etc.
* Massive amount of new tweets, comments, blogs pose a serious engineering challenge.

* Overall Architecture

![alt tag](https://raw.github.com/yvesx/projects/master/muses_imgs/a.png)


Language Detection
------------------

* [LingPipe](http://alias-i.com/lingpipe/)
* [``guess_language``](https://bitbucket.org/spirit/guess_language/)
* [``guess-language``](https://pypi.python.org/pypi/guess-language)
* [``guess-language``](https://github.com/dsc/guess-language)
* Languages on Facebook

![alt tag](https://raw.github.com/yvesx/projects/master/muses_imgs/0.png)


Multilingual Label System (MLLS)
--------------------------------

* A novel zero-effort labeling system that leverages knowledge bases like Wikipedia, and labels word-level sentiment for non-English words.

![alt tag](https://raw.github.com/yvesx/projects/master/muses_imgs/1.png)

3 Individual Algorithms
-----------------------

* Compositional Semantic Rule Algorithm

![alt tag](https://raw.github.com/yvesx/projects/master/muses_imgs/2.png)
![alt tag](https://raw.github.com/yvesx/projects/master/muses_imgs/5.png)

* Numeric Sentiment Identification Algorithm
 * How to associate numeric scores with the degree of textual sentiment;
 * If we assign a score to each word/phrase, how to combine all the scores of multiple words for a sentence.

![alt tag](https://raw.github.com/yvesx/projects/master/muses_imgs/3.png)

![alt tag](https://raw.github.com/yvesx/projects/master/muses_imgs/4.png)

* Bag-of-Words and Rule-based Algorithm
 * Due to the special characteristics of social media texts, we define some domain rules to analyze sentiments. What people write on Facebook or Twitter is different in style from traditional product reviews or blog articles. Social media texts are often short and contain Internet idioms, etc.

![alt tag](https://raw.github.com/yvesx/projects/master/muses_imgs/6.png)

![alt tag](https://raw.github.com/yvesx/projects/master/muses_imgs/7.png)

Evaluation
----------

* To unify the independent results from the three individual algorithms, MuSES employs high-level meta-learning techniques. Decision tree (DT), neural networks (NN), random forest model (RF), and logistic regression (LR) are used as our sentimental classification models. Five discriminative features are considered by these models. These features include 3 basic ones and 2 derived ones:
 * S1, integer output from compositional semantic rules;
 * S2, float output from the numeric sentimental identification algorithm;
 * S3, output from the back-of-word and rule-based algoithm (``P``, ``N``, or ``O``);
 * S1+S2; and
 * S1−S2.

![alt tag](https://raw.github.com/yvesx/projects/master/muses_imgs/8.png)


Acknowledgements
----------------

[Datasets](http://cucis.ece.northwestern.edu/projects/Social/) originally prepared by @ych133

Collaborators: @miccrun @kpzhang @ych133 @liuhaotian @honbo @palsetia @alokchoudhary


Macro Behavioral Targeting
==========================

[project link](https://github.com/yvesx/MacroBehavioralTargeting) We investigate a class of emerging online marketing challenges in social networks; macro behavioral targeting (MBT) is introduced as non-personalized broadcasting efforts to massive populations. We propose a new probabilistic graphical model for MBT. Further, a linear-time approximation method is proposed to circumvent an intractable parametric representation of user behaviors. We compare the proposed model with the existing state-of-the-art method on real datasets from social networks. Our model outperforms in all categories by comfortable margins.

Publication:
* ``13th SIAM Data Mining 2013`` Yusheng Xie, Zhengzhang Chen, Kunpeng Zhang, Md. Mostofa Ali Patwary, Yu Cheng, Haotian Liu, Ankit Agrawal, and Alok Choudhary. *Graphical Modeling of Macro Behavioral Targeting in Social Networks*
* A version has been sent to a top Marketing journal for review.

Audience & Problem
------------------

* **Target audience:** Brand and social media marketers and researchers
* **Problem:** Marketers spend millions every month to acquire Facebook fans
 * *We spent $30M and acquired 20M FB fans. Now what?* – a major US retailer
* **Research question:** How to optimally engage one’s fans so that they stay active and retain their value to the brand?
* FB user => **Fan => Engaged Fan** => Customer

Methodology
-----------

* Facebook Engagement Model
![alt tag](https://raw.github.com/yvesx/projects/master/mbt_imgs/1.png)
![alt tag](https://raw.github.com/yvesx/projects/master/mbt_imgs/2.png)
* Three major components in MBT model
![alt tag](https://raw.github.com/yvesx/projects/master/mbt_imgs/3.png)
* User parametrization
![alt tag](https://raw.github.com/yvesx/projects/master/mbt_imgs/4.png)
* Features
![alt tag](https://raw.github.com/yvesx/projects/master/mbt_imgs/5.png)
![alt tag](https://raw.github.com/yvesx/projects/master/mbt_imgs/6.png)
![alt tag](https://raw.github.com/yvesx/projects/master/mbt_imgs/7.png)
![alt tag](https://raw.github.com/yvesx/projects/master/mbt_imgs/viz.png)

Data & Experiments
------------------

![alt tag](https://raw.github.com/yvesx/projects/master/mbt_imgs/10.png)
* Prediction performance
![alt tag](https://raw.github.com/yvesx/projects/master/mbt_imgs/11.png)
* Optimization terms
![alt tag](https://raw.github.com/yvesx/projects/master/mbt_imgs/12.png)

CRF & Active Learning to Improve Sentiment Identification
=========================================================

[project link](https://github.com/yvesx/CRF_sentiment)

Incorporating Conditional Random Fields (CRF) and Active Learning to Improve Sentiment Identification

Many machine learning, statistical, and computational linguistic methods have been developed to identify sentiment in sentences in documents, yielding promising results. However, most of the current state-of-the-art methods focus on individual sentences and ignore the impact of context on the meaning of a sentence. In this paper, we propose a method based on conditional random fields to incorporate sentence structure and context information in addition to syntactic information. We also investigate how human interaction affects the accuracy of sentiment labeling using limited training data. We propose and evaluate two different active learning strategies for labeling sentiment data.

* Publication ``35th ACM SIGIR 2012`` Kunpeng Zhang, Yusheng Xie, Yu Cheng, Doug Downey, Ankit Agrawal, Wei-keng Liao, and Alok Choudhary. *Sentiment Identification by Incorporating Syntactics, Semantics and Context Information* 

* Publication ``under journal review`` Incorporating Conditional Random Fields and Active Learning to Improve Sentiment Identification

Main Challenges
---------------

* How to take full advantage of the sentence structure;
* How to use  context information to capture the relationship among sentences and to improve document-level sentiment classification;
* How to account for Internet language word set and emoticons;
* How to incorporate human interaction to improve sentiment identification accuracy and construct a large training dataset.

Why CRF Model
-------------

* We want to capture the context information (e.g., neighboring sentences or sentences connected by transition words) among sentences in a document. The procedure of sentiment identification therefore becomes a kind of sequence labeling. 

* The goal of the model is to give a label to each sentence corresponding to the sentence sequence. We use CRF as a tool to model this sequence labeling problem.

* ![alt tag](https://raw.github.com/yvesx/projects/master/crf_imgs/1.png)

* ![alt tag](https://raw.github.com/yvesx/projects/master/crf_imgs/2.png)

Semantic Features
-----------------

* Number of Positive/Negative Words 
* Containing Any Positive/Negative Emoticons
* Comparative Sentences (JJR vs RBR vs JJS vs RBS)
* Type of Conjunction Words (IN vs CC)

Syntactic Features
------------------

* Sentence Position in Paragraph
* Sentence/clause Complexity
* Position of Positive/Negative Words
* Position of Negation Words
* Comparison Subject
* Similarity to Neighboring Sentences
 * Levenshtein
 * LSI-Levenshtein

Evaluation
----------

* ![alt tag](https://raw.github.com/yvesx/projects/master/crf_imgs/3.png)
* ![alt tag](https://raw.github.com/yvesx/projects/master/crf_imgs/4.png)


How It Works
------------

* ``python ./prepare.py`` check the parameters, paths, etc.
* ``python ./generate_template.py`` if necessary.
* ``bash ./run_crf.sh`` modify ``run_crf.sh`` if necessary.


Acknowledgements
----------------

* [Dataset](https://raw.github.com/yvesx/CRF_sentiment/master/data/CRF_long_data.xlsx) contains long, complicated sentences from [Stanford](http://nlp.stanford.edu/sentiment/index.html) & [Northwestern](http://cucis.ece.northwestern.edu/projects/Social/).
* [CRF++](http://crfpp.googlecode.com/svn/trunk/doc/index.html) is a great tool.

Collaborators: @kpzhang @hixiaoxi



Sensitivity
===========

[project link](https://github.com/yvesx/Sensitivity)

Recommendation systems automatically recommend relevant items to users based on their preferences, which are vital to the success of online retailers and content providers. Collaborative filtering works well in practice at web scale. However, one common difficulty in collaborative filtering rec- ommendation systems is the "cold start" problem. The word "cold" refers to the items that are not yet rated by any user or the users who have not yet rated any items. We propose ELVER, an algorithm for recommending cold items from large, sparse user-item matrices. We use ELVER to recommend and optimize page-interest targeting on Facebook. Special traits of a social network like Facebook have influenced the design of ELVER. Existing techniques for cold recommendation mostly rely on content features in the event of lacking user ratings. Traditional items (e.g., movies or music) have rich, organized content features like actors, directors, awards, etc. Since it is very hard to construct universally meaningful features for the millions of Facebook pages, ELVER makes minimal assumption of content features.

``2013 IEEE International Conference on Big Data`` Yusheng Xie, Zhengzhang Chen, Kunpeng Zhang, Yu Cheng, Chen Jin, Ankit Agrawal, and Alok Choudhary. *Elver: Recommending Facebook Pages in Cold Start Situation Without Content Features*


Background
----------

* Recommending traditional items and social entities
![alt tag](https://raw.github.com/yvesx/projects/master/sensitivity_imgs/1.png)
![alt tag](https://raw.github.com/yvesx/projects/master/sensitivity_imgs/2.png)
* Collaborative Filtering Algorithm
![alt tag](https://raw.github.com/yvesx/projects/master/sensitivity_imgs/3.png)

The Problem
-----------

* The cold item situation: items do not have enough user ratings.
![alt tag](https://raw.github.com/yvesx/projects/master/sensitivity_imgs/4.png)
![alt tag](https://raw.github.com/yvesx/projects/master/sensitivity_imgs/5.png)
![alt tag](https://raw.github.com/yvesx/projects/master/sensitivity_imgs/6.png)
* Limitations of Collaborative Filtering
![alt tag](https://raw.github.com/yvesx/projects/master/sensitivity_imgs/7.png)
![alt tag](https://raw.github.com/yvesx/projects/master/sensitivity_imgs/8.png)
* The proposed framework and components
![alt tag](https://raw.github.com/yvesx/projects/master/sensitivity_imgs/9.png)
![alt tag](https://raw.github.com/yvesx/projects/master/sensitivity_imgs/10.png)
* An iterative algorithm (stochastic Expectation-Maximization algorithm)
![alt tag](https://raw.github.com/yvesx/projects/master/sensitivity_imgs/11.png)

Evaluation
----------
* Convergence of the algorithm
![alt tag](https://raw.github.com/yvesx/projects/master/sensitivity_imgs/12.png)
* Matrix-wise recommendation mean square errors.
![alt tag](https://raw.github.com/yvesx/projects/master/sensitivity_imgs/13.png)

