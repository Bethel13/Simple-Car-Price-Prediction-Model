# Used Car Price Prediction 

A complete supervised machine learning regression project to predict the selling price of used cars using features like age, mileage (Kms Driven), present price, fuel type, transmission, seller type, and owner history.

Built end-to-end in Jupyter Notebook with scikit-learn



- Model: RandomForestRegressor (baseline — easy to upgrade to XGBoost/CatBoost)
- Train/Val/Test split: 80% / 10% / 10%
- Test set results (typical range on this dataset):
  - MAE: ~₹90,000 – ₹150,000
  - RMSE: ~₹140,000 – ₹220,000
  - R²: 0.85 – 0.93


## Dataset

- Filename: `car data.csv`
- Typical source: Cardekho / popular Kaggle-style used car dataset (~301 rows)
- Target variable: `Selling_Price` (in ₹ lakhs)
- Features usually include:
  - `Car_Name`
  - `Year` → engineered into `Age`
  - `Present_Price` (ex-showroom price in ₹ lakhs)
  - `Kms_Driven`
  - `Fuel_Type` (Petrol / Diesel / CNG)
  - `Seller_Type` (Dealer / Individual)
  - `Transmission` (Manual / Automatic)
  - `Owner` (0 / 1 / 3+ previous owners)

## What's Inside

- Full exploratory data analysis (EDA)
- Cleaning & feature engineering (age calculation, handling missing/outliers)
- 80/10/10 stratified split (train / validation / test)
- Scikit-learn Pipeline with:
  - Numeric scaling (StandardScaler)
  - Categorical one-hot encoding
  - RandomForestRegressor (plug-and-play — swap easily)
- Evaluation: MAE, RMSE, R² on validation + test sets
- Visuals: actual vs predicted scatter plot
- Ready for experimentation (log transform, hyperparameter tuning, better models, etc.)

## Project Folder Structure

used-car-price-prediction/  
├── car data.csv                        # the dataset  
├── Used_Car_Price_Prediction.ipynb     # main notebook with everything  
├── README.md                           # ← you are here  
└── requirements.txt                    # (optional — create if you want)

## How to Run This Project Locally

1. Clone the repository  
   ```bash
   git clone https://github.com/Beezthedev/used-car-price-prediction.git
   cd used-car-price-prediction

(Recommended) Create & activate virtual environment  bash

python -m venv venv
# Windows:
venv\Scripts\activate
# macOS/Linux:
source venv/bin/activate

Install dependencies  bash

pip install pandas numpy matplotlib seaborn scikit-learn

(or if you add a requirements.txt file later:)bash

pip install -r requirements.txt

Launch Jupyter Notebook  bash

jupyter notebook

→ Open Used_Car_Price_Prediction.ipynb → Run → All Cells

Technologies / StackPython 3.8+
pandas & numpy (data handling)
matplotlib & seaborn (visualization)
scikit-learn (pipelines, RandomForest, metrics)
Jupyter Notebook (development environment)


  
X / Twitter: @Beezthedev

