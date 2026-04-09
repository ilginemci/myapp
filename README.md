# Menstrual Cycle Analysis

## Overview
This project analyzes how different phases of the menstrual cycle influence physical and emotional well-being. Using self-tracked daily data, the study investigates patterns in mood, cramps and energy levels across cycle phases.

---

## Motivation

Menstrual cycle–related changes are often talked about in general terms, but they are rarely examined through personal data. Since I have been tracking my cycle for some time, I became curious about whether these commonly discussed patterns actually appear in my own daily life.

Rather than relying only on general assumptions, this project focuses on exploring real, self-tracked data to better understand how mood, energy and physical symptoms vary throughout the cycle. Turning this personal dataset into a structured analysis made it possible to observe patterns more objectively.

Working on a topic that is directly connected to everyday experience also made the project more engaging, while still allowing the application of core data science concepts such as data collection, preprocessing, visualization and interpretation.

---

## Dataset
The dataset consists of manually recorded daily observations over multiple menstrual cycles.

Each entry includes:
- `date`: calendar date  
- `cycle_id`: identifier for each cycle  
- `cycle_day`: day within the cycle  
- `bleeding`: binary indicator (1 = yes, 0 = no)  
- `flow_level`: intensity of bleeding (0–3)  
- `cramps`: severity of cramps (0–3)  
- `headache`: presence of headache (0–2)  
- `mood`: subjective mood level (1–5)  
- `energy`: energy level (1–5)  

---

## Methodology

### 1. Data Collection
Data was manually collected based on daily menstrual cycle tracking.

### 2. Data Processing
- Dates were converted to datetime format  
- Data was sorted chronologically  
- A new feature called `phase` was created:
  - **menstrual** → bleeding days  
  - **premenstrual** → late cycle days  
  - **other** → remaining days  

### 3. Exploratory Data Analysis (EDA)
The following relationships were analyzed:
- Mood vs. cycle phase  
- Cramps vs. cycle phase  
- Energy vs. cycle phase  

Visualizations were created to identify trends across phases.

---

## Key Findings

- **Mood** is highest during the non-menstrual phase and lowest during the premenstrual phase.  
- **Cramps** peak during the menstrual phase and are minimal otherwise.  
- **Energy** is highest during the middle of the cycle and decreases before and during menstruation.  

These results indicate a clear relationship between menstrual cycle phases and both physical and emotional states.

---

## Repository Structure

data/
clue_daily_data.csv

notebooks/
01_data_loading.ipynb
02_eda.ipynb
03_hypothesis.ipynb

---

## Tools and Technologies
- Python  
- Pandas  
- Matplotlib  
- Google Colab  

---

## Conclusion
This project demonstrates that menstrual cycle phases have a measurable and consistent impact on daily well-being. The findings highlight the importance of incorporating biological cycles into personal health analysis and data-driven decision making.

---

## Future Work
- Extend dataset to longer time periods  
- Apply statistical testing  
- Build predictive models for symptom forecasting  
