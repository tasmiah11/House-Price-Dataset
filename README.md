# House-Price-Dataset
# House Price Prediction - Exploratory Data Analysis (EDA)

## Overview
This is the **Ames, Iowa House Price Dataset** EDA analysis! This project explores **1,460 houses** with **80 different features**, ranging from lot size to garage details, to understand what drives house prices. Through **Exploratory Data Analysis (EDA)**, we uncover key trends, relationships, and insights that can help predict house prices effectively.

## About the Dataset
- **Source**: Kaggle - Ames Housing Dataset
- **Target Variable**: `SalePrice` (House Sale Price in USD)
- **Total Features**: 80 (38 numerical, 43 categorical)
- **Observations**: 1,460 homes

## Data Overview
### **Numerical Features**
- **House & Property Details**: Lot size, year built, basement area, living space, number of rooms, garage area
- **Amenities & Outdoor Features**: Decks, porches, pools, fireplaces
- **Sale Information**: Year and month sold

### **Categorical Features**
- **Zoning & Location**: Neighborhood, condition, zoning classification
- **Design & Construction**: House style, roof type, exterior material
- **Utilities & Features**: Heating type, garage quality, kitchen rating, sale type

## Exploratory Data Analysis (EDA) Insights
### **1️⃣ Missing Values & Data Cleaning**
- Columns with **>50% missing data** (`Alley`, `PoolQC`, `Fence`) were removed.
- Missing values in key numerical columns were filled using **median imputation**.

### **2️⃣ Outliers & Distributions**
- **Right-Skewed Data**: Sale prices, lot sizes, basement areas, and living spaces have a long tail of high values.
- **Outliers Identified**: Certain homes have **very large lot areas, basements, and garages**, making them potential luxury properties.

### **3️⃣ Correlation Analysis**
- **Strongest Positive Correlations**:
  - **Overall Quality** (`OverallQual`) vs. **Sale Price** (0.8) → Higher quality homes are more expensive.
  - **Living Space** (`GrLivArea`) vs. **Sale Price** (0.7) → Bigger houses tend to cost more.
  - **Garage Size** (`GarageCars`, `GarageArea`) → More garage space = higher value.
- **Weak Correlations**:
  - **Year Sold** (`YrSold`) vs. **Sale Price** (0.0) → Selling year has no impact on price.
- **Negative Correlations**:
  - **House Age** (`GarageYrBlt` & `OverallQual`) (-0.4) → Older homes tend to be lower quality.

## Hypothesis Testing Results
✅ **Hypothesis 1**: Higher quality houses have **higher sale prices** → Confirmed! Homes rated 7+ in quality sell at much higher prices.
✅ **Hypothesis 2**: Houses sold in **summer months (May - July) have higher sale prices** → Confirmed! Summer sales tend to fetch **better prices** than winter ones.

## Visualizations
- **Histograms**: Show the distribution of property features.
- **Boxplots**: Identify outliers in `LotArea`, `GrLivArea`, `TotalBsmtSF`.
- **Bar Charts**: Compare `OverallQual` & `MoSold` against `SalePrice`.
- **Scatterplots**: Explore relationships between house features & price.
- **Heatmap**: Visualizes correlation among key numerical variables.

## Key Takeaways
- **Bigger, newer, and higher-quality homes sell for more.**
- **Features like garage size, basement space, and living area significantly impact house prices.**
- **Seasonality affects house prices – summer sales tend to be higher.**
- **Outliers (luxury homes) can skew price predictions and should be handled properly.**

### **Requirements**
- Pandas, NumPy, Matplotlib, Seaborn

### Repository Structure
README.md: This file.
Src/: Jupyter notebooks detailing the EDA process.
Docs/: Scripts used for data cleaning and visualization.
Results/: Output visualizations and statistical analysis results.
