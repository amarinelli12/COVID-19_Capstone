# Capstone Project: COVID-19 Hospital Stay Predictor

## Technical Summary

In this project, I create a predictive classification model geared towards a hospital's analytics team seeking to make informed decisions for resources and personnel allocation based on predicted inpatient length of stay. The target variable is classified into three labels: "Short-Term", "Medium-Term", and "Long-Term" based on the number of days a patient is predicted to stay. The model uses fourteen features to predict the length of stay -- with features such as Type of Admission, Severity of Illness, Bed Grade, and Ward Type having the most influence. The final model produced is an tuned XGBoost model that is able to predict length of stay with 54% accuracy. With further research and implementation, classifiers like these could be used in emergency situations to properly allocate resources based on predictive knowledge of how long a patient is expected to admitted for. 

## The Motivation

It goes without saying that the onset of the COVID-19 virus has had a drastic impact on the world as we know it today. At the beginning of the pandemic, hospitals were overrun with patients needing medical attention and it became clear that hospital infrastructure was not equipped for this unprecedented event.

!(dc4c15f1-efbe-40ca-b4ce-82e00df1d94f_w408_r1_s.webp)


The motivation for this project came from a conversation I had with my roommate who is a nurse here in San Francisco who worked on a COVID unit during the pandemic. She told me that one of the biggest factors leading to inadequate care was the lack of hospital resources. Without proper resources, sick people were not able to receieve proper care. One of major contributing factors to this came from not knowing how long a patient would be hospitalized for when they are admitted. With such a huge influx of long-term residential patients, hospitals were quickly drained of resources such as PPE, certain medications, and even beds themselves. 
