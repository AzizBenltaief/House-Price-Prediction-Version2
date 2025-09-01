# 🏠 California Housing Price Prediction

This project predicts median house values in California districts using the **California Housing Dataset**.  
It includes **data exploration, preprocessing, feature engineering, and model training** with both **Linear Regression** and **Random Forest** (with hyperparameter tuning).

---

## 📌 Project Overview
- **Dataset**: [California Housing dataset](https://www.kaggle.com/datasets/camnugent/california-housing-prices)  
- **Goal**: Predict `median_house_value` from housing-related features.  
- **Tech stack**: Python, Pandas, NumPy, Matplotlib, Seaborn, Scikit-Learn.  

---

## 🔎 Steps in the Workflow

### 1. Data Exploration
- Loaded dataset (`housing.csv`)  
- Checked missing values and distributions  
- Plotted histograms & correlations (heatmap)

### 2. Data Preprocessing
- Removed rows with missing values (`total_bedrooms`)  
- Log-transformed skewed features:
  - `total_rooms`, `total_bedrooms`, `population`, `households`  
- Converted categorical column `ocean_proximity` into **one-hot encoded 0/1 features**  
- Train/test split  

### 3. Feature Engineering
- Created new meaningful features:
  - `bedroom_ratio = total_bedrooms / total_rooms`  
  - `household_rooms = total_rooms / households`  

### 4. Modeling
- **Linear Regression**  
  - Trained on standardized data  
  - Baseline performance  
- **Random Forest Regressor**  
  - Strong non-linear model  
  - GridSearchCV used to tune hyperparameters (`n_estimators`, `max_features`)  
  - Achieved **~0.94 R² score** on test data 🎯  

---

## 📊 Results
- Linear Regression: ✅ Works but underfits  
- Random Forest: ✅ Best performance (~94% accuracy on test set)  
