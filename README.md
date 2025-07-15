# Cafe-Sales-Data-Cleaning-and-Explatory-Data-Analysis


This project involves cleaning and performing exploratory data analysis on a dataset of cafe sales. The goal is to identify patterns, trends, and insights from the sales data.

## Dataset

The dataset used in this project is sourced from Kaggle: ["Cafe Sales Dirty Data for Cleaning Training"](https://www.kaggle.com/datasets/ahmedmohamed2003/cafe-sales-dirty-data-for-cleaning-training). It contains raw sales data with various inconsistencies and missing values, requiring cleaning before analysis.

## Project Steps

1.  **Data Loading**: The dataset was downloaded from Kaggle using the `kagglehub` library and loaded into a pandas DataFrame.
2.  **Data Cleaning**:
    *   Column names were cleaned by replacing spaces with underscores and capitalizing the first letter.
    *   Data types for numerical and date columns were converted to appropriate types, handling errors by coercing invalid values to NaN.
    *   'UNKNOWN' and 'ERROR' values in the dataset were replaced with NaN.
    *   Missing values in 'Location' and 'Payment_method' were filled using the mode.
    *   Missing 'Price_per_unit' values were imputed where possible using 'Total_spent' and 'Quantity'.
    *   Missing 'Item' values were imputed based on the calculated 'Price_per_unit'.
    *   Rows with missing values in columns with less than 10% missing data were dropped.
3.  **Exploratory Data Analysis (EDA)**:
    *   Basic data information (`df.info()`) and descriptive statistics (`df.describe()`) were examined.
    *   The shape of the cleaned data was checked.
    *   Total revenue was calculated.
    *   Sales performance by item was analyzed to identify top and bottom-selling items.
    *   Datetime features (Year, Month, Day, Hour, Weekday, Day Type) were extracted from the 'Transaction_date' column.
    *   Monthly sales trends were visualized.
    *   The distribution of 'Total_spent' was analyzed using a histogram.
    *   Box plots were used to visualize the distribution of 'Total_spent' by 'Item' and the distributions of numerical variables ('Quantity', 'Price_per_unit', 'Total_spent').
    *   Sales were compared between weekdays and weekends.
    *   Item sales were compared between weekdays and weekends.
    *   The distribution of total spent by categorical variables ('Item', 'Payment_method', 'Location') was visualized.
    *   A correlation heatmap was generated for numerical variables to understand relationships.
    *   A scatter plot and pair plot were created to visualize the relationships between 'Quantity', 'Price_per_unit', and 'Total_spent'.

## Key Findings

*   The dataset initially contained several data quality issues, including inconsistent column names, incorrect data types, and missing values represented by NaN, 'UNKNOWN', and 'ERROR'.
*   After cleaning, the dataset was ready for analysis with appropriate data types and handled missing values.
*   The total revenue generated during the period was calculated.
*   Specific items were identified as top and bottom performers in terms of total sales.
*   Monthly sales trends showed variations throughout the year.
*   The distribution of total spent was right-skewed, indicating that most transactions were for smaller amounts.
*   Box plots revealed variations in spending across different items and the spread of numerical variables.
*   Interestingly, weekday sales were higher than weekend sales.
*   Analysis of item sales by day type showed how different items performed on weekdays versus weekends.
*   Visualizations of categorical variables provided insights into sales distribution by item, payment method, and location.
*   The correlation analysis showed the relationships between numerical variables.

## Technologies Used

*   Python
*   pandas
*   numpy
*   matplotlib
*   seaborn
*   missingno
*   mplcursors
*   plotly (although not used in the final plots, it was considered for interactive visualization)
