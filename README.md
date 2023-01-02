# Biased Police Behaviour Classifier

## Introduction
This project is developed for the module IE0005: Intro to Data Science & AI.

In this project, we focus to:

• Determine the reasons of individuals being stopped by police while driving  
• Determine if there are any biases for a police to stop someone based on their gender, race, age etc  

by using the dataset below.

## Dataset
Our team has decided to use the dataset from the "Stanford Open Policing Project", a project centered on collecting and tracking police stops information in the United States. The project provides tons of data, collected from 21 state patrols agencies and 29 municipal police department, totalling nearly 100 million traffic stops details such as Stop Date, Driver Race, Driver Sex, Contraband Found etc.

All the data are available on this page, https://openpolicing.stanford.edu/data/. 
We have chosen to use data from San Francisco, alluding to its high number of entries(almost 1 million), long period(Jan 2007 - Jun 2016) and most importantly, it has 12 out of the 14 attributes.

## Project Pipeline
1. [Data Cleaning](https://github.com/Jy158654/biased-police-behaviour-classifier/blob/main/data%20cleaning.ipynb)  
2. [Exploratory Data Analysis (EDA)](https://github.com/Jy158654/biased-police-behaviour-classifier/blob/main/EDA.ipynb)  
3. [Model Building](https://github.com/Jy158654/biased-police-behaviour-classifier/blob/main/model%20building.ipynb)  
4. [Machine Learning](https://github.com/Jy158654/biased-police-behaviour-classifier/blob/main/machine%20learning.ipynb)

## Problem Statement  
If you get stopped by the police in San Francisco, are you being stopped for a valid reason?

## EDA Summary 
There are numerous factors that might influence your odds of being convicted. 

Age is fairly interesting as those stopped with valid reasons tend to be slightly older folks, yet the younger folks are the ones being stopped more often. Gender, males specifically, gets stopped more often, and have a higher odds of being searched as well. Regardless, the variable that exhibits the most bias is Race. Blacks and Hispanics have a significantly higher chance of being stopped for a non-valid reason, and if stopped stopped for a valid reason, have a higher chance of being arrested, compared to just being issued a warning or citation. Next, vehicle search isn't directly correlated to being stopped for a valid reason, as most stopped for a valid reason did not get searched at all. In fact, if you are searched, statistically, you actually have a higher chance of being stopped without a valid reason. This is due to the fact that vehicle search is an extremely biased decision.

This realisation led to one of the most intriguing finding --- coming from race vs contraband found. Previously, we mentioned that vehicle search doesn't increase your chances of being caught. However, the nature of vehicle search is that it is almost entirely based on a police officer's gut feeling. In other words, it is a very subjective decision. Hence, there will be a lot of biases that comes into play when deciding to search a vechicle or not. Evident from the EDA of Race vs Contraband Found, almost half of the victims of unsuccessful search are Blacks, showing a huge bias against Black people that they might have contrabands on them.

## Machine Learning  
### Predictors  
```age_band```  
```subject_race```  
```subject_sex```  
```contraband_found```  
```search_vehicle```  
```reason_for_stop```  

### Response  
```outcome```  

### Models Used
• Decision Tree (depth=6 & K-Fold cross validation)  
• Artificial Neural Network (ANN) 

## Conclusion  
We met the initial objectives of our project which are to determine the reasons of individuals being stopped by police, and to determine if there are any biases for a police to stop someone based on their gender, race, age etc. By further working on the dataset, we are also able to produce highly accurate machine learning models in predicting if a person is stopped by a police with valid reason or without valid reason, which answered our problem statement.
