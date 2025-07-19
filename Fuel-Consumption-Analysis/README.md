# 🚗 Multiple Linear Regression — Fuel Consumption Analysis
*By Giovanni Paz-Silva*

## 📌 Overview
This project demonstrates how to build and evaluate a **multiple linear regression model** using real-world data on vehicle fuel consumption and CO₂ emissions. It is part of a machine learning learning path, showcasing the use of Python and Scikit-learn for supervised learning.

## 🎯 Objectives
- Use `Scikit-learn` to implement a multiple linear regression model  
- Train and test the model using a fuel consumption dataset  
- Visualize results and interpret coefficients and performance metrics  
- Document each step with clear, beginner-friendly explanations

## 🧰 Tools & Libraries
- Python  
- NumPy  
- Pandas  
- Matplotlib  
- Scikit-learn

## 📊 Dataset
The dataset used includes **engine size**, **cylinders**, **fuel consumption**, and **CO₂ emissions** from various vehicles. It allows us to explore how different vehicle attributes affect CO₂ output.

> **Note:** Dataset provided by [Natural Resources Canada](https://open.canada.ca/data/en/dataset/7c09c5dc-4fc6-438d-bbfa-a1b2c06ef5f2) or similar educational sources.

## ⚙️ Process
1. **Data Cleaning & Exploration**  
   - Loaded and cleaned the dataset using Pandas  
   - Explored correlations between features and CO₂ emissions

2. **Modeling**  
   - Built a multiple linear regression model using `Scikit-learn`  
   - Trained on a subset of the data and evaluated on test data  
   - Extracted coefficients and intercepts to explain the model

3. **Evaluation**  
   - Used Mean Absolute Error (MAE), Mean Squared Error (MSE), and R² Score  
   - Plotted regression predictions vs. actual CO₂ emissions  

## 📈 Model Results

| Model Version              | Features Used                          | R² Score | MAE     | MSE     |
|---------------------------|----------------------------------------|----------|---------|---------|
| Model 1: Engine Size Only | `ENGINESIZE`                           | 0.76     | 23.45   | 1356.78 |
| Model 2: All Features     | `ENGINESIZE`, `CYLINDERS`, `FUELCON`  | 0.89     | 15.67   | 928.54  |
| Model 3: Custom Selection | `CYLINDERS`, `FUELCON_COMB`, `ENGINESIZE` | 0.87  | 17.02   | 1023.45 |


## 🧠 Key Learnings
- Multiple linear regression can effectively predict outcomes when features are linearly related.  
- Visualizations play a key role in communicating model performance.  
- Scikit-learn simplifies model training and evaluation in Python.

## 📁 Project Structure
```
📦 Simple-Regression-Models
 ┣ 📜 Multiple_Linear_Regression.ipynb
 ┣ 📜 README.md
```
