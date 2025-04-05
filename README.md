# 🧠 Alphabet Soup Charity Funding Prediction  
## Deep Learning Model Report

---

## 📌 Overview of the Analysis

The purpose of this analysis is to create a machine learning model that predicts whether charitable funding provided by Alphabet Soup will be successful. Using a dataset of over 34,000 organizations, we leveraged a deep learning approach to build a binary classifier. The aim was to assist the company in making smarter investment decisions by identifying which applicants are most likely to use funds successfully based on their historical and categorical attributes.

---

## 📊 Results

### 🔄 Data Preprocessing

- **Target Variable**  
  The target variable is `IS_SUCCESSFUL`, which is labeled `1` for organizations that successfully used their funding, and `0` otherwise.

- **Feature Variables**  
  All other variables—after dropping irrelevant columns and encoding categorical variables—were used as features to train the model. These included application type, classification, income amount, and more.

- **Removed Variables**  
  The `EIN` and `NAME` columns were removed because they serve only as identifiers and do not contribute predictive value.

---

### 🏗️ Compiling, Training, and Evaluating the Model

- **Neural Network Architecture**  
  - Input layer: 80 neurons (matching number of features)  
  - Hidden layers: 30 and 15 neurons with **ReLU** activation  
  - Output layer: 1 neuron with **sigmoid** activation  

  This structure was chosen to balance complexity with generalization.

- **Model Performance**  
  The best-performing model reached an accuracy of **72.7%**, falling just short of the 75% target.

- **Optimization Attempts**  
  - Removed additional columns: `AFFILIATION`, `SPECIAL_CONSIDERATIONS`, `USE_CASE`, `ORGANIZATION`  
  - Filtered for common application types and classifications  
  - Tested alternative activation functions such as `tanh`  
  - Adjusted layer depth and neuron counts  
  - Scaled input data and rebalanced class distribution  

  Some of these adjustments resulted in lower performance, with accuracy dropping to around **63%** in certain runs.

---

## ✅ Summary and Recommendation

After extensive tuning, the highest accuracy achieved by the deep learning model was **72.7%**. While reasonably accurate, it did not meet the 75% performance goal.

### 🔁 Alternative Model Suggestion

A **Random Forest Classifier** was also tested and achieved a higher accuracy of **76.6%**, making it a more promising option for this type of dataset.

#### Why Use Random Forest?
- Better performance with tabular, mixed-type data  
- More robust to noise and outliers  
- Handles categorical variables with less preprocessing  
- Easier to interpret using feature importance metrics  

---

## 📸 Optional Visualizations

> (Include visuals such as training/validation loss plots, confusion matrix, or feature importance charts here, if available.)

