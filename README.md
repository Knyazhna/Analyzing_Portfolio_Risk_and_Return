# Module_4_Challenge
---
# Analyzing Portfolio Risk and Return

In Module 4 Challange we are tasked with evaluating four new investment options for inclusion in the client portfolios. Legendary fund and hedge-fund managers run all four selections. We will need to determine the fund with the most investment potential based on key risk-management metrics: **The Daily Returns, Standard Deviations, Sharpe Ratios, and Betas.**

---

## Technologies
Analyzing Portfolio Risk and Return project leverages python 3.7 with the following packages:

[Pandas](https://github.com/pandas-dev/pandas "Pandas") -
For the analysis/manipulation/plotting the data for the four fund portfolios and [S&P 500](https://en.wikipedia.org/wiki/S%26P_500 "S&P 500"). 

[NumPy](https://github.com/numpy/numpy "NumPy") -
To calculate annualized standard deviation by using the square root.

---

## Installation Guide

First install the following libraries and dependencies.

```
# conda
conda install pandas
```

```
import pandas as pd
import numpy as np
from pathlib import Path
%matplotlib inline
```


---

## Usage

**1.Analyze the Performance**
<br>
Analyze the data to determine if any of the portfolios outperform the broader stock market, which the S&P 500 represents.


First we need to import two dataframes and we will do this by using `read_csv` function from pandas.
```
bitstamp = pd.read_csv(
    Path("./Resources/bitstamp.csv"),
    index_col="Timestamp",
    parse_dates=True,
    infer_datetime_format=True
    )
```
**2.Analyze the Volatility**
<br>
Analyze the volatility of each of the four fund portfolios and of the S&P 500 Index by using box plots.


To prepare and clean the data we will use `isnull`,` dropna`, `duplicated`, `str.replace` functions.
```
bitstamp.isnull().sum()

bitstamp.dropna(inplace=True)

bitstamp.duplicated().sum()
```
**3.Analyze the Risk**
<br>
Evaluate the risk profile of each portfolio by using the standard deviation and the beta.


Finally by using the Pandas `plot` function, we will create the visualization for the Bitstamp and Coinbase DataFrame. 

![Bitstamp and Coinbase: January 2018](January%202018.png)
![Bitstamp and Coinbase: March 2018](March%202018.png)

---

## Contributors

* Brought to you by Olga Koryachek.
* Email: olgakoryachek@live.com
* [LinkedIn](https://www.linkedin.com/in/olga-koryachek-a74b1877/?msgOverlay=true "LinkedIn")


---

## License

Licensed under the [MIT License](https://choosealicense.com/licenses/mit/)



