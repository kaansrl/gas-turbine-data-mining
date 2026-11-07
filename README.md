# Gas Turbine Data Mining

This project analyzes gas turbine operating data using **Orange Data Mining**, focusing on carbon monoxide (CO) concentration prediction through regression analysis and dimensionality reduction using Principal Component Analysis (PCA).

## Dataset

♦ **Source:** [UCI Gas Turbine CO and NOx Emission Data Set](https://archive.ics.uci.edu/dataset/551/gas+turbine+co+and+nox+emission+data+set)  
♦ **Years:** 2014–2015  
♦ **Observations:** 14,542  
♦ **Original attributes:** 11  

### Dataset Attributes

| Attribute | Description | Unit |
|---|---|---|
| AT | Ambient Temperature | °C |
| AP | Ambient Pressure | mbar |
| AH | Ambient Humidity | % |
| AFDP | Air Filter Difference Pressure | mbar |
| GTEP | Gas Turbine Exhaust Pressure | mbar |
| TIT | Turbine Inlet Temperature | °C |
| TAT | Turbine After Temperature | °C |
| TEY | Turbine Energy Yield | MWh |
| CDP | Compressor Discharge Pressure | mbar |
| CO | Carbon Monoxide Concentration | mg/m³ |
| NOX | Nitrogen Oxides Concentration | mg/m³ |

Nine operating parameters were used as input features, while CO concentration was selected as the regression target. NOX was excluded from the predictive features.

## Methods

♦ **Regression:** Linear Regression and Random Forest (100 trees)  
♦ **Evaluation:** 5-fold cross-validation and year-based cross-validation  
♦ **Metrics:** MSE, RMSE, MAE, and R²  
♦ **PCA:** Standardization and dimensionality reduction using nine operating features  
♦ **Visualization:** Actual vs. predicted CO values and PC1–PC2 scatter plots  

## Results

### Regression Analysis

**5-Fold Cross-Validation**

| Metric | Linear Regression | Random Forest |
|---|---:|---:|
| MSE | 1.904 | 1.017 |
| RMSE | 1.380 | 1.008 |
| MAE | 0.800 | 0.429 |
| R² | 0.603 | 0.788 |

Random Forest achieved better predictive performance than Linear Regression, with a higher R² value and lower prediction errors.

**Year-Based Cross-Validation**

| Metric | Linear Regression | Random Forest |
|---|---:|---:|
| MSE | 3.092 | 2.917 |
| RMSE | 1.758 | 1.708 |
| MAE | 1.194 | 1.098 |
| R² | 0.355 | 0.391 |

Both models showed reduced performance in year-based validation compared with 5-fold cross-validation. This suggests that predicting CO concentrations across different years is more challenging.

### Principal Component Analysis (PCA)

PCA was applied after standardizing the nine operating features.

♦ **PC1:** 55.93% explained variance  
♦ **PC2:** 19.83% explained variance  
♦ **First two components:** 75.77% cumulative explained variance  
♦ **First four components:** 93.14% cumulative explained variance  

The PC1–PC2 scatter plot showed substantial overlap between observations from 2014 and 2015, without a clear separation between the two years.

## Tools

Orange Data Mining

## Project Files

The repository contains:

- 2014 and 2015 CSV datasets
- Orange workflow (.ows)
- Workflow screenshot

## Video Presentation

[Watch the project presentation on YouTube](https://www.youtube.com/watch?v=OZvX49sjtmY)

## References

UCI Machine Learning Repository: [Gas Turbine CO and NOx Emission Data Set](https://archive.ics.uci.edu/dataset/551/gas+turbine+co+and+nox+emission+data+set)

Orange Data Mining: https://orangedatamining.com/
