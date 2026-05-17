# Student Performance Analyzer - Machine Learning Project

##  Project Overview

Student Performance Analyzer is an end-to-end Machine Learning project that predicts a student's Maths score based on various academic and demographic factors such as gender, ethnicity, parental education level, lunch type, test preparation course, reading score, and writing score.

This project demonstrates the complete Machine Learning lifecycle including:

* Data Ingestion
* Data Transformation
* Model Training
* Model Evaluation
* Prediction Pipeline
* Flask Web Application Deployment

---

#  Features

* End-to-End Machine Learning Pipeline
* Data Preprocessing using Scikit-Learn Pipelines
* Multiple Regression Algorithms Comparison
* Hyperparameter Tuning
* Flask Web Interface
* Exception Handling and Logging
* Modular Project Structure

---

#  Technologies Used

## Programming Language

* Python

## Libraries and Frameworks

* Pandas
* NumPy
* Scikit-Learn
* CatBoost
* XGBoost
* Flask

---

#  Project Structure

```bash
ML_PROJECT/
│
├── artifacts/
│   ├── data.csv
│   ├── train.csv
│   ├── test.csv
│   ├── model.pkl
│   └── proprocessor.pkl
│
├── notebook/
│   ├── data/
│   │   └── stud.csv
│   ├── 1. EDA STUDENT PERFORMANCE.ipynb
│   └── 2. MODEL TRAINING.ipynb
│
├── src/
│   ├── components/
│   │   ├── data_ingestion.py
│   │   ├── data_transformation.py
│   │   └── model_trainer.py
│   │
│   ├── pipeline/
│   │   ├── predict_pipeline.py
│   │   └── train_pipeline.py
│   │
│   ├── exception.py
│   ├── logger.py
│   └── utils.py
│
├── templates/
│   ├── home.html
│   └── index.html
│
├── app.py
├── requirements.txt
└── README.md
```

---

#  Dataset Information

The dataset contains student academic performance details.

## Input Features

| Feature                     | Description               |
| --------------------------- | ------------------------- |
| gender                      | Student gender            |
| race_ethnicity              | Student ethnicity group   |
| parental_level_of_education | Parent education level    |
| lunch                       | Lunch type                |
| test_preparation_course     | Preparation course status |
| reading_score               | Reading marks             |
| writing_score               | Writing marks             |

## Target Feature

| Feature    | Description |
| ---------- | ----------- |
| math_score | Maths marks |

---

#  Machine Learning Workflow

## 1. Data Ingestion

Implemented in:

```python
src/components/data_ingestion.py
```

### Tasks Performed

* Read dataset using Pandas
* Train-test split
* Store raw/train/test CSV files in artifacts folder

---

## 2. Data Transformation

Implemented in:

```python
src/components/data_transformation.py
```

### Numerical Pipeline

* Median Imputation
* Standard Scaling

### Categorical Pipeline

* Most Frequent Imputation
* One Hot Encoding
* Feature Scaling

### Final Transformation

Used ColumnTransformer to combine both pipelines.

---

## 3. Model Training

Implemented in:

```python
src/components/model_trainer.py
```

### Models Used

* Linear Regression
* Decision Tree Regressor
* Random Forest Regressor
* Gradient Boosting Regressor
* XGBoost Regressor
* CatBoost Regressor
* AdaBoost Regressor

### Model Selection

* Hyperparameter tuning performed
* Best model selected based on R² Score

---

#  Model Evaluation

Evaluation Metric Used:

```text
R² Score
```

The best-performing model is saved as:

```text
artifacts/model.pkl
```

---

#  Prediction Pipeline

Implemented in:

```python
src/pipeline/predict_pipeline.py
```

### Functionality

* Load trained model
* Load preprocessing object
* Transform user input
* Predict Maths score

---

#  Flask Web Application

Implemented in:

```python
app.py
```

## Features

* User-friendly web interface
* Input student details
* Predict Maths performance instantly

---

# 👨‍💻 Author

Vedant Uplap

B.Tech CSE Student
Interested in AI/ML and Data Science

---

#  Conclusion

This project demonstrates a complete end-to-end Machine Learning workflow from data preprocessing to deployment using Flask. It showcases practical implementation of multiple regression models and real-time prediction through a web application.
