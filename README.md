# Optuna Hyperparameter Optimization

A notebook that shows how to tune a model's hyperparameters with [Optuna](https://optuna.org).

## What the notebook does

1. Loads the Iris dataset from scikit-learn.
2. Defines an objective function that suggests `n_estimators` (integer from 2 to 40) and `max_depth` (log-uniform from 1 to 20) for a `RandomForestClassifier`, and returns the mean 5-fold cross-validation score.
3. Creates an Optuna study that maximises that score and runs 100 trials.
4. Prints the best accuracy and the best hyperparameters.
5. Plots the optimisation history and a slice plot with `optuna.visualization`.

## Run

```bash
pip install optuna scikit-learn plotly
```

Then open `Optuna - A_hyperparameter_optimization_framework.ipynb` and run the cells. It also runs in Google Colab.
