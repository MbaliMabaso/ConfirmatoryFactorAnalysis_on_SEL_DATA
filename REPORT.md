###Confirmatory Factor Analysis (CFA) on SEL Data 
---

##Introduction
---

This report showcases the application of Confirmatory Factor Analysis (CFA) to Social and Emotional Learning (SEL) data. This project evaluates the factor structure
of SEL-related constructs using Python (semopy) and assesses model adequacy through goodness-of-fit indices.

Two CFA models were tested:
Model 1: A five-factor SEL structure based on theoretical constructs.
Self Awareness =~ I_say_sorry + Easy_talk_feelings + Teachers_lie 
Self Regulation =~ Good_at_lining_up + Others_make_fight + Teachers_disturbing_class + Feel_sad + Feel_worried 
Social awareness =~ Like_listen_ideas + Understand_others + Help_sad_people
Relationship skills =~ One_good_friend + Peers_like_me + Peers_say_kind 
Responsible Decisions =~ Follow_rules_alone + Homework_on_time + Think_before_act + Study_before_test

MODEL 2: A refined four-factor model aimed at improving model fit.
Self Regulation =~ Good_at_lining_up + Others_make_fight + Teachers_disturbing_class + Feel_sad + Feel_worried 
Social awareness =~ Like_listen_ideas + Understand_others + Help_sad_people
Relationship skills =~ One_good_friend + Peers_like_me + Peers_say_kind
Responsible Decisions =~ Follow_rules_alone + Homework_on_time + Think_before_act + Study_before_test

This report presents a comparison of both models, interpretations of results, and recommendations for further improvement.

##Pre-Analysis Data Preparation
---
1. Checking for Missing Data:
There was no missing data.

2. Removing Meaningless Variables:
Excluded non-relevant variables such as participant IDs unrelated to the CFA model.
Focused only on observed SEL-related indicators.

3. Checking Correlations and Variance Inflation Factor (VIF):
Evaluated multicollinearity among observed variables.
All items had extremely high VIFs. To practice CFA using Python, I continued with the CFA analysis anyway and provided
suggestions to improve model fit.

Checking Univariate and Multivariate Normality:

Used Shapiro-Wilk tests and skewness/kurtosis values to examine normality.

Assessed multivariate normality via Mardia’s test.

Cronbach’s Alpha for Internal Consistency:

Computed Cronbach’s Alpha for each latent factor to check internal consistency.

Ensured that all factors had acceptable reliability (α > 0.7) before conducting CFA.


