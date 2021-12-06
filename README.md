# Capstone Project: COVID-19 Hospital Stay Predictor

## Technical Summary

In this project, I create a predictive classification model geared towards a hospital's analytics team seeking to make informed decisions for resources and personnel allocation based on predicted inpatient length of stay. The target variable is classified into three labels: "Short-Term", "Medium-Term", and "Long-Term" based on the number of days a patient is predicted to stay. The model uses fourteen features to predict the length of stay -- with features such as Type of Admission, Severity of Illness, Bed Grade, and Ward Type having the most influence. The final model produced is an tuned XGBoost model that is able to predict length of stay with 54% accuracy. With further research and implementation, classifiers like these could be used in emergency situations to properly allocate resources based on predictive knowledge of how long a patient is expected to admitted for. 

## The Motivation

It goes without saying that the onset of the COVID-19 virus has had a drastic impact on the world as we know it today. At the beginning of the pandemic, hospitals were overrun with patients needing medical attention and it became clear that hospital infrastructure was not equipped for this unprecedented event.

The motivation for this project came from a conversation I had with my roommate who is a nurse here in San Francisco who worked on a COVID unit during the pandemic. She told me that one of the biggest factors leading to inadequate care was the lack of hospital resources. Without proper resources, sick people were not able to receieve proper care. One of major contributing factors to this came from not knowing how long a patient would be hospitalized for when they are admitted. With such a huge influx of long-term residential patients, hospitals were quickly drained of resources such as PPE, certain medications, and even beds themselves. 

### Data Analysis 

**Stakeholder**: Analytics team for a group of hospitals looking to predict length of stay (LOS) estimates for COVID-19 inpatients. 

**Problem**: Effectively predict the length of stay of a COVID-19 patient given similar past patient profiles in order to better allocate hospital resources and personnel. 

**Target**: Length of stay (LOS)
* Length of stay is defined as a categorical variable in this dataset broken into 10 day increments.
* In order to fit with my model, this was encoded using a LabelEncoder as follows:
    
| Label | # of Days |
| --- | --- |
| 0 | 0-10 Days |
| 1 | 11-20 Days |
| 2 | 21-30 Days |
| 3 | 31-40 Days |
| 4 | 41-50 Days |
| 5 | 51-60 Days |
| 6 | 61-70 Days |
| 7 | 71-80 Days |
| 8 | 81-90 Days |
| 9 | 91-100 Days |
| 10 | >100 Days |

* Upon further analysis of the data (discussed more in next section), I decided to group the labels into three categories: "Short-Term", "Medium-Term", and "Long-Term" by binning the data as follows: 

| Label | Type of Stay | # of Days |
| --- | --- | --- | 
| 0 | Short-Term | 0-20 Days |
| 1 | Medium-Term | 21-50 Days |
| 2 | Long-Term | > 51 Days |


My data came from a series of analytic healthcare data provided on Kaggle by Vidhya Healthcare Analytics to be used as a means of building and sharing predictive models for COVID-19 related projects.

The data was collected anonymously in order to protect the identity of the individuals and hospitals.
