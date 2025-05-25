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
    - Designed to quantify total leisure-based screen exposure, which may affect sleep or study focus.

- `study_efficiency`
    - Calculated by summing `study_hours_per_day` and `attendance_percentage`.
    - Represents a combined indicator of time invested and classroom engagement.

- `total_well-being`
    - Derived by adding together `exercise_frequency`, `mental_health_rating`, and `sleep_hours`.
    - Aims to capture overall wellness that may influence academic consistency and focus.

### 3. Exploratory Data Analysis 
- Explored data using histograms, scatter plots, box plots, and correlation heatmaps
- Strong positive correlations with exam score: study_hours_per_day, mental_health_rating, productive_hours
- Slight negative correlation with exam score: total_screen_time

### 4. Clustering (K-Means)
- Applied K-Means clustering on lifestyle features (excluding exam scores)
- Determined optimal cluster count using:
  - Elbow method (inertia plot) suggested 3 clusters
  - Silhouette scores confirmed 3 clusters with best balance
- Labeled clusters as:
    - High Screen & Low Sleep
    - Balanced & High Efficiency
    - Well-Rested & Active
- Visualized clusters using PCA for 2D representation with distinct color coding
- Compared exam scores across clusters using box plots, showing performance differences by lifestyle group

