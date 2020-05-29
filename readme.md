# SEC N-MFP2 Money Market Fund Holdings Data

- Author: Yangjue Han 
- Date: May 2020

## Introduction
This repository contains code that enables the user to parse and download money market fund holdings information in N-MFP2 filings from SEC EDGAR system. At the end of every month, all U.S. money market funds are required to report their securities holdings to SEC, including identification, maturity, market value, yield to maturity, issuer information, and other features. For repurchase agreement contracts, money market funds also have to report information on collateral securities. The granularity of this dataset provides an unparallel opportunity for financial economists to study questions related to the shadow banking system. 

## Installation

```
pip install -i https://test.pypi.org/simple/ secmmf==0.0.1
```

## Usage
```
import secmmf

# specify the directory used to store the data
# we recommand a local folder since the file could be several GB
data_dir = ## YOUR DIRECTORY HERE ##
pathfile = 'xmlpath.csv' # no need to change this

# download index files
secmmf.download_sec_index(data_dir, form_name = 'N-MFP2', start_date = '2016-10', end_date = '2020-05')
```


