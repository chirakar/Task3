# Final EDA Findings

## Dataset
- 564 production samples
- 334 features consisting of numerical, categorical, datetime, and time-series variables
- The dataset contains multiple binary defect labels, making it a multi-label classification problem.

## Missing Data
- Missing values were identified in 118 columns.
- The highest levels of missingness occur in Computer Vision (CV), Drying Process (DRY), and Simulation (SIM) features.
- Appropriate preprocessing, such as imputation or selective feature removal, will be required before model training.

## Defect Analysis
- 155 defective parts (LBL_NOK = 1), representing approximately 27.5% of all samples.
- Sink Marks are the most common defect, while Old Granulate is the rarest.
- The defect classes are imbalanced and may require class balancing techniques during model training.
- Around 11% of samples contain multiple defects, confirming this is a multi-label classification problem.

## Material Analysis
- PP: 360 samples
- ABS: 204 samples
- Material type appears to influence the occurrence of different defect types and should be considered an important feature during model development.

## Correlation Analysis
- Correlation analysis identified relationships among several numerical process variables.
- Highly correlated variables include plastification speed, melt pressure, temperature gradients, and part dimensions.
- These relationships may assist feature selection during defect classification.

## Time-Series Analysis
- 152 object-type columns contain time-series sensor data stored as arrays.
- These variables require feature extraction before they can be used in machine learning models.

## Recommendations for Modeling
1. Perform feature engineering on the time-series sensor data.
2. Handle missing values using appropriate preprocessing techniques.
3. Address class imbalance using methods such as class weights or oversampling.
4. Include material type as an important predictive feature.
5. Train and evaluate multi-label classification models such as Random Forest, XGBoost, and TCN for defect prediction.