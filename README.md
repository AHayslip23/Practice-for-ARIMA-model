# Practice for ARIMA Model

Time-series forecasting practice with ARIMA models on daily Delhi climate data.

## Repository Contents

| File | Description |
|---|---|
| `Practice for ARIMA with climate data.ipynb` | ARIMA modeling notebook (40 charts) |
| `Delhi Climate Data 2013.csv` | Daily Delhi climate data (1,462 days): mean temperature, humidity, wind speed and mean pressure |

## Commit History

### `3bde79b`: Upload of the ARIMA notebook and dataset (2023-03-26)
- **Choosing model orders:**
  - plotted ACF and PACF charts to estimate the ARIMA orders (p = 2, d = 0, q = 3)
  - confirmed them with `pmdarima.auto_arima`, a stepwise search minimizing AIC
- **Train/test split:** the first 1,097 days for training and the remaining 365 days for testing.
- **Fitted `statsmodels` ARIMA models over four rounds:** `(2,0,3)`, `(2,0,1)`, `(1,1,1)` and `(1,0,3)`.
- **Evaluation:** RMSE on the test set for each round (about 16.8, 11.5, 5.4 and 360), with forecast vs. actual plots.

## Tools
Python, pandas, NumPy, statsmodels, pmdarima, scikit-learn, matplotlib, seaborn, Jupyter Notebook
