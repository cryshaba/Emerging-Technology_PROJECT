# CapstoneProject_EmergingTechnologies
TEECE 2 Capstone Project Lifestyle and Learning – Predicting Student Performance
# Student Lifestyle Analysis and Exam Performance Prediction

This project utilizes a simulated dataset of 1,000 student records sourced from Kaggle. Each record captures key lifestyle habits—such as study hours, sleep patterns, screen time, diet, and mental health— and relates them to academic performance, specifically the final exam score. The dataset is ideal for educational machine learning applications, enabling learners to perform data preprocessing, visualization, clustering, regression, and classification.

## Project Goals
- Determine relationships between lifestyle habits and final exam scores
- Discover meaningful student groupings based on lifestyle through clustering
- Build and evaluate models that predict academic performance
- Summarize and communicate findings through data storytelling

## Dataset Description
Each studnet record contains:
- Demographics: age, gender, education level of parents
- Lifestyle Habits: daily study hours, screen time (Netflix/social media), dietary habits, sleep patterns
- Well-Being Indicators: mental health scores, physical activity, part-time job status
- Target Variable: final exam score (numerical)

## Workflow Summary
### 1. Data Preprocessing
- Handle missing values
- One-hot/ordinal encoding for categorial variables
- Normalize features using `StandardScaler`

### 2. Feature Engineering
New features were engineered on the scaled data to better represent student behavior patterns and enhance model performance:
- `total_screen_time`
    - Computed as the sum of `social_media_hours` and `netflix_hours`.

