---Conducting Confirmatory Factor Analysis (CFA) on SEL Data
---

##Overview
This repository contains an analysis of Confirmatory Factor Analysis (CFA) conducted on Social and Emotional Learning (SEL) data. The goal was to evaluate the factor
structure of SEL-related constructs and assess how well the observed variables represent the underlying latent variables.
Two CFA models were tested:
- Model 1: A five-factor structure based on theoretical constructs.
- Model 2: A refined four-factor model aimed at improving model fit.
This project demonstrates the process of performing CFA using Python (semopy) and interprets key goodness-of-fit indices to assess model adequacy.

##Data and Variables
---
#Latent Variables and Observed Indicators

MODEL 1: 5 factor structure
Self Awareness =~ I_say_sorry + Easy_talk_feelings + Teachers_lie
Self Regulation =~ Good_at_lining_up + Others_make_fight + Teachers_disturbing_class + Feel_sad + Feel_worried
social awareness =~ Like_listen_ideas + Understand_others + Help_sad_people
relationship skills =~ One_good_friend + Peers_like_me + Peers_say_kind
Responsible Decisions =~ Follow_rules_alone + Homework_on_time + Think_before_act + Study_before_test

MODEL 2: 4 factor structure
Self Regulation =~ Good_at_lining_up + Others_make_fight + Teachers_disturbing_class + Feel_sad + Feel_worried
social awareness =~ Like_listen_ideas + Understand_others + Help_sad_people
relationship skills =~ One_good_friend + Peers_like_me + Peers_say_kind
Responsible Decisions =~ Follow_rules_alone + Homework_on_time + Think_before_act + Study_before_test


--Self Awareness: Measures students' ability to recognize emotions and express themselves.

--Self Regulation: Examines emotional control and behavioral regulation.

--Social Social Awareness: Assesses students' empathy and understanding of others.

--Relationship Skills: Evaluates the ability to form and maintain relationships.

--Responsible Decisions: Measures decision-making and problem-solving skills.

#Removed variables
Respect culture was removed from the latent variable social awareness as it had a factor loading <.3
Feel sad and Feel worried were removed from the latent variable self-regulation because their factor loadings had insignificant p-values.
The SelfAwareness factor was removed due to poor fit in Model 1.
The structure was adjusted to test if model performance improved with fewer factors.

##Results and comparisons
image alt](URL)

Model 1 fit summary
Model 1 did not fit well. The CFI and TLI were below the recommended 0.90, and the RMSEA exceeded the acceptable threshold (0.08). The significant chi-square test also indicated a poor fit.

model 2 fit summary
Model 2 showed a notable improvement:
Chi-square reduced significantly (from 289.63 to 89.38), though still significant.
CFI increased to 0.91, surpassing the 0.90 threshold for acceptable fit.
TLI improved to 0.882, closer to the recommended >0.90.
RMSEA decreased to 0.07, now within the acceptable range (<0.08).


##Conclusion
Although model 2 has improved, the TLI is still below the ideal threshold and should be improved, and the VIF scores were very high (range from 19.39 to 76.81), suggesting severe multicollinearity which means that some items may be measuring the same underlying concept, rather than distinct constructs.
image alt](URL)

Suggestions:
-Identify and remove highly redundant items that might be measuring the same aspect of a latent variable.
-Conduct Exploratory Factor Analysis (EFA) to see if some items load onto multiple factors or if they cluster too closely. 
-Re-evaluate factor structure: Some items might fit better under a different latent variable than originally hypothesized.
-Modify the model by removing problematic items and testing whether the fit indices improve.






