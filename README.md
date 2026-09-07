# Student Mental Health Python Analysis

## 1. Project Title

*Student Mental Health Data Analysis Using Python*

## 2. Project Overview

This project presents a Python-based analysis of a Student Mental Health dataset.

The analysis covers data cleaning, calculated columns, exploratory data analysis, sorting and filtering, index-based filtering, correlation analysis, descriptive statistics, data visualization, and Logistic Regression for predicting reported depression status.

The project demonstrates how Python can be used to explore, visualize, and analyze student mental health data.

## 3. Problem Statement

Student mental health can be affected by different factors, including anxiety, panic attacks, academic factors, and other personal circumstances.

Analyzing student mental health data can help identify patterns and relationships among these factors.

This project uses Python to explore the dataset, examine relationships between mental health variables, and develop a Logistic Regression model to predict whether a student reported depression.

## 4. Data Source

The dataset contains *101 student records* and *11 original variables*.

The dataset includes information such as:

- Gender
- Age
- Course
- Year of Study
- CGPA
- Marital Status
- Depression
- Anxiety
- Panic Attack
- Specialist Treatment

The original dataset is included in the *Raw Data* folder of this repository.

## 5. Methodology

The project was carried out using Python through the following steps:

1. Loaded the Student Mental Health dataset.
2. Checked and cleaned the data.
3. Checked for missing values and duplicate records.
4. Standardized the CGPA field.
5. Created calculated columns.
6. Grouped students into age groups.
7. Encoded Depression, Anxiety, and Panic Attack as numerical scores.
8. Created a combined Mental Health Score.
9. Converted CGPA ranges into representative midpoint values.
10. Performed exploratory data analysis.
11. Performed sorting and filtering operations.
12. Applied index-based filtering using iloc[] and loc[].
13. Performed correlation analysis.
14. Generated descriptive statistics.
15. Created six dashboard-style visualizations using Plotly.
16. Applied Logistic Regression to predict reported depression.
17. Used an 80/20 stratified train-test split to evaluate the model.

### Calculated Columns

| Calculated Column | Purpose |
|---|---|
| Age_Group | Groups students into 18–20, 21–23 and 24+ |
| Depression_Score | Encodes Depression as 1/0 |
| Anxiety_Score | Encodes Anxiety as 1/0 |
| Panic_Score | Encodes Panic Attack as 1/0 |
| Mental_Health_Score | Combines depression, anxiety and panic scores |
| CGPA_Mid | Converts CGPA ranges into representative midpoint values |

### Visualizations

Six dashboard-style visualizations were created:

- Gender Distribution
- Number of Students by Course
- Age Distribution
- Students with Depression
- Distribution of Mental Health Scores
- Average CGPA by Year of Study

### Correlation Analysis

A Plotly correlation heatmap was created using Age, CGPA_Mid, Depression_Score, Anxiety_Score, Panic_Score, and Mental_Health_Score.

Selected correlations included:

- Age–CGPA: *0.03*
- Age–Depression: *−0.067*
- Age–Anxiety: *−0.089*
- Age–Panic: *0.06*
- Depression–Anxiety: *0.274*
- Depression–Panic: *0.247*
- Anxiety–Panic: *0.084*
- Depression–Mental Health Score: *0.743*
- Anxiety–Mental Health Score: *0.652*
- Panic–Mental Health Score: *0.646*

### Logistic Regression

Logistic Regression was used to predict whether a student reported depression.

*Target Variable:*
- Depression: Yes = 1, No = 0

*Predictors:*
- Age
- CGPA_Mid
- Anxiety_Score
- Panic_Score

An 80/20 stratified train-test split was used.

## 6. Key Insights

The analysis produced the following findings:

- The dataset contains *101 student records*.
- Depression, anxiety, and panic attack showed positive relationships with the combined Mental Health Score.
- Depression had the strongest selected correlation with the Mental Health Score at *0.743*.
- Anxiety had a correlation of *0.652* with the Mental Health Score.
- Panic Attack had a correlation of *0.646* with the Mental Health Score.
- Depression and Anxiety showed a positive relationship of *0.274*.
- Depression and Panic Attack showed a positive relationship of *0.247*.
- Age showed very weak relationships with the other analyzed variables.
- The Logistic Regression model achieved *71.43% accuracy*.
- The model correctly predicted *15 out of 21* test observations.
- Recall for No Depression was *100%, while recall for Depression was **14%*.
- The model therefore performed much better at identifying No Depression cases than Depression cases.

## 7. Conclusion / Recommendations

### Conclusion

This project demonstrates a complete Python data-analysis workflow using a Student Mental Health dataset.

The project combined data cleaning, feature engineering, exploratory analysis, visualization, statistical analysis, correlation analysis, and predictive modelling.

The Logistic Regression model achieved *71.43% accuracy* on the test set. However, its *14% recall for Depression cases* indicates that the model had difficulty identifying positive depression cases.

The relatively small dataset and test set should be considered when interpreting the model's performance.

### Recommendations

- Use larger datasets to improve the reliability of predictive modelling.
- Include additional relevant variables that may improve model performance.
- Evaluate mental health prediction models using multiple performance metrics rather than accuracy alone.
- Compare Logistic Regression with other suitable machine-learning models.
- Continue improving data quality and preprocessing before modelling.
- Use predictive results carefully and responsibly when dealing with mental health-related data.

## Project Files
[View Python Analysis](Python%20Analysis/student_mental_health_project%281%29.ipynb)

- *Raw Data* – Contains the original Student Mental Health dataset.
- *Python Analysis* – Contains the Python analysis file/notebook.
- *Report* – Contains the complete project report.

## Tools and Technologies

- Python
- Pandas
- Plotly
- Scikit-learn
- Jupyter / Google Colab

## Author

*Clement Jonathan*
