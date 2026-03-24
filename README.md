
### 🎗️ Breast Cancer Prediction 

## 📌 Project Overview
This project applies Machine Learning models to predict whether a breast cancer tumor is **Benign (B)** or **Malignant (M)** based on medical features extracted from digitized images of fine needle aspirates (FNA) of breast masses. 

## 📊 Dataset Description
* **Total Samples:** 569 
* **Features:** 30 numerical features (e.g., radius, texture, perimeter, area, smoothness, etc.)
* **Target Variable:** `diagnosis` (M = Malignant, B = Benign)
* **Data Quality:** Clean dataset with **0 missing values**.

## 🛠️ Tech Stack & Dependencies
* **Data Manipulation:** `pandas`, `numpy`
* **Data Visualization:** `matplotlib`, `seaborn`
* **Machine Learning:** `scikit-learn` (Logistic Regression, SVC, Random Forest)

## 🔮 Future Improvements
To further enhance this project, the following steps can be taken:
* **Feature Scaling:** Apply `StandardScaler` from Scikit-Learn to normalize the features. This will fix the Logistic Regression convergence warning and drastically improve the accuracy of the SVC model!
* **Hyperparameter Tuning:** Use `GridSearchCV` to optimize the Random Forest and SVC parameters.

## 🚀 Workflow Methodology
1. **Data Collection & Cleaning:** Loaded the `breast_cancer.csv` dataset and dropped the non-predictive `id` column.
2. **Exploratory Data Analysis (EDA):** Visualized the distribution of the cancer stages (Benign vs. Malignant) using a Seaborn countplot.
3. **Data Splitting:** Separated the features (`X`) and the target labels (`y`), then split the data into **90% Training** and **10% Testing** sets.
4. **Model Training:** Trained three different classifiers to compare performance:
   * Logistic Regression
   * Support Vector Classifier (SVC)
   * Random Forest Classifier
5. **Model Evaluation:** Evaluated the models using accuracy scores and a Confusion Matrix heatmap.

## 📈 Model Performance & Results
The models were evaluated on the 10% unseen test data. Here are the accuracy results:

| Model | Training Accuracy | Testing Accuracy |
| :--- | :--- | :--- |
| **Logistic Regression** | 91.60% | 94.73% |
| **SVC** | 62.10% | 68.42% |
| **Random Forest** | **100.00%** | **96.49%** |

🏆 **Best Performing Model:** The **Random Forest Classifier** achieved the highest testing accuracy (~96.5%), making it the most reliable model for this specific pipeline.

> **Note on Convergence:** You may notice a `ConvergenceWarning` with the Logistic Regression model. This indicates that the numerical features (like `area` vs `smoothness`) are on vastly different scales. 



