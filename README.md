# ![CI logo](https://codeinstitute.s3.amazonaws.com/fullstack/ci_logo_small.png)


# Credit Card Customer Churn Analysis

## Project Overview

This project analyses credit card customer data to identify the main factors associated with customer churn and predict customers at risk of leaving.

The project combines ETL, exploratory data analysis (EDA), machine learning, and Power BI to generate actionable insights that can support customer retention strategies.
## Business Problem

Customer churn can negatively affect revenue and long-term customer relationships. This project investigates customer behaviour to identify the main drivers of churn and support targeted retention decisions.
## Project Objectives

- Analyse customer churn patterns and key drivers.
- Explore customer demographic and behavioural factors.
- Build and compare machine learning models for churn prediction.
- Identify the most important predictive features.
- Present key insights through an interactive Power BI dashboard.
## Dataset

Dataset used: Credit Card Customer Churn Dataset  
Source: Kaggle  
Format: CSV  
Records: 10,127 customers  
Target variable: Churn  

https://www.kaggle.com/datasets/sakshigoyal7/credit-card-customers

 ## Ethics and Responsible Use

This project uses a public dataset from Kaggle for educational and analytical purposes.

The analysis focuses on customer churn patterns and does not attempt to identify individual customers. The results should be used to support business decisions rather than make decisions about customers solely based on model predictions.
## Project Hypotheses

The following hypotheses were investigated to identify key factors associated with customer churn:

1. **Customer Inactivity**  
   Customers with longer periods of inactivity are more likely to churn.

2. **Transaction Frequency**  
   Customers with lower transaction frequency are more likely to churn.

3. **Transaction Amount**  
   Customers with lower transaction amounts are more likely to churn.

4. **Credit Utilisation**  
   Credit utilisation differs significantly between existing and churned customers.
## Methodology

The project follows an end-to-end data analytics workflow:

### 1. ETL and Data Preparation
- Loaded the raw CSV dataset from Kaggle.
- Assessed missing values, duplicates and data quality.
- Removed unnecessary Naive Bayes classifier columns.
- Retained relevant `Unknown` categories to avoid unnecessary data loss.
- Created the binary `Churn` target variable.
- Saved the cleaned dataset for further analysis.

### 2. Exploratory Data Analysis (EDA)
- Analysed customer demographics, financial characteristics and behaviour.
- Compared existing and churned customers.
- Conducted statistical hypothesis testing.
- Identified important churn patterns and potential risk factors.

### 3. Machine Learning
- Built Logistic Regression and Random Forest classification models.
- Evaluated models using Accuracy, Precision, Recall, F1 Score and ROC-AUC.
- Compared model performance and analysed feature importance.

### 4. Power BI
- Developed an interactive three-page dashboard.
- Presented churn KPIs, customer segments, churn drivers and predictive insights.
- Added interactive filters to support business exploration.
## Machine Learning Results

Two classification models were developed and compared:

| Model | Accuracy | Precision | Recall | F1 Score | ROC-AUC |
|---|---:|---:|---:|---:|---:|
| Logistic Regression | 90.0% | 76.8% | 53.8% | 63.3% | 91.7% |
| **Random Forest** | **95.2%** | **93.2%** | **75.4%** | **83.3%** | **98.4%** |

### Selected Model

**Random Forest** was selected as the final model because it achieved stronger overall performance and identified a higher proportion of churned customers.

The model achieved **95.2% accuracy** and **98.4% ROC-AUC**, demonstrating strong predictive performance.
## Key Insights

The analysis identified several important patterns associated with customer churn:

- **Customer inactivity:** Churned customers showed higher levels of inactivity.
- **Transaction frequency:** Customers with fewer transactions were more likely to churn.
- **Transaction amount:** Churned customers generally had lower transaction amounts.
- **Credit utilisation:** Differences in credit utilisation were observed between existing and churned customers.
- **Customer engagement:** Overall behavioural activity was more informative for churn risk than demographic characteristics.

These findings suggest that changes in customer engagement and transaction behaviour can provide useful early indicators of churn.

## Power BI Dashboard

### Page 1 — Executive Overview

![Executive Overview](dashboard/1%20executive_overview.png)

### Page 2 — Churn Drivers

![Churn Drivers](dashboard/2%20churn_drivers.png)

### Page 3 — Predictive Insights

![Predictive Insights](dashboard/3%20predictive_insights.png)

### Dashboard File


https://app.powerbi.com/links/DCSm2gQA7F?ctid=c233c072-135b-431d-af59-35e05babf941&pbi_source=linkShare

## Business Recommendations

Based on the analysis and predictive results, the following actions are recommended:

- Prioritise customers with low transaction activity for retention campaigns.
- Monitor customers showing increasing inactivity.
- Target high-risk customer segments with personalised offers and engagement strategies.
- Use the churn prediction model to support early identification of customers at risk of leaving.
## Project Structure

```text
credit-card-customer-churn-analysis/
│
├── dashboard/
│   ├── credit_card_churn_dashboard.pbix
│   ├── 1 executive_overview.png
│   ├── 2 churn_drivers.png
│   ├── 3 predictive_insights.png
│   └── model view.png
│
├── data/
│   ├── raw/
│   │   └── BankChurners.csv
│   └── processed/
│       └── bank_churners_clean.csv
│
├── jupyter_notebooks/
│   ├── 01_ETL.ipynb
│   ├── 02_EDA.ipynb
│   └── 03_ML.ipynb
│
├── README.md
├── requirements.txt
└── .gitignore
```
## Technologies Used

- **Python** – data processing, analysis and machine learning
- **Pandas & NumPy** – data manipulation and numerical analysis
- **Matplotlib & Seaborn** – data visualisation
- **Scikit-learn** – machine learning and model evaluation
- **Power BI** – interactive dashboard and business insights
- **Jupyter Notebook** – ETL, EDA and ML development
- **Git & GitHub** – version control and project management
- **VS Code** – development environment
## How to Run the Project

1. Clone the repository:

   git clone https://github.com/sepidehsomeh/credit-card-customer-churn-analysis.git

2. Install the required dependencies:

   pip install -r requirements.txt

3. Run the Jupyter notebooks in the following order:

   - `01_ETL.ipynb`
   - `02_EDA.ipynb`
   - `03_ML.ipynb`

4. To explore the dashboard, open:

   ` https://app.powerbi.com/links/DCSm2gQA7F?ctid=c233c072-135b-431d-af59-35e05babf941&pbi_source=linkShare`

   using **Power BI Desktop**.
## Testing and Validation

The project was validated throughout the analytics workflow:

- Data quality checks were performed for missing values, duplicates and data types.
- Statistical hypothesis tests were used to validate relationships identified during EDA.
- Machine learning models were evaluated on a separate test dataset.
- Accuracy, Precision, Recall, F1 Score and ROC-AUC were used for model comparison.
- Power BI visuals, filters and relationships were tested to ensure consistent results.
## Conclusion

This project demonstrates an end-to-end data analytics workflow for understanding and predicting credit card customer churn.

The analysis identified customer engagement and transaction behaviour as important indicators of churn. The Random Forest model provided strong predictive performance, while the Power BI dashboard translated the findings into clear and actionable business insights.
## Future Improvements

Future development of the project could include:

- Testing additional machine learning models and tuning model parameters.
- Using more recent or larger customer datasets.
- Deploying the predictive model for real-time churn prediction.
- Integrating new customer data into the Power BI dashboard.
- Developing automated alerts for customers with high churn risk.
## Credits and Acknowledgements

- Dataset sourced from **Kaggle**.
- This project was developed as part of the **Data Analytics with AI** programme at **Code Institute**.
- Special thanks to my instructor, **Vasi**, for his guidance, support, and feedback throughout the project.
- Analysis, machine learning, Power BI dashboard development, and project documentation completed by **Sepideh Someh**.

