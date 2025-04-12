# **Project Overview**

This project focuses on predicting liver disease based on medical data. Various machine learning algorithms are used to classify individuals as either having liver disease or not, based on several medical features. The goal is to build an effective predictive model that can assist medical professionals in diagnosing liver-related conditions.

---

## **Requirements**

To run this project, make sure the following Python libraries are installed:

- **pandas** – For data manipulation and analysis  
- **numpy** – For numerical operations  
- **matplotlib** – For data visualization  
- **seaborn** – For enhanced visualizations  
- **scikit-learn** – For machine learning algorithms and tools  
- **imbalanced-learn** – For handling imbalanced datasets (e.g., SMOTE for oversampling)  
- **xgboost** – For gradient boosting classification

To install all required dependencies, you can use the `requirements.txt` file by running:

```bash
pip install -r requirements.txt
```

---

## **Dataset**

The dataset includes medical features such as:

- Age  
- Gender  
- Bilirubin levels  
- Albumin level  
- Alkaline phosphatase  
- SGOT (AST)  
- SGPT (ALT)  
- Total protein  
- Prothrombin time  
- And more...

The target variable is the **presence of liver disease**, formatted as a binary classification task (0 = No disease, 1 = Liver disease).

---

## **Steps to Run the Project**

1. **Load the data**  
   Load the liver disease dataset using pandas and explore it:

   ```python
   import pandas as pd
   df = pd.read_csv('liver_disease.csv')
   ```

2. **Data Preprocessing**  
   Proper data preparation is crucial and includes handling missing values, scaling features, and balancing the dataset.

3. **Train Machine Learning Models**  
   The following models were trained and evaluated:

   - `DecisionTreeClassifier`  
   - `RandomForestClassifier`  
   - `XGBClassifier`  
   - `KNeighborsClassifier`  
   - `MLPClassifier`  

4. **Model Evaluation**  
   Models were evaluated on the test set using the following metrics:

   - **Accuracy** – The proportion of correct predictions  
   - **Recall** – The model’s ability to identify liver disease cases  
   - **Precision** – The model’s ability to correctly classify positive cases  
   - **F1 Score** – The balance between precision and recall  
   - **ROC-AUC** – Area under the ROC curve

5. **Hyperparameter Tuning**  
   Model performance was further improved using hyperparameter optimization techniques such as:

   - `GridSearchCV` (grid search)
   - `RandomizedSearchCV` (randomized search)

---

## **Conclusion**

This project demonstrates the potential of machine learning for predicting liver disease. Several models were tested, and results show that ensemble methods like Random Forest and XGBoost outperform individual classifiers in terms of accuracy and other performance metrics.

---

## **Future Improvements**

Potential future enhancements include:

- Collecting a larger dataset to improve model generalization  
- Exploring more advanced models such as deep neural networks  
- Applying more sophisticated techniques for handling class imbalance

---

## **How to Run**

1. **Clone the repository:**

   ```bash
   git clone <your_repository_link>
   cd <your_project_directory>
   ```

2. **Install dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

3. **Run the notebook or Python script for data analysis and model training:**

   ```bash
   jupyter notebook
   ```
