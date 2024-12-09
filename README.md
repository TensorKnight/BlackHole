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

##### Data Preprocessing
Clean your data and handle null values:

```bash
import pandas as pd
from automate.DataPreprocessor import Null_Value_Remover
data = pd.read_csv('data.csv')
data_clean = Null_Value_Remover.remove_null_value(data, data['Timestamp_or_Categorical Column'])
```
