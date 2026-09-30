# Assignment---5---DataPreprocessing
Performed complete data preprocessing using Python, Pandas, NumPy, Matplotlib, and Seaborn. Handled data inspection, column renaming, categorical value correction, missing values, duplicates, and statistical analysis. Identified and handled extreme outliers while preserving meaningful raw-data variations.
# DataPreprocessingAssignment
# Task 1 – Data Loading & Inspection
1) Load the dataset using Pandas --> read csv file
2) Display: head(), tail(), shape, columns, info(), dtypes --> printed shape, head, tail, columns, info,
dtypes, describe, unique valuess
3) Identify numerical and categorical columns --> num_cols and cat_cols contains numerical and categorical columns
# Task 2 – Data Cleaning
● Rename Columns: Update column names such as 'ID' to 'Visit_ID' and 'No_Pation' to
'Patient_ID' to make them more descriptive and clear. --> Using Rename updated the column name
● Check Unique Values in Categorical Columns: Identify the unique values in categorical
columns:
○ Gender: F (Female) & M (Male),
○ CLASS: N (No diabetes), P (Pre-diabetes), Y (Yes, Diabetes). --> Removed extra spaces, converteed upper case, Corrected the gender and class values
# ● Statistical Summary of Numerical Columns: Generate a statistical summary 
(mean,median, min, max, standard deviation) for all numerical columns to gain insights into
the data's distribution. --> got the statistical summary for numerial columns and plotted hist plot for all numerical columns
plt.subplot(2, 5)
# ● Box Plot of Numerical Columns: -->
box plotted for all numerical columns using sns.boxplot(data=df[cols])
# ● Identify Missing (Null) Values:--> 
identified missing values using df.isnull().sum()
# ● Impute Missing Values:
Using imputer filled missing values with median for numerical columns and mode for categorical columns
# ● Duplicate Handling:
found duplicate values and dropped it
# Task 3 – Outlier Handling
# Retain outlier -->
just found the outlier for Age,Hba1c,bmi didnt remove it as it is to be preserved because its raw customer data that could be very low or very high.
# filter cr and urea -->
found 99.9 and 99.5 percentile first. Then found values that exceed it. filtered it from the df.
# ● Remove Extreme Outliers: -->
Removed extreme outliers for (LDL, VLDL, HDL, TG, Chol)
# Task 4 – Data Transformation
# ● Feature Engineering: --> 
used label encoding for Gender column as asked F-->0 M-->1
# ● Feature Scaling:-->
Standard scaling choosed because we have extreme outliers and distributions
