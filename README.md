# Detecting Distinctive Features of Dispatched Employees with Machine Learning

 [![License: GPL v3](https://img.shields.io/badge/License-GPL%20v3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0) 

## 1. Introduction

This project aims at detecting the factors that distinguish dispatched employees from regular employees with classification and clustering algorithms.



## 2. Data

> China Family Panel Studies (CFPS) is a nationally representative, annual longitudinal survey of Chinese communities, families, and individuals launched in 2010 by the Institute of Social Science Survey (ISSS) of Peking University, China. The CFPS is designed to collect individual-, family-, and community-level longitudinal data in contemporary China. The studies focus on the economic, as well as the non-economic, wellbeing of the Chinese population, with a wealth of information covering such topics as economic activities, education outcomes, family dynamics and relationships, migration, and health. The CFPS is funded by the Chinese government through Peking University. The CFPS promises to provide to the academic community the most comprehensive and highest-quality survey data on contemporary China. Three key features of the CFPS are worth noting here:
>
> 1. All members over age 9 in a sampled household are interviewed. These individuals constitute core members of the CFPS.
>
> 2. As in the PSID, children of the CFPS are also considered core members of the CFPS. Theoretically, a core member can leave the study only through death.
>
> 3. Follow-up of all core members of the CFPS is designed to take place on a yearly basis. Five provinces are chosen for initial oversampling (1600 families in each) so that regional comparisons can be made. The remainder of the CFPS sample (8000 families) is drawn from the other provinces so as to make the overall CFPS sample representative of the country through weighting (except for remote areas, noted later).
>
> In the 2010 baseline survey, the CFPS successfully interviewed almost 15,000 families and almost 30,000 individuals within these families, for an approximately response rate of 79%. The CFPS respondents are tracked through annual follow-up surveys.



Data set: Chinese Family Panel Studies (Baseline) 2018

Citation: The data are from China Family Panel Studies (CFPS), funded by 985 Program of Peking University and carried out by the Institute of Social Science Survey of Peking University



## 3. Project Timeline

- Prepared for: Hanqian Zhang, 张含谦
- Prepared by: Kunyu He, 贺鲲羽

October 27th, 2019

Project length: 2 months



### Week 1

*Oct. 28 to Nov. 1*

- [x] Introduced each other and discussed about interests in research topics
- [x] Decided on the research subject: Dispatched Employees (*here after: DE*)
- [x] Outlined potential datasets to be used, including CFPS datasets and USA government-published employment data



### Week 2

*Nov. 4 to 8*

- [x] Decided on using CFPS datasets for the study

- [x] Decided on the research topic: what features distinguishes *DE* from Regular Employees  (*here after: RE*)

- [x] Started to look at CFPS 2018 cross-sectional data, define relevant variables (*`qg502` labeling whether the subject is a DE*)

  > Output: CFPS Relevant Features and Hypothesis.doc, [link](https://github.com/tzhanqian/dispatchedworkersCFPS/blob/master/data/Relevant%20Features%20and%20Research%20Hypothesis.docx)

- [x] Checked the differences in summary statistics (*mean, median*) of relevant variables across DE and RE to see if there are significance

  > Output: 20191102-Preliminary-Prep.Rmd, [link](https://github.com/tzhanqian/dispatchedworkersCFPS/blob/master/notebooks/EDA/20191102%20Preliminary%20Prep.Rmd)



### Week 3

*Nov. 11 to 15*

- [x] Started to work on data cleaning, produced first version of cleaned dataset

  > Output: employment2018.csv, [link](https://github.com/tzhanqian/dispatchedworkersCFPS/blob/master/data/employment2018.csv)

- [x] Continued to work on exploratory data analysis (*here after: EDA*) to further check how certain categorical variables differ across DE and RE:

  - Used conditional probability to quantify the empirical probability of belonging to DE given belonging to certain category (*exp. given unsatisfied of social equality, how likely the subject belongs to DE*)
  - Used box plots to visualize the difference in sample distribution of continuous variables across DE and RE groups

  > Output: 20191112-Data-Cleaning-Box-Plots-Conditional-Prob.Rmd, [link](https://github.com/tzhanqian/dispatchedworkersCFPS/blob/master/notebooks/EDA/20191112%20Data%20Cleaning-Box%20Plots-Conditional%20Prob.Rmd)

- [x] Introduced to classification and feature selection methods, namely, `Logistic Regression`, `Lasso Regression` and `Ridge Regression`

- [x] Introduce to statistics approaches of checking univariate hypothesis:

  - Continuous and categorical: `ANOVA`, `Intra-class Correlation`
  - Categorical and categorical: `Chi-squared Test`, `Cramer's V`

- [x] Introduced to the typical steps of data preprocessing



### Week 4

*Nov. 18 to 22*

- [x] Apply statistics approaches to check univariate hypothesis:
  - Check if the continuous variable is different across DE and RE significantly with `ANOVA` and test the strength of such association with `intra-class correlation`
  - Check if the categorical variable is significantly different across DE and RE with `chi-squared test`, test the strength of such association with `Cramer's V`
- [x] Synthesize a codebook of relevant variables
- [x] Finish data preprocessing for classification
- [ ] Illustrate working knowledge of `Logistic Regression`, `Lasso`, and `Ridge` with implementation in R
- [ ] Apply L`Logistic Regression`, `Lasso Regression` and `Ridge Regression`
