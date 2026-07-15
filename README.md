# House_Price_Prediction-Machine_Learning

# Overview
This project applies data science and machine learning techniques to **predict house prices using the Kaggle dataset**. The workflow covers data cleaning, visualization, feature engineering, model building and evaluation.

# Tools & Libraries
•	**Python**: pandas, numpy, matplotlib, seaborn, scikit learn

•	**Jupyter Notebook** for experimentation

# Work Flow
**1.	Data Setup & Cleaning**
        •	Loaded Kaggle dataset (~1,460 rows, 80+ features).
        •	Handled missing values (dropped >50% missing, filled categorical with “None”, numerical with median.
  	
**3.	Outliers & Encoding**
        •	Log transformation of SalePrice to reduce skewness.
        •	Removed extreme outliers using IQR.
        •	Encoded categorical features with LabelEncoder.
  	
**5.	Feature Selection & Modeling**
        •	Selected top 20 correlated features.
        •	Compared Linear Regression (R² ≈ 0.70) vs Random Forest (R² ≈ 0.82).
        •	Pruned features below importance threshold (0.02).
  	
**7.	Evaluation & Conclusion**
        •	Residual analysis and noisy prediction filtering.
•	Cross validation (5 fold) → mean R² ≈ 0.83 (stable).
•	Random Forest (Full) chosen as best model.

# Models Used
**1.	Linear Regression**
        •	Baseline model for predicting house prices.
        •	Achieved R² ≈ 0.70, showing moderate accuracy but limited ability to capture complex relationships.
        
**2.	Random Forest Regressor (Full)**
        •	Ensemble model with 200 trees, max depth 15.
        •	Best performing model with R² ≈ 0.82, explaining ~82% of variance in house prices.
        •	Identified key predictors such as Overall Quality, Living Area, Garage Capacity, and Basement Size.
        
**3.	Random Forest Regressor (Pruned)**
        •	Features with importance < 0.02 were removed.
        •	Achieved R² ≈ 0.79 on test data, but showed stable generalization with mean R² ≈ 0.83 across 5 fold cross validation.
        •	Reduced complexity while maintaining strong performance.

# Key Insights
•	**Best Model** → Random Forest (Full) with ~82% variance explained.

•	**Stable Generalization** → Pruned Random Forest achieved mean R² ≈ 0.83 across 5 fold cross validation.

•	**Top Predictors** → Overall Quality, Living Area, Garage Capacity and Basement Size strongly influence house prices.

•	**Residual Analysis** → ~10% of predictions were noisy, but filtering improved model reliability.

        

