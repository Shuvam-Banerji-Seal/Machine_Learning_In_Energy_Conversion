# Notes on "Power consumption forecast" Jupyter Notebook

## Overview
This Jupyter notebook demonstrates the application of machine learning for power consumption forecasting using historical energy data from PJM Interconnection LLC, a regional transmission organization in the United States.

## Key Components

### Libraries and Tools Used
- **pandas**: For data manipulation and analysis
- **numpy**: For numerical operations
- **matplotlib**: For data visualization
- **seaborn**: For statistical data visualization
- **scikit-learn**: Implied for machine learning models

### Dataset
- Hourly power consumption data from PJM's website in megawatts (MW)
- Dataset covers multiple years (2002-2018) for the Eastern Interconnection grid
- Serves regions including Delaware, Illinois, Indiana, Kentucky, Maryland, Michigan, New Jersey, North Carolina, Ohio, Pennsylvania, Tennessee, Virginia, West Virginia, and DC

### Data Preprocessing Steps
1. **Data Cleaning**:
   - Checking for null/NaN values
   - Identifying and removing duplicated datetimes
   - Verifying data time frequency (hourly)
   - Handling missing datetimes through reindexing and interpolation

2. **Feature Engineering**:
   - Extracting temporal features from datetime index:
     - hour
     - day of week
     - day of month
     - day of year
     - quarter
     - month
     - year
     - week of year

3. **Exploratory Data Analysis**:
   - Visualizing hourly, daily, and monthly power consumption patterns
   - Using boxplots to understand distribution across different time periods
   - Identifying seasonal patterns and trends

4. **Outlier Analysis**:
   - Detecting outliers using quantile-based approach
   - Identifying values below 1% quantile and above 99% quantile
   - Visualizing outliers through scatter plots

### Key Observations
- Daily power consumption peaks typically occur between 5:00 PM and 8:00 PM
- Lowest demand occurs during late-night hours (2:00 AM to 5:00 AM)
- Power consumption is highest during summer months (June, July, August)
- Data contains outliers that require special handling

### Machine Learning Approach
- The notebook prepares data for supervised learning models like XGBoost and Random Forest
- Time series data is transformed into a features/target format suitable for ML models
- Temporal features are used to capture patterns and seasonality in power consumption

## Reference
GitHub Repository: kaymen99/AI-for-energy-sector
Notebook: Power consumption forecast.ipynb
