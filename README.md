# GroupProject
Our project analyze different kinds of portfolios based on 12 stocks in China.

## Data
We get stock data from Tushare, which is a free open source python financial data interface package.
#### install Tushare

```bash
pip install tushare
```
or
```bash
pip install tushare -upgrade
```
or search on: https://pypi.org/project/tushare/
#### make sure already installed Tushare
```bash
import tushare
print(tushare._version_)
```
#### Usage
```bash
import tushare as ts
TOKEN=#you can create your own account at the following site: https://tushare.pro/register?reg=243276, then find your token id
ts.set_token(TOKEN)
api=ts.pro_api()
data=(api.daily(ts_code=,#stock id,for example:"000538.SZ"
start_date="20110101",end_date="20201231",fields=["ts_code","trade_date","close"]))#"close" means closing proce of one stock

```
Also, we use CSI 300 index download from quotes.money.163.com/trade/lsjysj_zhishu_399300
#### 399300.csv
This csv file contains the closing price('close') and dates ('trade_date') of CSI 300 from 2011 to 2020. We will input this data in our project code:
```bash
hs=pd.read_csv("399300.csv")#also, can be changed to the direction of file now
```

#### 399300.csv
This csv file contains the closing price('close') and dates ('trade_date') of CSI 300 from 2011 to 2021.
```bash
hs2=pd.read_csv("399300(1).csv")#also, can be changed to the direction of file now
```
## Execution instruction
To implement our project, please download the '.ipynb' file, '399300.csv' and '399300(1).csv' file. Then, please start jupyter notebook server.
```bash
jupyter notebook
```
From the notebook list page, navigate to our code directory and open a notebook. Execute the code in a notebook cell by clicking on it and hitting Shift+Enter. Now, you can get the result!


