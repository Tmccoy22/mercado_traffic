# Mercado Traffic Challenge 11
This is a Jupyter Notebook that does time series and Facebook Prophet predictions. This was made on Google CoLab and looks at Google trending search and Mercado to help marketing efforts and stock predictoins. Using HvPlots we can get a better understanding for when to market and volitilty of the market.
---

## Technologies

This project leverages python 3.7 with the following packages:

* [pandas](https://github.com/pandas-dev/pandas) - For the command line interface, help page, and entrypoint.

* [hvplot](https://github.com/holoviz/hvplot) - A high-level plotting API for pandas, dask, xarray, and networkx built on HoloViews

* [metaplot](https://github.com/matplotlib/matplotlib) - For entrypoint and help page.

* [Prophet](https://github.com/facebook/prophet) - Tool for producing high quality forecasts for time series data that has multiple seasonality with linear or non-linear growth.

---

## Installation Guide

Before running the application first install the following dependencies. Note that if you are running on the cloud and not locally you will have to run all lines of code.
```
from IPython.display import clear_output
try:
  !pip install pystan
  !pip install prophet
  !pip install hvplot
  !pip install holoviews
except:
  print("Error installing libraries")
finally:
  clear_output()
  print('Libraries successfully installed')
``` 

```
import pandas as pd
import holoviews as hv
from prophet import Prophet
import hvplot.pandas
import datetime as dt
%matplotlib inline
```


---

## Usage

Acitvate a Google CoLab by navigating to https://colab.research.google.com/

---

## Examples
```
mercado_model =  Prophet()
mercado_model

mercado_model.fit(mercado_prophet_df)

# Create a future dataframe to hold predictions
# Make the prediction go out as far as 2000 hours (approx 80 days)
future_mercado_trends = mercado_model.make_future_dataframe(periods=2000, freq='H')

# View the last five rows of the future_mercado_trends DataFrame
future_mercado_trends.tail()
```

---

## Contributors

DU Starter Code
Terrence McCoy


---

## License

MIT
