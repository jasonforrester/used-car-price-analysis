# **Unlocking Insights into Used Car Prices: A Guide for Dealerships**

## **Overview**

This project focuses on analyzing a dataset of used cars to uncover the key factors that influence their pricing. By utilizing historical data and predictive modeling, this analysis provides actionable recommendations to help dealerships optimize inventory and pricing strategies.

The dataset, sourced from Kaggle, contains 426,000 records with details such as car make, model, year, mileage, fuel type, and additional attributes impacting value.

The note book of this code can be found here: [https://github.com/jasonforrester/used-car-price-analysis](https://github.com/jasonforrester/used-car-price-analysis/blob/main/prompt_II-final.ipynb)
---

## **Business Understanding**

Dealerships aim to maximize revenue by accurately pricing and selling vehicles efficiently. This project identifies the main factors affecting car prices to help dealerships:

- Stock vehicles that hold higher value.
- Develop strategic pricing models based on influential features.
- Reduce time-to-sale and inventory turnover rates.

---

## **Data Preparation**

### **Data Cleaning**

- Eliminated rows with missing critical data (e.g., `price`, `year`, `odometer`).
- Removed unrealistic entries, such as prices below $1,000 or exceeding $100,000.

### **Outlier Management**

- Identified and removed outliers by visualizing price distributions.

### **Feature Engineering**

- Added new variables like `car age` for enhanced analysis.
- Used OneHotEncoding to convert categorical variables into machine-readable formats.
- Filtered out low-variance features using a Variance Threshold technique.

---

## **Exploratory Data Analysis (EDA)**

- Visualized price distributions before and after data cleaning.
- Analyzed correlations between features using heatmaps.
- Identified key predictors like mileage, condition, and manufacturer as strong determinants of price.

---

## **Modeling Approach**

### **Models Tested**

1. **Linear Regression:** Simple baseline model.
2. **Lasso Regression:** Effective for handling multicollinearity.
3. **Random Forest Regression:** Accounts for non-linear relationships and feature importance.

### **Evaluation Metrics**

- Employed 5-fold cross-validation.
- Measured performance using Mean Squared Error (MSE) and R² scores.
- Fine-tuned hyperparameters for Lasso and Random Forest models using GridSearchCV.

---

## **Key Findings**

- **Age:** Cars that are newer consistently sell at higher prices.
- **Mileage:** Vehicles with lower odometer readings hold significantly more value.
- **Manufacturer:** Brands like Toyota and Honda command higher average resale values.
- **Condition:** Cars in "Excellent" condition are priced up to 40% more than those in "Fair" condition.
- **Fuel Type:** Hybrid and electric vehicles are valued higher than their gasoline counterparts.

---

## **Recommendations**

### **Stock Wisely**

- Prioritize vehicles with under 50,000 miles for resale.
- Focus on trusted brands like Toyota and Honda to ensure steady demand and resale value.

### **Develop Competitive Pricing**

- Leverage predictive models, such as Random Forest, to set dynamic, data-driven prices.
- Offer discounts for older vehicles, especially those over 10 years old, to incentivize faster sales.

### **Appeal to Buyers**

- Highlight features like fuel efficiency and all-wheel drive to cater to buyer preferences.
- Showcase eco-friendly vehicles, as hybrids and electric cars attract higher price points.

---

## **Next Steps**

1. **Incorporate Additional Data:** Include regional market trends and seasonal demand patterns.
2. **Test Advanced Models:** Experiment with Gradient Boosting or XGBoost for improved prediction accuracy.
3. **Increase Interpretability:** Apply SHAP values to better understand the impact of individual features on pricing.

---

## **Requirements**

### **Python Libraries Used**

- pandas  
- numpy  
- matplotlib  
- seaborn  
- scikit-learn  
- missingno
