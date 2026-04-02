# Medical Insurance Cost Prediction

## Project Overview
This project uses **Linear Regression** to predict medical insurance charges based on patient demographics and health indicators. The model analyzes factors such as age, BMI, smoking status, and region to estimate insurance costs.

## Dataset
The dataset (`insurance.csv`) contains **1,338 records** with the following features:

| Feature | Description | Data Type |
|---------|-------------|-----------|
| age | Age of beneficiary | int64 |
| sex | Gender (female/male) | object |
| bmi | Body Mass Index (kg/m²) | float64 |
| children | Number of children/dependents covered | int64 |
| smoker | Smoking status (yes/no) | object |
| region | Residential area in US (northeast, northwest, southeast, southwest) | object |
| charges | Individual medical costs billed by health insurance (target variable) | float64 |

## Tech Stack
- **Python 3.x**
- **Pandas** - Data manipulation
- **Seaborn/Matplotlib** - Data visualization
- **Scikit-learn** - Machine learning

## Model Performance

### Model 1: Basic Linear Regression
- **Features used**: age, sex, bmi, children, smoker
- **R-squared**: 0.7811
- **Adjusted R-squared**: 0.7770

### Model 2: Linear Regression with One-Hot Encoding
- **Features used**: age, sex, bmi, children, smoker, region (one-hot encoded)
- **R-squared**: 0.7811

## Key Findings
- **Smoking status** is the strongest predictor of insurance charges
- **Age** and **BMI** also show significant correlation with charges
- **Region** has minimal impact on prediction accuracy
- The model explains approximately **78%** of the variance in insurance costs

## Visualizations
The scatter plot of BMI vs Charges, colored by smoking status, reveals:
- Smokers have significantly higher insurance charges
- Non-smokers show relatively stable charges across BMI ranges
- Positive correlation between BMI and charges for smokers

## Installation & Usage

### Prerequisites
```bash
pip install pandas seaborn scikit-learn matplotlib
