# phase3project
![photo](https://github.com/mbuvenzuve/phase3project/blob/main/shutterstock_1680091963-1024x683.jpg)

## Overview
This project focuses on analyzing H1N1 and seasonal flu vaccine uptake patterns during the 2009 pandemic, considering respondents' backgrounds, opinions, and health behaviors. The U.S. survey from late 2009 to early 2010 captured data on social, economic, and demographic factors, alongside perceptions of illness risks and vaccine effectiveness. 

By examining this dataset, the goal is to uncover insights into the factors shaping individual vaccination choices, providing valuable knowledge for future public health efforts. The competition offers an accessible opportunity for participants of all levels to engage in data science and contribute to understanding vaccination patterns during a crucial public health event.

##Business Understanding
This project is crucial for public health authorities, healthcare providers, and policymakers. It impacts individuals and communities, especially those susceptible to influenza, as the predictions can guide targeted vaccination campaigns and health interventions. The primary business problem addressed is predicting the likelihood of individuals getting H1N1 and seasonal flu vaccines based on their backgrounds, opinions, and health behaviors. By understanding these patterns, health organizations can optimize vaccine distribution, communication strategies, and public health campaigns. This project focuses specifically on predicting vaccine uptake. It does not address the production, distribution, or manufacturing challenges associated with vaccines.

## Data Understanding
Two datasets are available from Data-Driven. The first dataset contains information on H1N1 vaccine features, and the second dataset indicates patients who have taken either the H1N1 vaccine or the seasonal flu vaccine. Data-Driven controls the data sources. The target is to predict the likelihood of individuals getting H1N1 and seasonal flu vaccines based on their backgrounds, opinions, and health behaviors. Our Predictors include various demographic, behavioral, and opinion-related features, such as h1n1_concern, h1n1_knowledge, behavioral_antiviral_meds, etc. The predictors include both numerical (float64, int64) and categorical (object) data types. The distribution of the data includes information on 26,707 respondents with 38 features. With over 26,000 observations, we have a sufficient amount of data to build predictive models without the need for resampling methods.

## Features in this data set
h1n1_concern - Level of concern about the H1N1 flu.

0 = Not at all concerned; 1 = Not very concerned; 2 = Somewhat concerned; 3 = Very concerned.

h1n1_knowledge - Level of knowledge about H1N1 flu.

0 = No knowledge; 1 = A little knowledge; 2 = A lot of knowledge.

behavioral_antiviral_meds - Has taken antiviral medications. 

behavioral_avoidance - Has avoided close contact with others with flu-like symptoms.

behavioral_face_mask - Has bought a face mask.

behavioral_wash_hands - Has frequently washed hands or used hand sanitizer. 

behavioral_large_gatherings - Has reduced time at large gatherings. 

behavioral_outside_home - Has reduced contact with people outside of own household. 

behavioral_touch_face - Has avoided touching eyes, nose, or mouth.

doctor_recc_h1n1 - H1N1 flu vaccine was recommended by doctor. 

doctor_recc_seasonal - Seasonal flu vaccine was recommended by doctor.

chronic_med_condition - Has any of the following chronic medical conditions: asthma or an other lung condition, diabetes, a heart condition, a kidney condition, sickle cell anemia or other anemia, a neurological or neuromuscular condition, a liver condition, or a weakened immune system caused by a chronic illness or by medicines taken for a chronic illness.

child_under_6_months - Has regular close contact with a child under the age of six months.

health_worker - Is a healthcare worker.

health_insurance - Has health insurance.

opinion_h1n1_vacc_effective - Respondent's opinion about H1N1 vaccine effectiveness.

1 = Not at all effective; 2 = Not very effective; 3 = Don't know; 4 = Somewhat effective; 5 = Very effective.

opinion_h1n1_risk - Respondent's opinion about risk of getting sick with H1N1 flu without vaccine.

1 = Very Low; 2 = Somewhat low; 3 = Don't know; 4 = Somewhat high; 5 = Very high.

opinion_h1n1_sick_from_vacc - Respondent's worry of getting sick from taking H1N1 vaccine.

1 = Not at all worried; 2 = Not very worried; 3 = Don't know; 4 = Somewhat worried; 5 = Very worried.

opinion_seas_vacc_effective - Respondent's opinion about seasonal flu vaccine effectiveness.

1 = Not at all effective; 2 = Not very effective; 3 = Don't know; 4 = Somewhat effective; 5 = Very effective.

opinion_seas_risk - Respondent's opinion about risk of getting sick with seasonal flu without vaccine.

1 = Very Low; 2 = Somewhat low; 3 = Don't know; 4 = Somewhat high; 5 = Very high.

opinion_seas_sick_from_vacc - Respondent's worry of getting sick from taking seasonal flu vaccine.

1 = Not at all worried; 2 = Not very worried; 3 = Don't know; 4 = Somewhat worried; 5 = Very worried.

age_group - Age group of respondent.

education - Self-reported education level.

race - Race of respondent.

sex - Sex of respondent.

income_poverty - Household annual income of respondent with respect to 2008 Census poverty thresholds.

marital_status - Marital status of respondent.

rent_or_own - Housing situation of respondent.

employment_status - Employment status of respondent.

hhs_geo_region - Respondent's residence using a 10-region geographic classification defined by the U.S. Dept. of Health and Human Services. Values are represented as short random character strings.

census_msa - Respondent's residence within metropolitan statistical areas (MSA) as defined by the U.S. Census.

household_adults - Number of other adults in household, top-coded to 3.

household_children - Number of children in household, top-coded to 3.

employment_industry - Type of industry respondent is employed in. Values are represented as short random character strings.

employment_occupation - Type of occupation of respondent. Values are represented as short random character strings.

## Modeling
The project is dealing with a classification task since the goal is to predict whether individuals will get the H1N1 and seasonal flu vaccines based on their characteristics and behaviors. The model will include logistic regression, decision trees, random forests and XGBoost. The threshold of performance considered in this case is, achieving a high accuracy, precision, and recall for predicting vaccine uptake would be desirable.

## Evaluation 
Higher Uptake: The H1N1 vaccine appears to have a higher uptake compared to the seasonal flu vaccine. This is evident from the higher support (number of instances) for the seasonal vaccine in the dataset.

Prediction Confidence: Despite the higher uptake of the H1N1, both models exhibit similar predictive performance for both vaccines. This indicates that the models are equally effective at predicting individuals who took each vaccine.

Balanced Metrics: The F1-scores, precision, and recall values for both vaccines are relatively balanced, indicating that the models have a reasonable trade-off between correctly identifying individuals who took the vaccine and minimizing false positives.

Similar Accuracy: The accuracy of both models is also comparable, suggesting that they perform similarly overall in correctly predicting vaccine uptake.

## Conclusion
The H1N1 vaccine seems to have a higher uptake compared to the seasonal flu vaccine, as indicated by the higher support for the H1N1 vaccine in the dataset. Therefore, both vaccines are predicted with similar confidence levels, indicating that the models are robust and effective for predicting vaccine uptake in the given dataset. The higher accuracy could be attributed to the specific attributes and features that strongly correlated with H1N1 vaccine uptake, as identified in the analysis. This underscores the importance of tailoring vaccination promotion strategies based on vaccine-specific factors and utilizing predictive models that consider these nuances. Additionally, the conclusion may emphasize the need for targeted interventions to address specific challenges associated with seasonal flu vaccine uptake, as reflected in the slightly lower accuracy for that model.

The presentation can be viewed [here](https://www.canva.com/design/DAF-wUY4rvE/D6iHaUaBsc47xqjPfxd6OQ/edit?utm_content=DAF-wUY4rvE&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton)




