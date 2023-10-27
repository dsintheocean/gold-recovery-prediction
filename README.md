# Gold Recovery Prediction in the Mining Industry

## Project Description
A machine learning model is being developed for an industrial company that provides solutions for the efficient operation of industrial enterprises.  
The model aims to predict the recovery rate of gold from gold-bearing ore based on data with parameters related to extraction and purification processes.  
The model will help optimize production to avoid starting operations with unprofitable characteristics.  
The data is timestamped and extracted raw from the enterprise's DCS system.  

The quality metric used is sMAPE (Symmetric Mean Absolute Percentage Error).  
The goal is to predict two target features simultaneously:  
- Rougher concentrate recovery efficiency.  
- Final concentrate recovery efficiency.
  
The final metric is a combination of these two values.

## Key Findings
A comprehensive data preprocessing was performed, including outlier removal, missing value imputation, and feature scaling. Feature correlations were investigated.  
Changes in the concentrations and total concentrations of gold, silver, and lead were studied across successive stages of the purification and enrichment process.  
The distribution of raw material granule sizes in the training and testing datasets was examined.  
A function to calculate the final sMAPE was created.  

The best sMAPE value on the test dataset for the target feature "rougher.recovery" (8.563) was achieved using a Linear Regression model.  
The best sMAPE value on the test dataset for the target feature "final.recovery" (9.925) was achieved using a Decision Tree Regression model with the following parameters:  
- Criterion: 'friedman_mse'
- Max Depth: 3
- Min Samples Split: 2

The final sMAPE on the test dataset is 9.584.

## Additional Information
Toolkit: Matplotlib, Seaborn, NumPy, Pandas, Python, Scikit-learn, EDA, Data Preprocessing.
