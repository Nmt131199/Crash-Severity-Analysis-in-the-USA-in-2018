# Crash Severity Analysis in the USA in 2018


### Triet M. Nguyen & Trang M. Nguyen & Tri M. Nguyen & Tri H.M Vang
This is the project that we finished after the 13th week of studying **Big Data for Engineering (EEET2574)**.




## INTRODUCTION

### 1. CRSS and FARS dataset

FARS (2018) (https://www.nhtsa.gov/crash-data-systems/fatality-analysis-reporting-system) is a stratified sample of police-reported crashes involving different traffic participants, ranging from property-damage-only crashes to those involving fatalities. CRSS samples are collected from 6 million law enforcement agency reports each year.


CRSS (2018) (https://www.nhtsa.gov/crash-data-systems/crash-report-sampling-system) is a census of all fatal road incidents in the United States, grouped by state. FARS data, as well as CRSS data, are sourced from the U.S federal government under the same agency. To qualify as a FARS case, each entry must result in at least one death within 30 days since the date of crash.


### 2. Project goals
1. Evaluate factors contributing to an accident, and predict (binary) the injury severity of a person in that accident (CRSS)
2. Evaluate factors contributing to fatality alone, and predict (multiclass) the fatal injury severity based on delay from time of crash to time of death (FARS)
 

## MODEL PERFORMANCE AND ACCURACY
1. For CRSS (binary prediction)

| Models | Additional conditions | Accuracy |
| --- | --- | --- |
| Decision Tree (using K-Fold splitting method) |`criterion = 'entropy'; max_dept = 5`  | 0.72502 |
| Decision Tree | `criterion = 'gini'; max_dept = 5`  | 0.72455 |
| Decision Tree |`criterion = 'gini'; max_dept = none`   | 0.66 |
| Decision Tree |`criterion = 'entropy'; max_dept = 5`   | 0.73 |
| Random Forest | default | 0.77 |
| KNN | `k=30` | 0.76 |
| Multinomial Gaussian Naive Bayes | default | 0.7 |

1. For FARS (multiclass prediction with 6 outputs)


| Models | Additional conditions | Accuracy | Accuracy (after Feature selection) |
| --- | --- | --- | --- |
| Decision Tree | default | 0.589 | 0.326 |
| Random Forest | default | 0.77 | 0.429 |
| KNN | default | 0.283 | 0.302 |
| SVM | default | 0.292 | 0.372
| Bagging | default | 0.596 | 0.436 |
| Extra Trees | default | 0.57| 0.417 |

### CONCLUSION
At the end of the project, what we had accomplished were two working models that satisfy the business objectives we set out initially, which are two Decision Tree Classifiers with a respective accuracy 73% (> 65%) for binary classification and 42% (> 30%) for 6-class multiclass prediction.

However, there were some noticeable drawbacks during our data mining process that reduced the quality of our outcome. Firstly, although the models’ accuracy surpassed our expectation, their performance could potentially be improved much higher if we select better attributes and experiment with more models. 

Secondly, it could be the datasets we chose primarily were not sufficient to achieve better performance. Overall, the data mining process of our team was quite
constructive, especially in the second stage where we iterated the cycle twice so as to constantly improve the performance of the model by implementing different techniques and algorithms.
