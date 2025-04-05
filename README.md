# Deep-Learning-Challenge

Deep Learning Model Report

📌 Overview of the Analysis

The purpose of this analysis is to create a machine learning model that predicts whether charitable funding provided by Alphabet Soup will be successful. Using a dataset of over 34,000 organizations, we leveraged a deep learning approach to build a binary classifier. The aim was to assist the company in making smarter investment decisions by identifying which applicants are most likely to use funds successfully based on their historical and categorical attributes.

📊 Results

Data Preprocessing
🔹 What variable(s) are the target(s) for your model?
The target variable is IS_SUCCESSFUL, which is labeled 1 for organizations that successfully used their funding, and 0 otherwise.
🔹 What variable(s) are the features for your model?
All other variables—after dropping irrelevant columns and encoding categorical variables—were used as features to train the model. These included application type, classification, income amount, and more.
🔹 What variable(s) should be removed from the input data because they are neither targets nor features?
The EIN and NAME columns were removed because they serve only as identifiers and do not contribute predictive value.
Compiling, Training, and Evaluating the Model
🔹 How many neurons, layers, and activation functions did you select for your neural network model, and why?
The base model consisted of:
Input layer with 80 neurons (based on number of features)
Hidden layers with 30 and 15 neurons, using ReLU activation
Output layer with 1 neuron and sigmoid activation
This architecture was chosen to balance model complexity and generalization performance.
🔹 Were you able to achieve the target model performance?
The goal was to reach at least 75% accuracy. The best-performing neural network model achieved approximately 72.7%, which fell slightly short.
🔹 What steps did you take in your attempts to increase model performance?
Several strategies were tested:
Dropped additional columns that may have added noise (AFFILIATION, SPECIAL_CONSIDERATIONS, etc.)
Filtered out low-frequency application types and classifications
Changed activation functions (from relu to tanh)
Experimented with deeper networks and more neurons
Scaled and rebalanced the data
Despite these efforts, further optimization led to decreased performance, with one configuration dropping to 63% accuracy.
✅ Summary and Recommendation

After testing various neural network configurations, the model achieved a best-case accuracy of 72.7%. While this result indicates that the neural network was able to capture meaningful patterns in the data, it did not meet the performance target of 75%.

🔁 Alternative Model Suggestion
Given the nature of the dataset—which includes many categorical variables and a mix of numeric types—a Random Forest Classifier may be more suitable. In testing, a Random Forest model achieved approximately 76.6% accuracy, outperforming the neural network.

Why Random Forest?

Handles categorical variables better with less preprocessing
More robust to outliers and noise
Performs well with tabular data
Easier to interpret through feature importance metrics
