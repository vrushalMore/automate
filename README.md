# Neptune-Automate
## Description
Simplify your machine learning code with this module

## Install
To install the module use:

```bash

pip install neptune-automate

```

## Application

### Clean your data and handle null values:

(1) Import

```bash

import pandas as pd
from automate.DataPreprocessor import Null_Value_Remover

```

(2) Use the function with your data:

```bash

data = pd.read_csv('data.csv')
data_clean = Null_Value_Remover.remove_null_value(data, data['Timestamp_or_Categorical Column'])

```

---

### Apply different machine learning models:

(1) Import

```bash

from automate.machine_learning import Machine_Learning_Models

```

(2) Use the function with your data:

```bash

from automate.machine_learning import Machine_Learning_Models

X = ...
y = ...

Machine_Learning_Models.apply_linear_regression(X, y)
Machine_Learning_Models.apply_random_forest_regression(X, y)
Machine_Learning_Models.apply_decision_tree_regression(X, y)
Machine_Learning_Models.apply_support_vector_regression(X, y)
Machine_Learning_Models.apply_GBR(X, y)
Machine_Learning_Models.apply_LGBM(X, y)
Machine_Learning_Models.apply_XGB(X, y)
Machine_Learning_Models.apply_multinomial_nb(X, y)
Machine_Learning_Models.apply_gaussian_nb(X, y)


```

---

### Use ARIMA, SARIMA, or SARIMAX for time series analysis:

(1) Import

```bash

from automate.statistical_models import Statistics_Models

```

(2) Use the function with your data:

```bash

Statistics_Models.apply_ARIMA(data_clean, p, d, q, 'Target_variable')
Statistics_Models.apply_SARIMA(data_clean, p, d, q, 'Target_variable')
Statistics_Models.apply_SARIMAX(data_clean, p, d, q, 'Target_variable', exog_vars=['variable_1', 'variable_2', 'variable_3'])

```

---

### Perform exponential smoothing for time series forecasting:

(1) Import

```bash

from automate.exponential_smoothening import Exponential_Smoothening

```

(2) Use the function with your data:

```bash

Exponential_Smoothening.simple_exponential_smoothening(data_clean['Target_variable '])
Exponential_Smoothening.holt_smoothening(data_clean['Target_variable'])
Exponential_Smoothening.exponential_smoothening(data_clean['Target_variable'])

```

---

### Augmented Dickey-Fuller Test:

(1) Import

```bash

from automate.augmented_dickey_fuller_test import Augmented_Dickey_Fuller_Test

```

(2) Use the function with your data:

```bash

Augmented_Dickey_Fuller_Test.check_stationarity(data_clean['Target_variable'])

```

---

### Convert your time series data to stationary:

(1) Import

```bash
from automate.augmented_dickey_fuller_test import Stationary_Converter
```

(2) Use the function with your data:

```bash

stationary_data = Stationary_Converter.convert_to_stationary(data_clean['Target_variable'])
Augmented_Dickey_Fuller_Test.check_stationarity(stationary_data)

```

### Evaluation Metrics

The function will allow you to print the evaluation metrics based on the problem dataset.

(1) Import

```bash
from automate.evaluation import metrics
```

(2) Use the function with your data:

```bash
# Example for regression task
metrics.display_metrics(y_test, y_pred)

# Example for classification task
metrics.display_metrics(y_true, y_pred)

```

## Note

This module currently might not work in some cases.

## Requirements

```bash

pandas
numpy
scikit-learn
statsmodels
xgboost
lightgbm
catboost
matplotlib
seaborn

```