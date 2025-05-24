# 📊 Student Performance Prediction

This project analyzes and predicts student performance using data from a Portuguese secondary school. It includes data preprocessing, feature engineering, exploratory analysis, and classification using multiple machine learning models.

## 📁 Project Structure

- `Student_Performance.ipynb` — Main Colab notebook (upload yours here)
- `student_performance_-_math.csv` — Dataset used for analysis (original source: MUNI)
- `README.md` — Project overview and usage instructions

## 🧠 Objectives

- Analyze student data to understand patterns and correlations.
- Predict final **grades** (classified into 5 buckets).
- Predict **pass/fail** status using ML models.

## 🧰 Technologies Used

- Python, pandas, NumPy, matplotlib, seaborn
- Scikit-learn (SVM, Random Forest, DummyClassifier, MLPClassifier)
- Data pipelines (StandardScaler, OneHotEncoder, OrdinalEncoder, SelectKBest, etc.)

## 🔍 Data Overview

The dataset contains information about students’ demographic, academic, and social background. Some key fields:

- `age`, `sex`, `address`, `studytime`, `failures`, `absences`, etc.
- Final grade: `G3` (used to derive custom `grades` and `passfail` features)

## ⚙️ Preprocessing Steps

- Handling missing values using `SimpleImputer`
- Converting object columns to categorical types
- Dropping unnecessary columns (`id`, `G1`, `G2`, `G3`)
- Feature engineering: converting numeric grades to categorical labels
- Creating data pipelines using `ColumnTransformer` and `Pipeline`

## 📈 Models Tested

| Model           | Task        | Accuracy |
|----------------|-------------|----------|
| Baseline       | Grades      | 20%      |
| Baseline       | Pass/Fail   | 46%      |
| SVM (RBF)      | Grades      | **53%**  |
| SVM (RBF)      | Pass/Fail   | **77%**  |
| Random Forest  | Grades      | 41%      |
| Random Forest  | Pass/Fail   | **77%**  |
| Neural Network | Pass/Fail   | 62%      |

## 📊 Visualizations

- Box plots and pair plots of numeric data
- Correlation heatmaps
- Bar charts comparing accuracy across models

## 📌 Key Insights

- SVM and Random Forest were best for pass/fail prediction (~77% accuracy)
- Predicting exact grades is more difficult; best was ~53% accuracy with SVM
- Data preprocessing and feature selection played a crucial role

## 🚀 How to Run

1. Upload the dataset: `student_performance_-_math.csv`
2. Open the Colab notebook: `Student_Performance.ipynb`
3. Run all cells in order to:
   - Clean and preprocess the data
   - Train and evaluate machine learning models
   - Visualize the results

## 📄 License

This project is for educational and research purposes. Dataset comes from an academic resource (Masaryk University - IS.muni.cz).

---

Feel free to customize this further if you add more models, optimize hyperparameters, or publish it on GitHub.
