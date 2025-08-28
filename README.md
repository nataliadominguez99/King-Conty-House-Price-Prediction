# 🏡 King County House Prices Analysis 

Analyzing house sale prices across King County from May 2014 to May 2015 to uncover market trends and build predictive models for real estate valuation with Machine Learning.  

---

## 📂 Dataset Description

- **Dataset Source:** King County – House Sales (2014–2015)  
- **Size:** ~21,600 rows × 21 columns

- **Key Features:**  
- `id`: Unique house identifier  
- `date`: Date of sale  
- `price`: Sale price (target variable)  
- `bedrooms`, `bathrooms`: Property characteristics  
- `sqft_living`, `sqft_lot`, `sqft_above`, `sqft_basement`: Living space and land area  
- `floors`, `waterfront`, `view`, `condition`, `grade`: Quality indicators  
- `yr_built`, `yr_renovated`: Construction/renovation history  
- `zipcode`, `lat`, `long`: Location data  
- `sqft_living15`, `sqft_lot15`: Average size of nearby properties
  
**Notable Quirks:**
- Dates needed formatting for consistency.  
- Outliers present in `bedrooms` and `bathrooms` (e.g., extreme values).  
- Missing or 0 values in `yr_renovated` indicate houses never renovated.  
- Large variation in lot sizes required transformation for analysis.  

---

## 🎯 Research Goal

The goal of this project is to **predict house prices** using property features, identify the most influential variables, and understand market dynamics in King County.  


---

## 🛠 Steps Taken

## 🛠 Steps Taken

1. **Data Cleaning**
  - Converted `date` column to datetime format
  - Handled missing values, duplicates, and inconsistent data types
  - Treated outliers in `bedrooms`, `bathrooms`, and `sqft_lot`

2. **Exploratory Data Analysis (EDA)**
  - Analyzed distributions of features and target (`price`)
  - Checked correlations and multicollinearity
  - Identified data quality issues for preprocessing

3. **Feature Engineering & Preparation**
  - Defined target (`y = price`) and predictors (`X`)
  - No categorical encoding was required
  - Prepared datasets for model training/testing

4. **Modeling**
  - Performed train-test split
  - Applied multiple models:
    - Linear Regression
    - AdaBoost
    - XGBoost
    - Random Forest
    - Gradient Boosting
    - CatBoost
  - Compared results across models

5. **Model Evaluation & Improvement**
  - Metrics: RMSE, MAE, R²
  - Linear Regression performed the weakest
  - XGBoost, Random Forest, and CatBoost gave the best results
  - CatBoost achieved the highest overall accuracy
  - Improvements included cleaning, handling multicollinearity, and testing additional algorithms

---

## 📌 Main Findings
- The location of the property (lat) is one of the strongest drivers of house prices.
- Size and quality (sqft_living, grade) are key features influencing value.
- Number of bedrooms and floors have little impact compared to other variables.
- Boosting models (XGBoost, CatBoost) consistently outperform simple linear regression.
- CatBoost provided the most accurate predictions, with the best R² and MSE scores.

---

## 💻 How to Reproduce

**Prerequisites:**
- Python **3.10+**
- Libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`

**Run Instructions:**
1. **Clone this repository**
   ```bash
   git clone https://github.com/nataliadominguez99/King-Conty-House-Price-Prediction.git

2. **Navigate to the project folder**
   ```bash
    cd King-Conty-House-Price-Prediction

3. **Open the Jupyter Notebook**
- If you use Jupyter Notebook:
   ```bash
   jupyter notebook "King_countryproject.ipynb"
- Or, open it in VSCode by double-clicking the file or using:
   ```bash
    code "King_countryproject.ipynb"
  
4. **Ensure the dataset is in the correct location**
- The file sales_data_sample.csv must be in the same directory as the notebook.

5. **Run all cells**
- Select Cell > Run All in Jupyter Notebook or VSCode to reproduce the analysis.

## 🚀 Next Steps

- Incorporate external data (interest rates, economic indicators).
- Build a web app to predict house prices from user inputs.
- Perform time-series analysis of house prices over multiple years.  

---

## 📁 Repo Structure
```bash
├── King County Real Estate Market Analysis Pres...   # Project presentation (PDF/PowerPoint)  
├── King_countryproject.ipynb                        # Jupyter Notebook with analysis and modeling    
└── king_country_houses_aa.csv                       # Dataset used in the analysis     
