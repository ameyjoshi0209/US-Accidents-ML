# US Accidents Data Analysis and Modeling 🚗🚦
[![Python](https://img.shields.io/badge/python-3670A0?logo=python&logoColor=ffdd54)](https://www.python.org)
[![Jupyter Notebook](https://img.shields.io/badge/jupyter-%23FA0F00.svg?logo=jupyter&logoColor=white)](https://jupyter.org)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?logo=scikit-learn&logoColor=white)](https://scikit-learn.org/stable/index.html)
[![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?logo=pandas&logoColor=white)](https://pandas.pydata.org)
[![nVIDIA](https://img.shields.io/badge/nVIDIA-%2376B900.svg?logo=nVIDIA&logoColor=white)](https://www.nvidia.com/en-in/geforce/)  
![Visual Studio Code](https://img.shields.io/badge/Visual%20Studio%20Code-0078d7.svg?logo=visual-studio-code&logoColor=white)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## Welcome! 🎉

Welcome to the repository for the **US Accidents Data Analysis and Modeling** project! 🚗 In this project, we dive deep into a comprehensive dataset containing information about traffic accidents across the United States. The primary goal is to analyze trends, identify key factors influencing accident severity, and build predictive models using machine learning techniques 🤖.

This project provides valuable insights into accident patterns, helping us better understand the causes of accidents and predict their severity. By leveraging machine learning, we hope to contribute to improving road safety and assisting authorities in making data-driven decisions 💡. 

Feel free to explore the repository, experiment with the code, and contribute to improving the models. Your feedback and contributions are highly welcome! 🙌


## Introduction 📖

This documentation provides an in-depth analysis and machine learning modeling of U.S. traffic accident data. The primary goal of this work is to uncover trends, identify factors that influence accident severity, and build predictive models to assess the severity of accidents. The dataset includes various features such as accident location, time, weather conditions, and more, which are analyzed to gain insights into accident patterns.

## Dataset Overview 📊

The dataset used in this study contains detailed information about accidents in the United States, including various features that may contribute to the severity of accidents. Key features include:

| **Feature**         | **Description**                                                       |
|---------------------|-----------------------------------------------------------------------|
| **Source**          | The origin of the data 📡.                                            |
| **Severity**        | The severity level of the accident (integer values from 1 to 4) 🚑.  |
| **Start_Time**      | Timestamp indicating when the accident occurred ⏰.                   |
| **End_Time**        | Timestamp indicating when the accident ended ⏳.                      |
| **Start_Lat**       | Latitude of the start location of the accident 📍.                    |
| **Start_Lng**       | Longitude of the start location of the accident 📍.                   |
| **End_Lat**         | Latitude of the end location of the accident 📍.                      |
| **End_Lng**         | Longitude of the end location of the accident 📍.                     |
| **Distance(mi)**    | The distance the accident covered in miles 🚗.                        |
| **Description**     | A textual description of the accident 📝.                             |
| **Street**          | The street or road where the accident occurred 🛣️.                    |
| **City**            | The city where the accident took place 🏙️.                           |
| **State**           | The state where the accident occurred 🌎.                             |

## Data Cleaning and Preprocessing 🧹

Before performing any analysis or modeling, several preprocessing steps were taken to ensure the data is clean, consistent, and usable:

- **Missing Values**: Missing values were identified and handled appropriately. Numerical columns were filled with the median, and categorical columns with the mode.
- **Duplicates**: Duplicate entries were removed to avoid redundancy 🗑️.
- **Irrelevant Columns**: Columns deemed unnecessary for the analysis (e.g., "Country") were dropped 🗂️.
- **Data Type Conversion**: Timestamps were converted to more useful formats for feature extraction (e.g., extracting hour, day of the week, and month) ⏳.

## Feature Engineering 🔧

Feature engineering is crucial for improving the predictive power of the model. Key transformations applied include:

- **Time-based Features**: Extracted hour of the day, day of the week, and month from the accident start time to capture time-related patterns ⏰.
- **Geographical Features**: Created new features to measure distances to major highways or city centers 🗺️.
- **Weather-Related Features**: Weather-related data (e.g., temperature, precipitation) were included if available 🌦️.

## Exploratory Data Analysis (EDA) 🔍

EDA was conducted to identify trends, patterns, and correlations in the data. Key insights include:

- **Accident Frequency**: Analyzed by factors such as temperature, city, time of day, and season. 🚶‍♂️🌦️
- **Severity Distribution**: Found the dataset is imbalanced, with severity level 2 being most common ⚖️.
- **Accident Locations**: Visualized accident locations to identify high-risk areas 🗺️.
- **Temporal Trends**: Revealed higher accident frequencies during rush hour and certain seasons ⏳.

## Class Imbalance ⚖️

One major challenge in this dataset is the class imbalance. Most accidents belong to severity level 2, while severity levels 1, 3, and 4 are underrepresented.

- **Severity Distribution**: We explored techniques like **resampling** and **class weighting** to improve model performance on the minority classes 🎯.
- **Visualization**: A histogram was created to visually show the imbalance in the dataset 📊.

## Modeling 🧠

Various machine learning models were tested to predict accident severity:

- **Logistic Regression**: Initially implemented, achieving 85.84% accuracy, but was biased towards predicting severity 2 due to the class imbalance 📉.
- **Handling Class Imbalance**: Used **undersampling** to balance the dataset, which decreased accuracy to 55.00% but improved predictions across all severity classes ⚖️.
- **Hyperparameter Tuning**: Optimized model parameters with **RandomizedSearchCV**, improving accuracy to 72.16% 🔧.
- **Model Evaluation**: Accuracy, precision, recall, F1-score, and confusion matrix were used to assess model performance 🔍.


## Visualization Results 📊

Visualizations, including confusion matrices and heatmaps, were employed to illustrate model performance and class distribution. The confusion matrix indicated the model's ability to predict different severity levels, while the heatmap provided a clear representation of precision and recall across classes. These visual tools facilitated a better understanding of the model's strengths and weaknesses.

## Conclusion 🎯

The analysis and modeling of the US accidents dataset 🗺️ emphasized the critical importance of:

- Data Cleaning 🧹: Ensuring the dataset is accurate and ready for analysis.
- Feature Engineering 🔧: Transforming raw data into useful features for better predictions.
- Class Imbalance ⚖️: Addressing imbalance to avoid biased predictions.

The Logistic Regression model improved after hyperparameter tuning 🔧, but further exploration of additional models and techniques 🤖 could lead to even better results 🚀.

Overall, this study highlights the potential of machine learning 🤖 in predicting accident severity 🚗 and the need for continuous model refinement to enhance accuracy 🎯 and reliability 🔍.

## Future Scope

Future Scope 🚀

The analysis uncovered key insights into accident trends and identified factors influencing severity. Predictive models were developed, but improvements are needed, particularly for minority classes. Future work may involve:

- Exploring advanced algorithms like Random Forest 🌲, XGBoost 📈, or Neural Networks 🧠.
- Adding real-time traffic and weather data for more accurate predictions 🌧️🚗.
- Addressing class imbalance using more advanced techniques like SMOTE ⚖️.

## Acknowledgments 🙏

Special thanks to the dataset creators and contributors for providing the data. We also acknowledge the open-source libraries that made this analysis possible, including **scikit-learn**, **pandas**, **matplotlib**, and **seaborn** 📚.

Feel free to explore, contribute, and make this project even better! 💻
