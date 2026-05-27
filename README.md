# Video Game Sales Analysis and Machine Learning Project

This repository contains a cumulative data science project focused on analyzing video game sales and building machine learning models to predict global sales using game-related features such as platform, genre, publisher, release year, and regional sales.

## Project overview

The project was completed across multiple course milestones, moving from data cleaning and exploration to hypothesis testing, machine learning, model comparison, and final evaluation. The main hypothesis examined in the project is whether **game genre and platform have a significant impact on global video game sales**.

### Hypotheses

- **Null hypothesis (H0):** There is no significant impact of game genre and platform on global sales.
- **Alternative hypothesis (H1):** Game genre and platform play a major role in global sales.

The final modeling results support the alternative hypothesis, with the best-performing models showing that genre, platform, and related features are highly informative for predicting global sales.

## Dataset

The project uses a cleaned video game sales dataset stored in spreadsheet format. The data includes game titles, platform, genre, publisher, release information, and regional/global sales fields that were further transformed for analysis and machine learning.

## Project structure

This repository may contain files such as:

- `README.md` — project description and setup instructions.
- `*.ipynb` — Jupyter/Colab notebooks used for analysis and modeling.
- `*.pdf` — exported project reports or milestone submissions.
- `vgsales_cleaned.xlsx` — cleaned dataset used in the project.
- Image files used for documentation or visual outputs.

## Methods used

The project includes the following major steps:

- Data cleaning and preparation.
- Exploratory data analysis and visualization.
- Feature engineering.
- Correlation-based feature filtering and PCA-based dimensionality reduction trials.
- Supervised machine learning for regression.
- Model evaluation using multiple regression metrics.
- Comparison of baseline, regularized, ensemble, and boosted models.

### Machine learning models tried

The following models were trained and compared:

- Linear Regression.
- Ridge Regression.
- Lasso Regression.
- Random Forest Regressor.
- Gradient Boosting Regressor.
- Support Vector Regression (SVR).

## Evaluation metrics

Because this is a regression problem, model performance was evaluated using:

- **R² score** — to measure goodness of fit.
- **RMSE** — to measure average prediction error magnitude.
- **MAE** — to measure average absolute error.

## Final model results

The final compared models produced the following test-set results:

| Model | R² | RMSE | MAE |
|---|---:|---:|---:|
| Linear Regression | 0.950 | 0.091 | 0.052 |
| Ridge Regression | 0.950 | 0.091 | 0.052 |
| Lasso Regression | 0.950 | 0.091 | 0.052 |
| Random Forest Regressor | 0.995 | 0.030 | 0.009 |
| Gradient Boosting Regressor | 0.997 | 0.023 | 0.011 |
| SVR (RBF kernel) | 0.861 | 0.152 | 0.080 |

Based on these results, **Gradient Boosting Regressor** achieved the strongest overall test performance, with Random Forest also performing extremely well. The linear and regularized linear models provided strong baselines, while SVR underperformed relative to the tree-based ensemble methods.

## Key findings

- Genre and platform contribute meaningfully to predicting global sales, supporting the alternative hypothesis explored in the project.
- Linear, Ridge, and Lasso Regression performed similarly, suggesting regularization did not materially improve performance for this feature set.
- Random Forest and Gradient Boosting captured nonlinear structure much better than linear models.
- Tree-based ensemble methods were the best fit for this dataset.

## Visualizations included

Depending on the notebook version, the project may include:

- Exploratory charts for distributions and feature relationships.
- Correlation heatmaps.
- PCA explained variance plots.
- Actual vs predicted plots for regression models.
- Residual plots.
- Feature importance plots for ensemble models.

## Environment and file path note

This project was originally developed in **Google Colab** and later adapted to a local computer / GitHub folder structure. Most file paths were updated during cleanup, but users should still review notebook file paths carefully before running the project, since local directory structures may differ.

To avoid file path issues:

- Keep the dataset in the expected project folder, or
- Update the notebook paths to match your own system.

If a notebook cell fails because a file cannot be found, the first thing to check is the input or output path used in that cell.

## How to run

1. Clone or download this repository.
2. Make sure the dataset file is available in the expected project directory.
3. Open the notebook in Jupyter Notebook, JupyterLab, VS Code, or Google Colab.
4. Install required Python libraries if they are not already available.
5. Run the notebook cells in order from top to bottom.
6. If a file-loading error occurs, update the relevant file path to match your local environment.

## Suggested dependencies

This project uses common Python data science libraries, including:

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn`

A typical install command is:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn openpyxl
```

## Learning outcomes

This project demonstrates:

- End-to-end data science workflow.
- Hypothesis-driven analysis.
- Data cleaning and feature engineering.
- Regression model development and comparison.
- Evaluation of model fit, including overfitting and underfitting considerations.
- Communication of findings through metrics, visualizations, and written interpretation.

## Acknowledgment

This project was developed as part of a multi-stage academic data science assignment sequence and refined into a cumulative final project!!!
