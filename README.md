# Gas Turbine Data Mining

This project analyzes gas turbine data using **Orange Data Mining**, focusing on CO emission prediction and dimensionality reduction.

## Dataset
♦ **Source:** [UCI Gas Turbine CO and NOx Emission Data Set](https://archive.ics.uci.edu/dataset/551/gas+turbine+co+and+nox+emission+data+set)
♦ **Years:** 2014–2015
♦ **Observations:** 14,542

## Methods
♦ **Regression:** Linear Regression and Random Forest
♦ **Evaluation:** 5-fold cross-validation and year-based validation
♦ **PCA:** Dimensionality reduction and visualization using PC1 and PC2

## Results

### Regression Analysis

**5-Fold Cross-Validation**

| Metric | Linear Regression | Random Forest |
|---|---:|---:|
| R² | 0.603 | 0.788 |
| RMSE | 1.380 | 1.008 |
| MAE | 0.800 | 0.429 |

Random Forest outperformed Linear Regression, achieving higher R² and lower prediction errors.

**Year-Based Cross-Validation**

| Metric | Linear Regression | Random Forest |
|---|---:|---:|
| R² | 0.355 | 0.391 |
| RMSE | 1.758 | 1.708 |
| MAE | 1.194 | 1.098 |

Both models showed reduced performance when evaluated across different years, indicating challenges in generalizing to unseen yearly data.

### Principal Component Analysis (PCA)

♦ **PC1:** 55.93% explained variance
♦ **PC2:** 19.83% explained variance
♦ **First two components:** 75.77% cumulative explained variance
♦ **First four components:** 93.14% cumulative explained variance

The PC1–PC2 scatter plot showed substantial overlap between observations from 2014 and 2015.

## Tools
Orange Data Mining

## Project Files
CSV datasets, Orange workflow (.ows), and workflow screenshot.
