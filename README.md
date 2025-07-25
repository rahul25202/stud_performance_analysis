Student Performance Indicator
📊 Dataset Overview
The objective of this project is to explore how factors like parental background, test preparation, and other student-specific variables influence math performance. The dataset contains 8 input features:

gender: Student's gender (Male/Female)

race/ethnicity: Ethnic background (Group A, B, C, D, E)

parental level of education: Highest education level achieved by parents (e.g., bachelor's degree, master's degree, high school, etc.)

lunch: Type of lunch received (standard or free/reduced)

test preparation course: Completion status of a test preparation course

reading score: Score achieved in the reading test

writing score: Score achieved in the writing test

🎯 Target Feature:

math score: Math test result of the student

📌 Dataset Source: https://www.kaggle.com/datasets/spscientist/students-performance-in-exams?resource=download

🎥 UI Animation


🛠️ Development Workflow
1. Data Ingestion
Load the dataset from CSV format

Perform train-test split

Save the resulting datasets for further processing

2. Data Transformation
Construct a ColumnTransformer pipeline

For numerical features:

Apply SimpleImputer with a median strategy (to address outliers)

Use StandardScaler for normalization

For categorical features:

Use SimpleImputer with most frequent strategy

Apply One-Hot Encoding

Normalize with StandardScaler

Save the preprocessor as a .pkl file in the artifacts folder

3. Model Training
Train multiple models and evaluate their performance

The best-performing model was Linear Regression

Perform hyperparameter tuning for improved accuracy

Save the best model as a pickle file for predictions

4. Prediction Pipeline
Take input data and convert it to a DataFrame

Load the saved preprocessor and model pickle files

Generate predictions using the trained pipeline

5. Flask Web Application
Build a web interface using Flask

Allow users to input student details and get math score predictions directly on the app

📈 EDA Notebook
Explore the data here: EDA Notebook

🤖 Model Training Notebook
View training approach: Model Training Notebook

🚀 How to Use
bash
Copy
Edit
1. conda create -p std python=3.8 -y  
2. conda activate std/  
3. pip install -r requirements.txt  
4. python app.py
