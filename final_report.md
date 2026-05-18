# Menstrual Cycle Analysis Using Personal Symptom Tracking Data

## Introduction

Menstrual cycle–related changes affect both physical and emotional well-being, yet these patterns are often discussed only in general terms rather than analyzed through personal data. With the increasing availability of self-tracking applications, it has become possible to collect daily health-related information and explore these changes more systematically.

This project analyzes self-tracked menstrual cycle data to investigate how symptoms such as mood, cramps and energy levels vary across different phases of the cycle. By combining exploratory data analysis, statistical testing and machine learning methods, the project aims to identify meaningful patterns and evaluate whether daily symptoms can be used to predict cycle phases.

The study follows a complete data science pipeline, including data collection, preprocessing, visualization, hypothesis testing and predictive modeling.

## Motivation

Menstrual cycle–related changes are often talked about in general terms, but they are rarely examined through personal data. Since I have been tracking my cycle for some time, I became curious about whether these commonly discussed patterns actually appear in my own daily life.

Rather than relying only on general assumptions, this project focuses on exploring real, self-tracked data to better understand how mood, energy and physical symptoms vary throughout the cycle. Turning this personal dataset into a structured analysis made it possible to observe patterns more objectively.

Working on a topic that is directly connected to everyday experience also made the project more engaging, while still allowing the application of core data science concepts such as data collection, preprocessing, visualization and interpretation.

## Dataset and Data Collection

The dataset used in this project was created manually based on self-tracked menstrual cycle records collected over multiple months. Each row in the dataset represents a single day and includes information related to physical and emotional symptoms experienced during the menstrual cycle.

The dataset contains the following features:

- `date`: calendar date  
- `cycle_id`: identifier for each menstrual cycle  
- `cycle_day`: day within the cycle  
- `bleeding`: binary indicator of menstruation  
- `flow_level`: intensity of bleeding  
- `cramps`: severity of cramps  
- `headache`: presence and severity of headaches  
- `mood`: daily mood level  
- `energy`: daily energy level  

The collected data was stored in CSV format and processed using Python libraries such as Pandas and NumPy.

Since the dataset is based on personal tracking data, it reflects real daily variations and symptom patterns rather than artificially generated observations.

## Methodology

The project follows a structured data science workflow consisting of data preprocessing, exploratory data analysis, statistical testing and machine learning.

### Data Preprocessing

The dataset was first cleaned and organized using Pandas. Dates were converted into datetime format and the data was sorted chronologically. In addition, a new feature called `phase` was created to categorize each day into one of three menstrual cycle phases:

- menstrual  
- premenstrual  
- other  

This categorization was based on bleeding information and cycle day values.

### Exploratory Data Analysis (EDA)

Several visualization techniques were used to explore patterns in the data. Bar charts were created to compare average mood, cramps and energy levels across different cycle phases. Correlation matrices and scatter plots were also used to analyze relationships between symptoms and observe trends throughout the cycle.

### Statistical Testing

To numerically evaluate relationships between symptoms, Pearson and Spearman correlation coefficients were calculated. These tests were used to investigate associations between physical symptoms such as cramps and emotional indicators such as mood and energy.

### Machine Learning

Machine learning models were applied to predict menstrual cycle phases based on daily symptoms. Logistic Regression and Random Forest classifiers were trained using features such as mood, cramps, energy and headache.

Model performance was evaluated using:
- accuracy
- confusion matrix
- classification report
- feature importance analysis

This approach made it possible to compare exploratory findings with predictive modeling results.

## Findings

The analysis reveals clear and consistent patterns across different phases of the menstrual cycle.

### Mood

Mood levels are highest during the non-menstrual phase and decrease noticeably during the premenstrual phase. This suggests that emotional well-being is affected by cycle-related changes, particularly towards the end of the cycle.

### Cramps

Cramps are most intense during the menstrual phase and are minimal during other phases. A slight increase is also observed during premenstrual days, indicating that physical discomfort may begin before menstruation starts.

### Energy

Energy levels follow a pattern similar to mood. Higher energy levels are generally observed during the middle of the cycle, while lower values appear during menstrual and premenstrual phases.

### Correlation Analysis

Pearson and Spearman correlation analyses show negative relationships between cramps and both mood and energy. These findings suggest that increased physical discomfort is associated with lower emotional well-being and reduced energy levels.

### Machine Learning Results

The machine learning models achieved reasonable performance in predicting menstrual cycle phases using daily symptoms.

Both Logistic Regression and Random Forest models were able to capture meaningful patterns in the data. Feature importance analysis indicates that cramps, mood, and energy are among the most influential variables for phase prediction.

The consistency between exploratory analysis and machine learning results supports the hypothesis that menstrual cycle phases influence both physical and emotional states.

## Limitations and Future Work

Although the project produced meaningful findings, several limitations should be considered.

First, the dataset is relatively small and based on self-tracked personal observations. Because the data reflects only a limited number of menstrual cycles, the results may not generalize to larger populations.

In addition, some variables such as mood and energy are subjective measurements and may vary depending on external factors unrelated to the menstrual cycle.

The machine learning models also have limitations due to the dataset size and overlapping characteristics between cycle phases. While the models capture important patterns, their predictive performance could be improved with more extensive data.

Future work could include:
- collecting data over longer periods  
- incorporating wearable device data such as sleep or heart rate  
- applying more advanced machine learning models  
- developing personalized symptom forecasting systems

## Conclusion

This project explored how menstrual cycle phases relate to physical and emotional well-being using self-tracked daily symptom data.

Through exploratory data analysis, statistical testing, and machine learning methods, clear patterns were identified between cycle phases and symptoms such as mood, cramps and energy levels. Both the visual analyses and predictive models support the hypothesis that menstrual cycle phases influence daily well-being.

The project also demonstrates how personal health tracking data can be analyzed using data science techniques to generate meaningful insights. Despite limitations related to dataset size and subjectivity, the findings highlight the potential of data-driven approaches in understanding menstrual health patterns.
