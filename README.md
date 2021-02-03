# Crash Severity Analysis in the USA in 2018


### Triet M. Nguyen & Trang M. Nguyen & Tri M. Nguyen & Tri H.M Vang
This is the project that we finished after the 6th week of studying **Big Data for Engineering (EEET2574)**.




## INTRODUCTION

### 1. CRSS and FARS dataset

FARS (2018) (https://www.nhtsa.gov/crash-data-systems/fatality-analysis-reporting-system) is a stratified sample of police-reported crashes involving different traffic participants, ranging from property-damage-only crashes to those involving fatalities. CRSS samples are collected from 6 million law enforcement agency reports each year.


CRSS (2018) (https://www.nhtsa.gov/crash-data-systems/crash-report-sampling-system) is a census of all fatal road incidents in the United States, grouped by state. FARS data, as well as CRSS data, are sourced from the U.S federal government under the same agency. To qualify as a FARS case, each entry must result in at least one death within 30 days since the date of crash.


### 2. Project goals
1. Evaluate factors contributing to an accident, and predict (binary) the injury severity of a person in that accident (CRSS)
2. Evaluate factors contributing to fatality alone, and predict (multiclass) the fatal injury severity based on delay from time of crash to time of death (FARS)
 
