# Customer Churn Analysis and Prediction

## Project Background
This project focuses on **customer churn analysis** for a telecom firm. Churn analysis helps identify customers likely to leave the service, enabling businesses to take preventive actions. The project uses machine learning techniques to predict churn and visualize critical patterns using **Power BI**. Although tailored for the telecom industry, these techniques can be applied to other domains, such as retail, finance, and healthcare, to enhance customer retention strategies.
[dashboard](images/1.png)
## Insights and Recommendations
Insights and recommendations are provided across the following key areas:

1. **Demographic Analysis**
2. **Geographic Trends**
3. **Payment and Account Details**
4. **Service Usage and Preferences**

## Data Structure & Initial Checks
The main database consists of four tables, loaded and processed via an ETL pipeline in SQL Server:

- **Customer Demographics**: Gender, age, marital status, and location.
- **Account Information**: Contract type, tenure, and payment method.
- **Service Details**: Internet type, phone services, and additional services.
- **Churn Indicators**: Customer status, churn category, and churn reason.


## Executive Summary
This project identified key factors influencing churn, including:
- Customers with **month-to-month contracts** had the highest churn rate compared to those with annual contracts.
- Older customers aged **50+** were more likely to churn than younger age groups.
- Customers in regions like **Jammu & Kashmir** and **Assam** showed significantly higher churn rates.

These findings empower marketing teams to design targeted retention campaigns.  

## Insights Deep Dive

### **Demographic Analysis**
- **Insight 1**: Female customers churned 15% more than male customers.
- **Insight 2**: Customers aged **50+** have a churn rate of 35%, the highest among age groups.

### **Geographic Trends**
- **Insight 1**: Top regions with high churn rates are **Jammu & Kashmir** and **Assam**.
- **Insight 2**: States with the lowest churn rates include **Kerala** and **Tamil Nadu**.

### **Payment & Account Details**
- **Insight 1**: Customers using **Mailed Check** as a payment method showed higher churn rates.
- **Insight 2**: Customers with **month-to-month contracts** showed the highest churn rates, while those with **2-year contracts** churned the least.

### **Service Usage**
- **Insight 1**: Customers without additional services like **Online Backup** or **Device Protection Plan** had higher churn rates.
- **Insight 2**: Users with **Fiber Optic Internet** had a higher churn rate compared to DSL users.

## Recommendations
Based on the analysis, the following actions are recommended:
- Offer incentives like discounts to customers on **month-to-month contracts** to shift them to annual plans.
- Target customers aged **50+** with loyalty rewards and personalized support.
- Improve customer satisfaction in regions with higher churn rates, such as **Jammu & Kashmir** and **Assam**.
- Promote bundled service plans to encourage adoption of **Online Backup** and **Device Protection Plans**.

## Assumptions and Caveats
1. Missing data (e.g., null values in key columns) was handled by imputation or exclusion.
2. Customer churn reasons were grouped into categories for simplicity.
3. Monthly charge ranges were segmented into predefined brackets for analysis.
4. Predictions were made using the **Random Forest Classifier** with an 80-20 train-test split.

## Metrics
The following key metrics were calculated:
- **Total Customers**: 6,418
- **Total Churned Customers**: 1,732
- **Churn Rate**: 27%
- **New Joiners**: 411

## Steps for Implementation

### Step 1: ETL Process in SQL Server
- Load the data into SQL Server using the Import Wizard.
- Perform initial exploration with SQL queries to understand the data structure and null values.

### Step 2: Data Transformation
- Create views in SQL Server for Power BI visualization.
- Transform columns into meaningful groups (e.g., age groups, tenure groups).

### Step 3: Machine Learning
- Use the **Random Forest Classifier** to predict churn.
- Save predictions to a CSV file for further analysis.

### Step 4: Power BI Dashboard
- Visualize customer churn trends by demographic, geographic, and account details.
- Create a **Predicted Churners** dashboard to identify at-risk customers.

![dashboard](images/1.png)(images/2.png)

## Tools & Technologies
- **SQL Server**: For data storage and ETL pipeline.
- **Power BI**: For creating interactive dashboards.
- **Python**: For building the machine learning model.
- **Random Forest**: Used for churn prediction.

---

Feel free to adapt this project for your business needs. If you have any questions, feel free to reach out or explore the repository for additional details.
