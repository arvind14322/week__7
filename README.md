# Week 7 — Kelmarsh Wind Forecasting

This repository contains the Week 7 work for **College Project Team 25**, focusing on forecasting wind-related data using the Kelmarsh wind dataset.

## Project Overview

The project explores wind data from the Kelmarsh wind farm and builds a forecasting workflow using Python and Jupyter Notebook. The main notebook, `kelmarsh_wind_forecasting.ipynb`, contains data exploration, preprocessing, model training, evaluation, and reporting.

## Repository Contents

| File | Description |
|---|---|
| `kelmarsh_wind_forecasting.ipynb` | Main Jupyter Notebook containing the wind forecasting analysis and model workflow |
| `Combined_Project_Plans.txt` | Combined project planning document for the team |
| `.gitignore` | Files and folders excluded from version control |
| `README.md` | Project documentation |

## Requirements

To run the notebook, install Python and the required libraries:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

You can also create and activate a virtual environment first:

```bash
python -m venv venv
source venv/bin/activate  # macOS/Linux
venv\Scripts\activate     # Windows
```

## How to Run

1. Clone the repository:

```bash
git clone [https://github.com/arvind14322/week__7.git](https://github.com/arvind14322/week__7.git)
cd week__7
```

2. Install the required packages:

```bash
pip install -r requirements.txt
```

> If `requirements.txt` is not included, install the libraries listed in the Requirements section.

3. Start Jupyter Notebook:

```bash
jupyter notebook
```

4. Open `kelmarsh_wind_forecasting.ipynb` and run the cells from top to bottom.

## Workflow

The notebook follows these main stages:

1. Load and inspect the Kelmarsh wind dataset  
2. Clean and preprocess the data  
3. Perform exploratory data analysis  
4. Create features for forecasting  
5. Train and evaluate forecasting models  
6. Compare model performance  
7. Visualise and interpret the results  

## Models Used

Two forecasting models were developed and compared:

- **Baseline MLP**: A Multilayer Perceptron neural network used as the baseline forecasting model.
- **Random Forest**: A tree-based ensemble model used to compare performance against the baseline.

Both models were evaluated on the test set using MAE, RMSE, normalised MAE, accuracy, and R².

## Model Comparison

### Test Set Results

| Model | MAE (Z) | RMSE (Z) | MAE (kW) | RMSE (kW) | Norm MAE (%) | Accuracy Cap (%) | Accuracy Act (%) | R² |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Baseline MLP | 0.0436 | 0.0579 | 119.98 | 160.25 | 0.98 | 99.02 | 90.03 | 0.9985 |
| Random Forest | 0.0421 | 0.0724 | 134.38 | 231.19 | 1.09 | 98.91 | 96.13 | 0.9969 |

### Best Model

The **Baseline MLP** is the best overall model because it achieved:

- The lowest RMSE for both normalised and kW predictions  
- The lowest MAE in kW  
- The lowest normalised MAE  
- The highest R² score  
- The highest accuracy against capacity  

The **Random Forest** model achieved a slightly lower MAE in the normalised scale and higher actual accuracy, but its higher RMSE and lower R² indicate that the Baseline MLP provides more consistent overall forecasting performance.

## Report Summary

The results show that both models perform strongly on the Kelmarsh wind forecasting task. However, the **Baseline MLP** is recommended as the preferred model because it produces lower overall prediction errors and explains more variance in the target variable.

Future improvements could include hyperparameter tuning, additional weather features, time-series feature engineering, and testing more advanced forecasting models.

## Team

**College Project Team 25**

## Notes

This repository is for academic project work. Update this README as the project develops with more detail on the dataset, model configuration, results, and conclusions.
