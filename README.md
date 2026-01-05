![Rossmann Logo](img/Logo_rossmann_2024.svg)

# Rossmann Sales Forecasting

## 1. Business Problem
Rossmann is a large pharmacy retail chain with **3,000+ stores across 7 European countries**.  
Store managers were asked to **predict daily sales for the next six weeks** for each store.

Sales performance is influenced by multiple factors such as:
- promotions
- competition
- holidays
- seasonality
- store location
- assortment size

Given this context, the goal of this project is to develop a **reliable sales forecasting solution** that meets stakeholder expectations and supports strategic decision-making at the store level.

During the problem exploration phase, several business questions were raised, including:

1. Do stores with a larger product assortment sell more?
2. Do stores with closer competitors sell less?
3. Do stores with long-established competitors sell more?
4. Do stores with long-running promotions sell more?
5. Do stores with consecutive promotions perform better?
6. Do stores open on holidays sell more?
7. Are stores selling more over the years?
8. Do stores sell less during holiday or vacation periods?

These and other questions were explored throughout the project and helped guide the development of the final solution.

---

## 2. Assumptions and Data Context
- Public datasets provided on **Kaggle** were used for model training and to simulate a production environment.
- Columns with missing values were analyzed individually, and specific imputation strategies were defined for each case.
- Business hypotheses were structured around five main dimensions:
  - customers
  - location
  - stores
  - products
  - seasonality
- The dataset covers the period from **early 2013 to mid-2015**.

---

## 3. Solution Strategy
The solution was developed following the **CRISP-DM methodology**, using a cyclical and iterative approach.

A Python notebook was created covering the entire data science workflow, including:
- Data description and cleaning
- Feature engineering
- Variable filtering
- Exploratory Data Analysis (EDA)
- Data preparation
- Feature selection
- Machine learning modeling
- Hyperparameter fine-tuning
- Error translation and business interpretation
- Model deployment

All these steps are documented in the project notebook.

In addition to the analytical notebook, two production components were developed:
- a **web API** to serve the trained model
- a **Telegram Bot** that allows stakeholders to request real-time sales predictions by simply sending a store ID

This setup simulates a real-world production environment, enabling fast and practical access to model predictions.

---

## 4.Tech Stack

The following tools and libraries were used throughout the project, from data analysis to model deployment:

### Data Analysis & Machine Learning
- **Python** – core programming language
- **Pandas** – data manipulation and feature engineering
- **NumPy** – numerical computing
- **Scikit-learn** – preprocessing, feature selection, model evaluation, and baseline models
- **XGBoost** – gradient boosting model used for sales forecasting
- **Boruta** – feature selection
- **SciPy** – statistical analysis
- **Joblib / Pickle** – model serialization

### Data Visualization & EDA
- **Matplotlib** – static visualizations
- **Seaborn** – exploratory data analysis and statistical plots

### Backend & Deployment
- **Flask** – API development for model serving
- **Requests** – HTTP communication
- **Telegram Bot** – real-time interaction with stakeholders

### Utilities
- **Inflection** – feature and column name standardization
- **Tabulate** – structured tabular outputs
- **Warnings** – warning management during experiments


---

## 5. Top 3 Data Insights
1. Stores with a **larger product assortment tend to sell less**, contradicting initial expectations.
2. Stores with **long-running promotions start to experience declining sales after a certain period**, suggesting promotion fatigue.
3. Overall, stores are **selling less over the years**, indicating the need for a deeper investigation into structural or market-related issues affecting the retail network.

---

## 6. Final Product
The final solution consists of a **production-ready API** and a **Telegram Bot**.

This architecture allows the model to remain online and generate predictions quickly and efficiently.

- API project: https://github.com/alefaizi/pa_rossmann_webapp  
- Telegram Bot project: https://github.com/alefaizi/pa_rossmann_telegram  

### Telegram Bot Example
![Telegram Bot Example](img/bot.jpg)

---

## 7. Conclusion
The objective of this project was to develop a **practical and scalable solution** to forecast sales for a multinational pharmacy retail chain.

The proposed solution enables decision-making related to:
- budgeting
- store positioning
- operational and strategic actions at the store level

By simply sending a store number to the Telegram Bot, stakeholders receive a **six-week sales forecast** for that specific store.

Working on this project significantly strengthened my data science skills and provided hands-on experience in building APIs and deploying machine learning models in a production-like environment, closely aligned with real-world industry scenarios.

---

## 8. Next Steps
- Run a new CRISP-DM cycle with additional experiments and ML algorithms to further improve model accuracy and robustness.
- Develop new business hypotheses and dive deeper into the data to uncover insights that can help improve the model.
- Enhance the Telegram Bot with more interaction options and additional information for stakeholders to query.
