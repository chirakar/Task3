# Final EDA Findings

## Dataset
- 564 samples
- 334 features

## Missing Data
- Many DRY, SIM, and SET features contain >60% missing values.
- Missing values are concentrated in specific experiment groups.

## Defect Analysis
- 155 defective parts (LBL_NOK = 1)
- Defect rate ≈ 27.5%

## Material Analysis
- PP: 360 samples
- ABS: 204 samples
- PP exhibits higher warpage and higher defect rates.

## Warpage Analysis
- Mean = 0.91
- Max = 7.10
- Distribution is right-skewed.
- Significant outliers are present.

## Experiment Analysis
- Lowest warpage: A08, A05, A07
- Highest warpage: A25, A28, A29

## Positive Correlations with Warpage
- E77_PlastificationSpeed
- E77_MeltPressure2Max
- ENV_AirHumidity
- IR temperature gradient features

## Negative Correlations with Warpage
- CV_Width1
- CV_Height1
- CV_Height2
- MET_MaterialMoisture
- SET_HoldingPressure2
- SCA_PartWeight

## Recommended Targets
- Classification: LBL_NOK
- Regression: CV_Warpage

## Recommendations for Modeling
1. Handle missing values in DRY and SIM features.
2. Remove or impute highly incomplete columns.
3. Investigate top correlated features first.
4. Address CV_Warpage outliers.
5. Compare classification and regression approaches.