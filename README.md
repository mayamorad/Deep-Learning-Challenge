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
  - Input layer: 100 neurons  
  - Hidden layers: 30 and 10 neurons with **ReLU** and **sigmoid** activations  
  - Output layer: 1 neuron with **sigmoid** activation  

  This structure was selected to balance complexity and performance, while minimizing overfitting.

- **Model Performance**  
  - **Training Accuracy (Final Epoch)**: 81.15%  
  - **Test Accuracy**: **79.42%**  
  - **Test Loss**: 0.4568  
  The model came close to the 80% target and maintained consistent performance between training and test datasets.

- **Optimization Attempts**  
  - Removed additional non-contributing columns: `AFFILIATION`, `SPECIAL_CONSIDERATIONS`, `USE_CASE`, `ORGANIZATION`  
  - Filtered for common application types and classifications  
  - Experimented with different activation functions (e.g., `tanh`)  
  - Adjusted neuron count and network depth  
  - Tuned learning rate, batch size, and number of epochs  

  These adjustments helped fine-tune the model to achieve higher generalization accuracy.

---

## ✅ Summary and Recommendation

After multiple iterations, the deep learning model achieved a strong **79.42% accuracy** on unseen test data. This suggests that the model is fairly effective at identifying organizations likely to use funds successfully.

### 🔁 Alternative Model Suggestion

A **Random Forest Classifier** previously tested in the project produced an accuracy of approximately **76.6%**, which was slightly lower than the neural network. However, it requires less tuning and can be more interpretable for decision-making.

#### Why Consider Random Forest?
- Performs well with mixed-type tabular data  
- Robust to noise and outliers  
- Easier to interpret using feature importance metrics  
- Faster to train and less sensitive to parameter tuning  

For quick iteration or deployment in a low-resource environment, Random Forest could be a strong backup.
