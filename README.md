# Housing Data Analysis - README

## Dataset Description

This dataset contains housing market information from California, including various property characteristics and their corresponding median house values. The data is structured for regression analysis to predict housing prices based on multiple features.

### Data Features

- **longitude**: Longitudinal coordinate of the property
- **latitude**: Latitudinal coordinate of the property  
- **housing_median_age**: Median age of houses in the area
- **total_rooms**: Total number of rooms in the area
- **total_bedrooms**: Total number of bedrooms in the area (contains some missing values)
- **population**: Population in the area
- **households**: Number of households in the area
- **median_income**: Median income of households (in tens of thousands)
- **median_house_value**: Target variable - Median house value for the area
- **ocean_proximity**: Categorical variable indicating proximity to ocean (NEAR BAY, <1H OCEAN, INLAND)

### Dataset Characteristics
- Contains geographic, demographic, and housing-specific features
- Mixed data types: numerical and categorical
- Some missing values present in `total_bedrooms` column
- Target variable: `median_house_value`

## Normal Steps for Machine Learning Models

### 1. Data Preprocessing
- **Handle missing values**: Impute or remove missing data in `total_bedrooms`
- **Feature engineering**: Create new features like rooms_per_household, bedrooms_per_room, population_per_household
- **Encode categorical variables**: Convert `ocean_proximity` using one-hot encoding or label encoding
- **Feature scaling**: Standardize or normalize numerical features for models sensitive to scale

### 2. Exploratory Data Analysis (EDA)
- Visualize distributions of features and target variable
- Analyze correlations between features and target
- Identify outliers and understand data patterns
- Explore geographic patterns using longitude and latitude

### 3. Data Splitting
- Split data into training, validation, and test sets (typically 70-15-15 or 80-20)
- Use stratified sampling if dealing with imbalanced data
- Ensure temporal consistency if time is a factor

### 4. Model Selection & Training
**Common models for regression tasks:**
- **Linear Regression**

### 5. Model Evaluation
**Regression metrics:**
- Root Mean Squared Error (RMSE)
- R-squared (R²)
