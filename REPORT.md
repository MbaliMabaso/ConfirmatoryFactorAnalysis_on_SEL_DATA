###Confirmatory Factor Analysis (CFA) on SEL Data 
---

##Introduction
---

This report showcases the application of Confirmatory Factor Analysis (CFA) to Social and Emotional Learning (SEL) data. This project evaluates the factor structure
of SEL-related constructs using Python (semopy) and assesses model adequacy through goodness-of-fit indices.

Two CFA models were tested:
MODEL 1: A five-factor SEL structure based on theoretical constructs.

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
The items were also removed as survey administrators informed me that students thought
these questions were unclear : Know_not_good_at, Like_talk_front, Prefer_grownups.

4. Checking Correlations and Variance Inflation Factor (VIF):
Evaluated multicollinearity among observed variables.
All items had extremely high VIFs. To practice CFA using Python, I continued with the CFA analysis anyway and provided
suggestions to improve model fit.
(nsert image here)

5. Checking Multivariate Normality and Univariate Normality:
Assessed multivariate normality via Mardia’s test.
Used Shapiro-Wilk tests and skewness/kurtosis values to examine normality in all survey items.
Both tests were significant (p = <.05), indicating non-normality of data. Therefore, Robust Maximum Likelihood (MLR) was used.

6. Cronbach’s Alpha for Internal Consistency:
   
Computed Cronbach’s Alpha for each latent factor to check internal consistency.

-Cronbach alpha for self awareness (I_say_sorry, Easy_talk_feelings, Teachers_lie) is .425, which is not good reliability.

-Cronbach alpha for self regulation (Good_at_lining_up, Others_make_fight, Teachers_disturbing_class,Feel_sad,Feel_worried)
is .617. However, since Feel_sad and Feel_worried were later found to have insignificant factor loading, they were removed
from the model and the recalculated Cronbach alpha was .650, which is still acceptable.

-Cronbach alpha for social awareness (Like_listen_ideas, Respect_cultures, Understand_others, Help_sad_people) was .662.
However, since Respect_cultures had a very low factor loading, it was removed from the model the recalculated Cronbach alpha was .712, which is very good.

-Cronbach alpha for relationship skills (One_good_friend, Peers_like_me, Peers_say_kind) was .726, which is very good.

-Cronbach alpha for responsible decision making (Follow_rules_alone, Homework_on_time, Think_before_act, Study_before_test) was .658, which is acceptable.
Cronbach alpha summary

##Methodology
---
MODEL 1: A five-factor SEL structure based on theoretical constructs.

1.Self Awareness =~ I_say_sorry + Easy_talk_feelings + Teachers_lie 

2.Self Regulation =~ Good_at_lining_up + Others_make_fight + Teachers_disturbing_class + Feel_sad + Feel_worried 

3.Social awareness =~ Like_listen_ideas + Understand_others + Help_sad_people

4.Relationship skills =~ One_good_friend + Peers_like_me + Peers_say_kind 

5.Responsible Decisions =~ Follow_rules_alone + Homework_on_time + Think_before_act + Study_before_test

MODEL 2: A refined four-factor model aimed at improving model fit.

1.Self Regulation =~ Good_at_lining_up + Others_make_fight + Teachers_disturbing_class 

2.Social awareness =~ Like_listen_ideas + Understand_others + Help_sad_people

3.Relationship skills =~ One_good_friend + Peers_like_me + Peers_say_kind

4.Responsible Decisions =~ Follow_rules_alone + Homework_on_time + Think_before_act + Study_before_test

Model 2 was refined by removing Self Awareness, which did not perform well in Model 1. Moreover, it made sense to remove 
Self Awareness due to its low Cronbach alpha (.425).

##Results and Model Fit Comparison
---
Model Fit Summary

image

Model 1 did not fit well, with CFI and TLI below the recommended 0.90 and RMSEA above the acceptable threshold (<0.08). 
The significant chi-square also indicates poor fit.

Model 2 shows a significant improvement:
Chi-square decreased from 289.63 to 89.38, though still significant.
CFI increased to 0.91, surpassing the 0.90 threshold for acceptable fit.
TLI improved to 0.882, approaching the recommended >0.90.
RMSEA decreased to 0.07, now within acceptable limits (<0.08).

Model 2, while not perfect, provides a substantial improvement over Model 1.

##Recommendations for Model Improvement
---
1. Address Multicollinearity:
High VIF scores (19.39 - 76.81) indicate strong correlations between some items.
Removing redundant items that might be measuring the same aspect of a latent variable can enhance model validity.
2. Refine Item Selection:
Perform Exploratory Factor Analysis (EFA) to check if certain items load onto multiple factors. Perhaps certain
items should be reclassified as they might fit better under a different latent variable than originally
hypothesized. Some items may need to be removed altogether. 
3. Investigate Alternative Model Structures:
Further refinements in factor structure may yield better model performance. Testing additional models can identify the most reliable and valid measurement approach.
4. Increase Sample Size:
Chi-square tests are sensitive to sample size; larger datasets may improve model estimation accuracy.

##Technologies Used
---
Python (semopy, pandas, matplotlib)
Confirmatory Factor Analysis (CFA)
Model Fit Evaluation (CFI, TLI, RMSEA, Chi-Square)
Data Visualization

##Key Takeaways for My Data Science Portfolio
---
✅ Demonstrated expertise in structural equation modeling (SEM) using Python.
✅ Applied confirmatory factor analysis (CFA) for psychometric research.
✅ Conducted model fit evaluation using industry-standard indices.
✅ Provided data-driven recommendations to improve model performance.

##Conclusion
---
This CFA study on SEL data compared two models and found that Model 2 outperforms Model 1 based on goodness-of-fit indices. However, further improvements are still needed to address multicollinearity and refine factor loadings.

This project demonstrates my ability to conduct advanced statistical modeling, evaluate psychometric constructs, and make data-driven improvements—essential skills in data science and educational research.

##Next Steps:
---
Conduct CFA to refine item selection.
Explore alternative CFA models for enhanced factor structure.
Apply machine learning techniques to predict SEL outcomes.

##Author
---
[Mbali Mabaso]Data Scientist | Data Analyst[[[LinkedIn](https://www.linkedin.com/jobs/view/4106488511/)]

