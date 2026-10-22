# White Wine Quality Prediction

## Project Overview

This project uses **Linear Regression** in **Orange Data Mining** to predict the quality score of white wine from its physicochemical properties. The workflow loads the wine-quality dataset, samples the data, trains a regression model, evaluates it, and generates predictions for the remaining records.

## Dataset

The workflow is configured for the `winequality-white.csv` dataset.

According to the supplied Orange prediction output:
- **Instances:** 1,459
- **Variables:** 12
- **Input features:** 11 numeric features
- **Target:** `quality` (numeric)
- **Missing values:** None reported in the displayed input summary

The features include measurements such as fixed acidity, volatile acidity, citric acid, residual sugar, chlorides, free sulfur dioxide, total sulfur dioxide, density, pH, sulphates, and alcohol. The target is the wine's quality score.

> Note: The supplied workflow references a local Windows path for the CSV. You may need to select the dataset again when opening the project on another computer.

## Tools and Technology

- **Orange Data Mining** — visual, widget-based machine-learning workflow
- **Linear Regression** — prediction model
- **Wine Quality (White) dataset** — regression dataset

## Workflow

The Orange workflow (`untitled.ows`) contains these widgets:

1. **File** — loads the wine-quality CSV file.
2. **Data Sampler** — selects a 70% sample of the data; the remaining data is sent separately for prediction.
3. **Linear Regression** — trains a linear regression model using the sampled data.
4. **Test and Score** — evaluates the learner using the sampled data input configured in the workflow. Check the widget's evaluation settings before reporting final metrics.
5. **Predictions** — applies the trained model to the remaining data and displays predicted quality values.

## How to Run

1. Install and open [Orange Data Mining](https://orangedatamining.com/).
2. Open `untitled.ows` in Orange.
3. In the **File** widget, select your local copy of `winequality-white.csv` if the data source is missing.
4. Confirm the target variable is `quality` and is treated as numeric.
5. Run the workflow and inspect the **Test and Score** and **Predictions** widgets.
6. Record evaluation metrics from Orange before drawing conclusions about model performance.

## Expected Output

The **Predictions** widget displays the predicted wine-quality score alongside available dataset columns. The supplied screenshot shows predictions and example values, but it does not provide enough evaluation results to claim a particular accuracy or error score.

## Project Objective

The objective is to explore how wine's physicochemical measurements relate to its quality score and to demonstrate a basic end-to-end regression workflow in Orange.

## Limitations

- Linear Regression models linear relationships and may not capture all complex relationships in wine-quality data.
- Predictions are estimates, not guaranteed expert or sensory assessments of wine quality.
- Results depend on the dataset, sampling, and evaluation configuration.
- The dataset path may need to be updated on another machine.

## Files

- `untitled.ows` — Orange Data Mining workflow
- `res.pdf` — screenshot/export showing the prediction output

## Possible Improvements

- Compare Linear Regression with Random Forest, Gradient Boosting, and other regression models.
- Use a clearly defined train/test split or cross-validation and report MAE, RMSE, and R².
- Visualize actual versus predicted quality scores and examine residuals.
- Document the dataset source and its license in the project repository.

---
Created from the supplied Orange workflow and prediction screenshot.
