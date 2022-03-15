# Module_4_Challenge
---
# Analyzing Portfolio Risk and Return

In Module 4 Challange assigment our task is to apply the three phases of financial analysis to determine if any arbitrage opportunities exist for Bitcoin. <br>Three phases are **Collect, Prepare, Analyze**. <br>We will sort through historical trade data for Bitcoin on two exchanges to find those opportunities: *Bitstamp* and *Coinbase*. 

---

## Technologies
Analyzing Portfolio Risk and Return project leverages python 3.7 with the following packages:

[Pandas](https://github.com/pandas-dev/pandas "Pandas") -
For the analysis/manipulation of two provided dataframes. 

We will use [Pandas](https://github.com/pandas-dev/pandas "Pandas") for handling [missing data](https://pandas.pydata.org/pandas-docs/stable/user_guide/missing_data.html), [removing duplicates](https://pandas.pydata.org/pandas-docs/stable/user_guide/duplicates.html), [slicing](https://pandas.pydata.org/pandas-docs/stable/user_guide/indexing.html#slicing-ranges), [chart visualization](https://pandas.pydata.org/pandas-docs/stable/user_guide/visualization.html), and much more.

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

**1.Analyzing Portfolio Risk and Return**
<br>



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



To prepare and clean the data we will use `isnull`,` dropna`, `duplicated`, `str.replace` functions.
```
bitstamp.isnull().sum()

bitstamp.dropna(inplace=True)

bitstamp.duplicated().sum()
```
**3.Analyze the Risk**
<br>



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



