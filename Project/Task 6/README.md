# Task 6: House Price Prediction

## Task Objective
The objective of this task is to predict house prices using a machine learning regression model. The model analyzes various house features (both numeric and categorical) to accurately estimate the selling price of houses.

## Dataset Used
- **Dataset Name**: House Price Prediction Dataset
- **File**: House Price Prediction Dataset.csv
- **Location**: Task 6/ directory
- **Total Samples**: Multiple rows of house data
- **Features**: Mix of numeric (area, rooms, etc.) and categorical (location, type, etc.) variables
- **Target Variable**: Price (house selling price to predict)

### Feature Categories:
- **Numeric Features**: Area, rooms, bedrooms, bathrooms, age, etc.
- **Categorical Features**: Location, house type, condition, etc.

## Data Preparation
1. **Data Loading**: Loaded CSV file using pandas
2. **Data Cleaning**: 
   - Removed ID column (not useful for prediction)
   - Identified target column (Price)
3. **Feature Separation**: Separated features (X) from target (y)
4. **Missing Value Handling**: 
   - Numeric features: Filled with mean values
   - Categorical features: Filled with most frequent values
5. **Encoding**: Converted categorical text data to numeric using OneHotEncoder
6. **Scaling**: Normalized numeric features using StandardScaler
7. **Data Split**: 80% training (544 rows) and 20% testing (136 rows)

## Model Applied
**Random Forest Regressor**
- **Type**: Ensemble Learning, Regression
- **Configuration**:
  - Number of trees (n_estimators): 200
  - Random state: 42 (for reproducibility)
  
### Why Random Forest?
- Handles both numeric and categorical data well
- Captures non-linear relationships in data
- Robust to outliers
- Provides good generalization on real-world datasets
- Better accuracy than simple linear models for house price prediction

## Model Architecture
The model uses a Pipeline with:
1. **Preprocessing Stage**: 
   - Numeric transformer (SimpleImputer + StandardScaler)
   - Categorical transformer (SimpleImputer + OneHotEncoder)
   - ColumnTransformer combines both
2. **Prediction Stage**: Random Forest Regressor (200 trees)

## Results

### Model Evaluation Metrics:
- **Mean Absolute Error (MAE)**: Average absolute error in price prediction
- **Root Mean Squared Error (RMSE)**: Square root of average squared errors (penalizes large errors more)

### Predictions:
- Model generates price predictions for all test samples
- Comparison DataFrame shows Actual vs Predicted prices

### Visualization:
- **Scatter Plot**: Shows relationship between actual and predicted prices
- **Perfect Prediction Line**: Diagonal line representing ideal predictions
- **Interpretation**: Points closer to the diagonal line indicate better predictions

## Key Findings
1. Random Forest model successfully learns patterns in house pricing
2. Model demonstrates reasonable prediction accuracy on test data
3. Feature preprocessing (scaling and encoding) improves model performance
4. The ensemble approach (200 trees) provides robust predictions
5. Scatter plot reveals model's performance distribution across price ranges

## Model Performance Interpretation
- **Low MAE/RMSE**: Model predictions are close to actual prices
- **High Residuals**: Indicates properties with unique characteristics not well-captured by features
- **Outliers**: Some houses may have unusual prices due to special circumstances

## Advantages of Random Forest for House Price Prediction
1. Automatically handles feature interactions
2. Provides feature importance rankings
3. Robust to outliers and missing patterns
4. No need for explicit feature scaling in tree-based algorithms
5. Can capture non-linear relationships in housing market

## Libraries Used
- **pandas**: Data loading and manipulation
- **numpy**: Numerical computations
- **sklearn.preprocessing**: Data scaling and encoding
- **sklearn.compose**: ColumnTransformer for combined preprocessing
- **sklearn.pipeline**: Pipeline for model workflow
- **sklearn.ensemble**: RandomForestRegressor model
- **sklearn.metrics**: Evaluation metrics (MAE, RMSE)
- **matplotlib**: Data visualization

## Files in This Task
- `house_price_prediction.py`: Main Python script for house price prediction
- `House Price Prediction Dataset.csv`: Dataset containing house features and prices

## How to Run
```bash
python house_price_prediction.py
```

## Output
- **Console Output**:
  - First 5 rows of dataset
  - Dataset information (columns, data types)
  - Missing values summary
  - Numeric and categorical features list
  - Training completion message
  - Model evaluation metrics (MAE, RMSE)
  - Actual vs Predicted prices comparison table

- **Visualization**:
  - Scatter plot comparing actual vs predicted house prices
  - Diagonal reference line for perfect predictions
  - Clear visualization of model performance

## Future Improvements
1. Hyperparameter tuning (grid search, random search)
2. Feature engineering (creating new features from existing ones)
3. Cross-validation for better performance estimation
4. Trying other models (Gradient Boosting, XGBoost, Neural Networks)
5. Feature importance analysis
6. Handling outliers in house prices
