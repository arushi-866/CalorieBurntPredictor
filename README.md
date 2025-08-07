# Calorie Burnt Predictor 


This project uses machine learning to predict the number of calories a person burns during a workout. By analyzing user attributes and exercise data, an **XGBoost Regressor model** is trained to provide accurate calorie expenditure estimates.

***

## Project Overview

The core of this project is to build a regression model that learns the relationship between various physiological features and the total calories burned. The process involves data exploration, preprocessing, model training, and evaluation.

### **1. Data Exploration & Visualization**
The relationships between different features and calorie expenditure were analyzed. A **correlation heatmap** was used to understand the linear relationships between variables, guiding feature selection. It revealed that `Duration`, `Heart_Rate`, and `Body_Temp` have the strongest positive correlations with `Calories`.



### **2. Preprocessing**
* Categorical features like `Gender` were converted into a numerical format (`'male': 0`, `'female': 1`).
* Non-informative features like `User_ID` were dropped before training.

### **3. Model Training & Evaluation**
The dataset, consisting of 15,000 samples, was split into training (80%) and testing (20%) sets. An **XGBoost Regressor** was trained on the data. The model's performance was evaluated on the unseen test data using the **Mean Absolute Error (MAE)** metric.

***

##  Results

The trained model can predict calorie expenditure with a **Mean Absolute Error (MAE) of approximately 15.6**. This means, on average, the model's prediction is off by about 16 calories, which indicates a strong performance for this task.



***

##  Technologies Used

* **Programming Language:** Python
* **Libraries:**
    * **Pandas:** For data manipulation and analysis.
    * **NumPy:** For numerical operations.
    * **Matplotlib & Seaborn:** For data visualization.
    * **Scikit-learn:** For splitting the dataset and evaluating the model (`train_test_split`, `mean_absolute_error`).
    * **XGBoost:** For the core regression model (`XGBRegressor`).
* **Environment:** Google Colab

***
