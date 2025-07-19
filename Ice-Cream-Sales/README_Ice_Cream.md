# 🍦 Ice Cream Sales Prediction — Simple Linear Regression
*By Giovanni Paz-Silva*

## 📌 Overview
This project demonstrates how to build and interpret a **simple linear regression model** using real-world-inspired data: daily temperature vs. ice cream sales. It is part of an educational machine learning path focusing on foundational regression techniques using Python and Scikit-learn.

## 🎯 Objectives
- Implement a simple linear regression model using `Scikit-learn`  
- Train and test the model using temperature vs. sales data  
- Visualize the regression line and evaluate the model’s accuracy  
- Clearly document each step to demonstrate conceptual understanding

## 🧰 Tools & Libraries
- Python  
- NumPy  
- Pandas  
- Matplotlib  
- Scikit-learn

## 📊 Dataset
The dataset contains paired values of **daily temperature (°C)** and **ice cream sales (USD)**. The goal is to explore how strongly temperature affects consumer behavior in ice cream purchases.

## ⚙️ Process
1. **Data Preparation**  
   - Loaded the dataset with Pandas  
   - Checked for missing values and explored feature correlation

2. **Model Building**  
   - Applied simple linear regression using `Scikit-learn`  
   - Trained the model on part of the data and tested on the rest  
   - Generated predictions based on temperature

3. **Evaluation**  
   - Evaluated performance using **R² score**, **Mean Absolute Error (MAE)**, and **Mean Squared Error (MSE)**  
   - Visualized the **regression line** and model **fit**

## 📈 Results
- The regression model showed a strong positive correlation between **temperature and ice cream sales**.  
- The **R² score** of approximately **0.976** indicates that temperature is a good predictor of sales.  
- Visual inspection confirmed that the model generalizes well to the test data.

## 🧠 Key Learnings
- Simple linear regression is an effective baseline for predictive modeling when there is a strong linear relationship between two variables.  
- Even a basic model can yield meaningful insights when paired with thoughtful data exploration and visualization.  
- Scikit-learn’s simplicity makes it easy to focus on learning the core regression concepts.

## 📁 Repository Structure

```
📦 Ice-Cream-Sales-Prediction
 ┣ 📜 Ice-Cream_Linear_Regression.ipynb
 ┣ 📜 README.md
 ┗ 📊 data/
```
