# internet-use: A Data Science Project for Predicting Internet Use

Kaggle competition for the [Child Mind Institute - Problematic Internet Use](https://www.kaggle.com/competitions/child-mind-institute-problematic-internet-use/overviewhttps://www.kaggle.com/competitions/child-mind-institute-problematic-internet-use/overview).

## Personal Objectives
- Build more experience with existing frameworks like [Apache Spark](https://spark.apache.org/) and [PyTorch](https://pytorch.org/).

## Workflow + Stack

### Exploratory Data Analysis

First and foremost, for any data science project, it is crucial to understand two components: 1) the data and 2) the problem at hand. 
The first is the "data" of data science while the second is the "science."
As such, I will document my observations here as I work through the project.
I will then remodularize my `README.md` file so other can follow through my logic for this project!

**One Sentence Objective**: predict a participant's severity impairment index `sii` from two categories of data: physical activity data (which, for discussion, I call `phys_data`) and internet usage behavior data (which I call `iuse_data`). 

**Challenges**
- The target `sii` is missing for a portion of individuals in the training-set. Need to apply some form of non-supervised learning/imputation. In fact, a majority of entries are missing for the training-set. 
- There are two distinct datasets, where one is a time series while the other is time-invariant. Need a way to reasonable combine these datasets. Also, the transformations are unclear + feature engineering necessary to design such a model is unclear. 

##### First Iteration

I believe before working on any data science project, its operatant to look at the variables and make some claims/hypotheses based on my 22 years of existence on this fine planet. Then, I can double-check my intuition through data analysis and iterate with more hypotheses. The end goal of this process is to develop a strong intuition when working with this data, as eventually I need a model that I think would best be suited for this problem. 

Thus, here are my first round of hypotheses:
- Claim 1: There should be a negative correlation between outside physical activity and internet usage. 
The intuition is that if a child spends more time doing something else, they have less time for the internet. 
- Claim 2: Likewise, sleep quality should be inversely related with internet usage. This seems terrible to cite, but I heard (through some little bird) that late-night and early-morning internet-usage drastically affects an individual's quality of sleep. 
Clearly, a child is an individual so this seems fair to assume. 
- Claim 3: 
- Claim 4: 
- Claim 5: 

When exploring the data, I first decided to stratify the `iuse_data` by the different `sii` scores (an ordinal discrete variable ranging from `0` to `3` with increasing severity) to get the `id`'s of children into mutually exclusive buckets. 

From there, I can analyze the `phys_data` within these groups to see if there are any jarring differences between the different `sii` classes. 


