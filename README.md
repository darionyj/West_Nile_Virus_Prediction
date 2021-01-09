# West_Nile_Virus_Prediction

## Problem Statement
West Nile Virus (Wnv), a mosquito-bourne arbovirus, has been causing significant and sometimes severe human diseases. Although pesticides are known to be effective in dealing with the virus-carrying mosquitoes, it is expensive to deploy pesticides throughout the city. As data scientists in the Division of Societal Cures in Epidemiology & New Creative Engineering, we want to understand the factors driving the spread of Wnv by leveraging on data collected by Chicago's weather stations and the surveillance system set up by the Chicago Department of Public Health. We also want to develop a classfication model that could predict the presence of Wnv within the area of Windy City. Through these studies, we hope to suggest a cost-efficient and effective method of deploying pesticides within the area.

## Executive Summary

This project is part of a [Kaggle competition](https://www.kaggle.com/c/predict-west-nile-virus/overview) and explores data collected from various sources, namely:  
* Mosquito trap data collected by the surveillance and control system
* Location data of spraying efforts
* Weather data

The data from these three sources were combined to form a more wholesome dataset for analysis and modelling. The spray data was used to create a feature indicating if each mosquito trap was within the spray zone over a period of 30 days from the spray date. The weather data was added to the combined dataset based on date and location.

Several classifier models were developed, where the hyperparameters were tuned for each model to obtain the best cross-validated AUC scores. Because there were heavy imbalances in the data collected (about 95% of the data indicated no Wnv), an over-sampling method known as SMOTE (Synthetic Minority Over-sampling Technique) was adopted. It was also the reason for optimizing the models on AUC scores instead of accuracy. Comparing the AUC and recall scores, the production model selected was the AdaBoost model. Comparing the train and test accuracy scores of the selected model, there was evidence of slight overfitting of the data but the small difference was acceptable by our means.

We discovered that the time of the day where the sun is out was where the presence of Wnv was the strongest. Also, we observed that the more competent vectors for the spread of Wnv were the culex pipiens and culex restuans species. In order to deploy pesticides in a more cost-efficient way, we recommend spraying in areas where culex pipiens/restuans are most prominent and during the day as the Sun rises where the mosquitoes are most active.

We also explored into deep learning and neural networks. However, our neural network did not outperform the selected model, likely due to the fact it had low complexity. We decided not to further develop the deep learning model since it is not easily interpretable and we had to keep within the limited timeframe of this project.


