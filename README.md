## Neptune-Automate
### Description
Simplify your machine learning code with this module

---

### Install
To install the module use:

```bash
pip install neptune-automate
```

### Usage

Clean your data and handle null values:

```bash

import pandas as pd
from automate.DataPreprocessor import Null_Value_Remover
data = pd.read_csv('data.csv')
data_clean = Null_Value_Remover.remove_null_value(data, data['Timestamp_or_Categorical Column'])

```

Apply different machine learning models:

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

```

Use ARIMA, SARIMA, or SARIMAX for time series analysis:

```bash

from automate.statistical_models import Statistics_Models

Statistics_Models.apply_ARIMA(data_clean, 1, 1, 0, 'Target_variable ')
Statistics_Models.apply_SARIMA(data_clean, 1, 1, 0, 'Target_variable ')
Statistics_Models.apply_SARIMAX(data_clean, 1, 1, 0, 'Target_variable ', exog_vars=['variable_1', 'variable_2', 'variable_3'])

```

Perform exponential smoothing for time series forecasting:

```bash

from automate.exponential_smoothening import Exponential_Smoothening

Exponential_Smoothening.simple_exponential_smoothening(data_clean['Target_variable '])
Exponential_Smoothening.holt_smoothening(data_clean['Target_variable'])
Exponential_Smoothening.exponential_smoothening(data_clean['Target_variable'])

```

Augmented Dickey-Fuller Test:

```bash

from automate.augmented_dickey_fuller_test import Augmented_Dickey_Fuller_Test

Augmented_Dickey_Fuller_Test.check_stationarity(data_clean['Target_variable'])

```

Convert your time series data to stationary:

```bash

from automate.augmented_dickey_fuller_test import Stationary_Converter

stationary_data = Stationary_Converter.convert_to_stationary(data_clean['Target_variable '])
Augmented_Dickey_Fuller_Test.check_stationarity(stationary_data)

```

### Note

This module currently only works for Non-Categorical Time Series Data

### Requirements.txt

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
twine
wheel
setuptools

```