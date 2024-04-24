1. Load both datasets (main_data.xlsx and supplementary_data.xlsx)
2. Merge the two datasets using "id" as key
3. Rename the column "F_5" to "feature_5" in the new dataset
4. Extract the year from the column "date" and name it as "year"
5. Categorize "year" into groups (2000-2006,2007-2010,2011-2022), and summarize the mean value of 'feature_4' by year groups.
6. Identify missing values for "feature_2". Then, for each "id", impute the missings with the value from previous year, if not available, use the value from next year. Name the new feature "feature_2_impute". 
7. Drop those observations with "feature_5" is "F"
8. Winsorize "feature_3" by limiting the extreme values to 1 percentile (left tail) and 99 percentile (right tail). Name it "feature_3_winsor". 
9. Split the dataset into training and testing datasets using 70:30 split ratio
10. Build a logistic regression on the training set to predict 'y' being (90+DPD) using "feature_1", "feature_2_impute", "feature_3_winsor". "feature_4" as independent variables.
11. report AUC and RMSE of the training set and testing set.
