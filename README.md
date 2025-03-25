 Garments Worker Productivity Analysis

Project Overview

This project investigates how various factors, such as overtime, incentives, and departmental performance, affect worker productivity in a garment manufacturing environment. The dataset includes information on different workers across several departments, providing insights into how production targets are met and how various operational factors influence worker output.
 Dataset:
Rows: 1197
Columns: 15
Key Columns:
   `targeted_productivity`: The target productivity level set for workers.
  `actual_productivity`: The actual productivity achieved by workers.
  `overtime`: The amount of overtime worked (in minutes).
  `incentive`: The incentive paid to workers.
  `smv`, `wip`, `idle_time`, `no_of_workers`: Other operational factors.

Techniques Applied

The following techniques were applied during this project:

 1. Exploratory Data Analysis (EDA):
- Summarizing the Data: Descriptive statistics and data summaries using `df.describe()` and `df.info()`.
- Visualizing Data: Histograms and a correlation matrix to examine the relationships between different numerical variables.
- Pattern Recognition: Identified patterns in the data, such as the correlation between `overtime` and `actual_productivity`.

 2. Data Cleaning and Transformation:
- Handling Missing Values: Missing values in `wip` were filled with the median value.
- Data Type Correction: Converted the `date` column from a string to `datetime` type.
- Outlier Removal**: Used the IQR method to remove outliers from the data to avoid skewed results.
- Removing Unrealistic Values: Removed rows where values in columns such as `no_of_workers` or `incentive` were unrealistic (negative values).

3. Data Visualization:
- Visualizing Key Insights:
  - Bar plots comparing `targeted_productivity` vs `actual_productivity`.
  - Scatter plots showing relationships between `overtime` and `actual_productivity`, as well as `incentive` and `actual_productivity`.
  - Line plot to observe trends in `actual_productivity` across different quarters.
  
 4. Aggregation and Grouping:
- Aggregation: Calculated the mean of all numeric columns to get an overall sense of the data.
- Grouping: Grouped data by `department` and performed aggregations like the mean of `actual_productivity` and the sum of `overtime`.
- Pivot Tables: Created pivot tables to examine `actual_productivity` across different departments and quarters.

How to Run the Code

1. Clone the Repository:

    git clone https://github.com/your-username/garment-productivity-analysis.git
    cd garment-productivity-analysis
    ```
2. Install Required Libraries:
    The project requires the following libraries:
    - pandas
    - numpy
    - matplotlib
    - seaborn

    Install them using `pip`:

    pip install -r requirements.txt
    ```

3. Run the Jupyter Notebook:
    Open the Jupyter Notebook (`.ipynb`) file in Jupyter Notebook or JupyterLab:
    ```
    jupyter notebook
    ```
 Project Structure
.
├── data
│   └── garments_worker_productivity.csv
├── notebooks
│   └── garments_worker_productivity_analysis.ipynb
├── images
│   └── targeted_productivityVS_actual_productivity.png
│   └── overtime_vs_actual_productivity.png
│   └── correlation_matrix.png
│   └── departmental_performance.png
│   
├── src
│   └── data_cleaning.py
│   
├── requirements.txt
└── README.md
