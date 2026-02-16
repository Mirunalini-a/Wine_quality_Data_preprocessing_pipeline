##Wine Quality – End-to-End Data Preprocessing Pipeline

A complete implementation of a structured data preprocessing pipeline applied to the Wine Quality dataset. This project demonstrates how cleaning, transformation, feature selection, and dimensionality reduction impact machine learning model performance.

#📌 Project Objective

To implement and evaluate a complete data preprocessing workflow including:

Data Cleaning

Data Transformation

Feature Selection

Dimensionality Reduction (PCA)

Data Visualization

Model Performance Comparison

The goal is to clearly demonstrate the Before vs After impact of preprocessing techniques on classification accuracy.

#📂 Dataset Information

Dataset: Wine Quality (Red Wine)

Source: UCI Machine Learning Repository

Samples: 1599

Features: 11 physicochemical attributes

Target: Wine Quality

The regression target was converted into a binary classification problem:

Quality ≥ 6 → Good Wine (1)

Quality < 6 → Bad Wine (0)

🧠 Machine Learning Problem

Binary classification using:

Logistic Regression

Evaluation metric:

Accuracy

🔎 Project Pipeline
1️⃣ Exploratory Data Analysis (EDA)

Performed before any preprocessing.

Analysis Included:

Dataset structure inspection

Missing value analysis

Statistical summary

Feature distributions

Correlation analysis

Outlier visualization

Key Observations:

No missing values

Duplicate records present

Several features contain outliers

Alcohol positively correlated with quality

Volatile acidity negatively correlated with quality

Visualizations:

Missing value heatmap

Histograms

Correlation heatmap

Boxplots

2️⃣ Data Cleaning
Steps Performed:

Removed duplicate rows

Removed outliers using IQR method

Compared statistical summaries before and after cleaning

Impact:

Reduced extreme values

Improved dataset consistency

Stabilized feature distributions

3️⃣ Data Transformation

Performed after train-test split to prevent data leakage.

Train-Test Split:

80% Training

20% Testing

Stratified split to maintain class balance

Scaling Techniques:

Z-score Normalization (StandardScaler)

Min-Max Normalization

Observations:

Scaling changed feature ranges

Correlation structure remained unchanged

Standardization improved model stability

4️⃣ Feature Selection

Two methods were implemented:

🔹 Correlation-Based Selection

Selected features significantly correlated with target

🔹 Recursive Feature Elimination (RFE)

Selected top 5 most predictive features using Logistic Regression

Impact:

Reduced dimensionality

Minimal performance loss

Improved interpretability

5️⃣ Dimensionality Reduction (PCA)

Principal Component Analysis applied after scaling.

Reduced 11 features → 2 principal components

Preserved majority of dataset variance

Enabled 2D visualization of data

Observations:

Slight drop in accuracy due to compression

Significant dimensionality reduction achieved

📊 Model Performance Comparison

Logistic Regression was trained at multiple stages:

Dataset Stage	Description
Raw Scaled Data	All features after scaling
Correlation Selected	Reduced features via correlation
RFE Selected	Top 5 features via RFE
PCA	2 Principal Components

Performance comparison chart included in notebook.

📈 Key Learnings

Data cleaning improves reliability and robustness.

Scaling is critical for algorithms like Logistic Regression.

Feature selection reduces dimensionality with minimal performance loss.

PCA enables compression but may slightly reduce accuracy.

Structured preprocessing significantly affects model behavior.

🛠️ Technologies Used

Python

Pandas

NumPy

Matplotlib

Seaborn

Scikit-learn

📁 Repository Structure
Wine-Quality-Preprocessing/
│
├── winequality-red.csv
├── Wine_Preprocessing.ipynb
├── README.md
└── Report.pdf

🚀 How to Run

Clone the repository

Install required libraries

Open the notebook in Jupyter / Google Colab

Run cells sequentially

🎯 Project Outcomes

This project demonstrates:

End-to-end preprocessing workflow

Prevention of data leakage

Comparative model evaluation

Practical understanding of dimensionality reduction

Real-world ML pipeline implementation

👩‍💻 Authors

Mirunalini A.R.A – B.E CSE (AI & ML) – SCSVMV

Shivani Reddy – B.E CSE (Cybersecurity) – SCSVMV

📚 References

UCI Machine Learning Repository – Wine Quality Dataset

Scikit-learn Documentation

Pandas Documentation

⭐ Why This Project Matters

In real-world machine learning systems, preprocessing determines model success.
This project emphasizes structured, measurable preprocessing impact rather than blindly training models.
