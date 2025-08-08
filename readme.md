# Titanic Survival Prediction

This project explores the Titanic dataset to predict passenger survival using various machine learning models. It includes Exploratory Data Analysis (EDA), preprocessing, and the implementation of multiple classification algorithms — including ensemble and stacking techniques — to evaluate and compare performance.

## Dataset

The dataset is the classic **Titanic dataset** from [Kaggle](https://www.kaggle.com/c/titanic), which contains information about passengers on the Titanic, such as age, sex, class, and whether they survived.

---

## Project Structure

- **EDA & Preprocessing**: Cleaning missing values, encoding categorical variables, feature engineering.
- **Model Training**:
  - Decision Tree
  - Random Forest
  - Support Vector Machine (SVM)
  - Ensemble (Voting Classifier)
  - Stacking Classifier
- **Evaluation**: Each model was evaluated using cross-validation and tested on a held-out test set.

---

## Models & Performance

### 1. **Decision Tree**
- **Best Parameters**: `criterion='gini'`, `min_samples_leaf=4`
- **CV Score**: 0.787
- **Test Accuracy**: 76.8%
- **Highlights**:
  - Precision for class 1: 0.79
  - Recall for class 1: 0.53

---

### 2. **Random Forest**
- **Best Parameters**: `criterion='entropy'`, `max_depth=5`, `min_samples_leaf=2`, `n_estimators=50`
- **CV Score**: 0.787
- **Test Accuracy**: 81.7%
- **Highlights**:
  - Precision for class 1: 0.85
  - Recall for class 1: 0.63

---

### 3. **SVM (Linear Kernel)**
- **Best Parameters**: `C=0.1`, `kernel='linear'`
- **CV Score**: 0.798
- **Test Accuracy**: 78.3%
- **Highlights**:
  - Precision for class 1: 0.74
  - Recall for class 1: 0.66

---

### 4. **Voting Classifier (Ensemble)**
- **Base Models**: Decision Tree, Random Forest, SVM
- **Test Accuracy**: 80.3%
- **Highlights**:
  - Balanced performance
  - Precision for class 1: 0.81
  - Recall for class 1: 0.63

---

### 5. **Stacking Classifier**
- **Base Models**: Decision Tree, Random Forest, SVM  
- **Final Estimator**: Logistic Regression
- **Test Accuracy**: 78.2%
- **Highlights**:
  - Precision for class 1: 0.74
  - Recall for class 1: 0.66

---

## Conclusion

- **Best Performer**: Random Forest with 81.7% accuracy
- Ensemble models provided robust and consistent performance, combining the strengths of individual classifiers.
- Precision and recall trade-offs show different strengths across models depending on the business or real-world importance (e.g., minimizing false negatives).

---

## 🛠️ Technologies Used

- Python
- Pandas, NumPy
- Scikit-learn
- Matplotlib, Seaborn (for EDA)
