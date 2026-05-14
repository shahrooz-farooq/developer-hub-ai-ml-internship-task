# Task 1: Exploring and Visualizing a Simple Dataset

## Task Objective
The objective of this task is to load, explore, and visualize the Iris dataset to understand its structure, statistical properties, and relationships between different features. This is an **Exploratory Data Analysis (EDA)** project.

## Dataset Used
- **Dataset Name**: Iris Dataset
- **Source**: Seaborn built-in dataset
- **Description**: Contains measurements of iris flowers from 3 different species (Setosa, Versicolor, Virginica)
- **Total Samples**: 150 rows
- **Features**: 
  - sepal_length
  - sepal_width
  - petal_length
  - petal_width
  - species (target variable)

## Data Exploration Steps
1. **Data Loading**: Loaded Iris dataset using seaborn.load_dataset()
2. **Shape & Structure**: Analyzed dataset dimensions and column names
3. **Statistical Summary**: Calculated mean, median, standard deviation, min, max for all features
4. **Data Types**: Identified numeric and categorical columns
5. **Missing Values**: Checked for any missing or null values

## Visualizations Created
1. **Scatter Plot**: Shows relationship between sepal_length and petal_length with species differentiation
2. **Histogram**: Displays distribution of all numerical features across 150 samples
3. **Box Plot**: Identifies outliers and shows data spread for each feature

## Model Applied
**No Machine Learning Model** - This is purely an Exploratory Data Analysis (EDA) project focused on understanding data characteristics and relationships.

## Key Findings
1. The Iris dataset contains 150 complete records with no missing values
2. Three distinct iris species are well-separated based on flower measurements
3. Petal measurements (petal_length, petal_width) show strong correlation with species type
4. Sepal measurements have less distinction between species compared to petal measurements
5. Data is well-distributed with no significant outliers detected
6. Clear visual clustering patterns visible in scatter plots suggesting good separability for classification

## Libraries Used
- **pandas**: Data manipulation and analysis
- **seaborn**: Statistical data visualization
- **matplotlib**: Plotting and visualization

## Files in This Task
- `Exploring and Visualizing a Simple Dataset.py`: Main Python script containing all analysis and visualizations

## How to Run
```bash
python "Exploring and Visualizing a Simple Dataset.py"
```

## Output
The script produces three interactive visualizations:
- Scatter plot showing sepal measurements by species
- Histogram showing distribution of all numeric features
- Box plot showing outliers and data spread
