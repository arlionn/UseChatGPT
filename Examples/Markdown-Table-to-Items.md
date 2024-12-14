---
Title: Code Formatting for Stata codes
Author: Yujun Lian, ChatGPT 4o
Date: 2024/12/14 10:39
---

<br>

> 原始提问过程：[Click](https://chatgpt.com/share/675cee15-7f4c-8005-9e9b-412368ea279b)，`2024/12/14 10:37`

&emsp; 

## Prompt 1

```Markdown
将 Markdown 表格转换为 items 
> Source: https://www.tidy-finance.org/r/other-data-providers.html

帮我把如下表格整理成 items 的形式：
- FED
  - R packages: ...
  - Description

直接输出结果，不要显示提示信息

---

| Source                                   | Description                              | R packages                               |
| ---------------------------------------- | ---------------------------------------- | ---------------------------------------- |
|                                          | **Macroeconomic Variables**              |                                          |
| FED                                      | The Federal Reserve Bank of St. Louis provides more than 818,000 US and international time series from 109 sources via the API FRED. The data is freely available and can be browsed online on the [FRED homepage.](https://fred.stlouisfed.org/) | `fredr` ([Boysel and Vaughan 2021](https://www.tidy-finance.org/r/other-data-providers.html#ref-fredr)) and `alfred` ([Kleen 2021](https://www.tidy-finance.org/r/other-data-providers.html#ref-alfred)) |
| ECB                                      | The European Central Bank’s [Statistical Data Warehouse](https://sdw.ecb.europa.eu/) provides data on Euro area monetary policy, financial stability, and other topics relevant to the activities of the ECB and the European System of Central Banks (ESCB). | `ecb` ([Persson 2021](https://www.tidy-finance.org/r/other-data-providers.html#ref-ecb)) |
|                                          | **Financial data**                       |                                          |
| [Bloomberg](https://www.bloomberg.com/)  | Bloomberg’s Fundamental coverage includes current and normalized historical data for the balance sheet, income statement, cash flows statement, and financial ratios. Additionally, it provides industry-specific data for communications, consumer, energy, health care, and many more. In order to retrieve Bloomberg data, a paid subscription is needed. | `Rblpapi` ([Armstrong, Eddelbuettel, and Laing 2022](https://www.tidy-finance.org/r/other-data-providers.html#ref-Rblpapi)) |
| [Refinitiv Eikon](https://www.refinitiv.com/en/financial-data) | Eikon provides access to real-time market data, news, fundamental data, analytics, trading, and messaging tools. Refinitiv’s Eikon is a paid service. Apart from the CRAN version, there is also `https://github.com/philaris/eikonapir`. | `DatastreamDSWS2R` ([Cara 2021](https://www.tidy-finance.org/r/other-data-providers.html#ref-DatastreamDSWS2R)) and `eikonapir` |
| [Nasdaq Data Link (Quandl)](https://www.tidy-finance.org/r/data.nasdaq.com/publishers/qdl) | Quandl is a publisher of alternative data. Quandl publishes free data, scraped from many different sources from the web. However, some of the data requires specific subscriptions on the Quandl platform. | `Quandl` ([McTaggart, Daroczi, and Leung 2021](https://www.tidy-finance.org/r/other-data-providers.html#ref-Quandl)) |
| [Simfin](https://simfin.com/)            | Simfin make fundamental financial data freely available to private investors, researchers, and students. The data provider applies automating data collection processes to collect a large set of publicly available information from firms’ financial statements. | `simfinapi` ([Gomolka 2021](https://www.tidy-finance.org/r/other-data-providers.html#ref-simfinapi)) |
|                                          | **High-frequency data**                  |                                          |
| IEX                                      | The IEX Group operates the Investors Exchange (IEX), a stock exchange for US equities. IEX offers US reference and market data including end-of-day and *intraday pricing data*. IEX offers an API which is freely available. | `Riex` ([Ibrahim 2021](https://www.tidy-finance.org/r/other-data-providers.html#ref-Riex)) |
| TAQ                                      | TAQ data provides subscribed users access to all trades and quotes for all issues traded on NYSE, Nasdaq, and the regional exchanges. [TAQ data](https://www.nyse.com/market-data/historical) can be accessed from WRDS via Postgres. The `highfrequency` package delivers useful workflows to clean TAQ data. | `highfrequency` ([Boudt et al. 2022](https://www.tidy-finance.org/r/other-data-providers.html#ref-highfrequency)) |
|                                          | **Other (free) data**                    |                                          |
| [CoinMarketCap](https://coinmarketcap.com/) | The data provider CoinMarketCap provides cryptocurrency information and historical prices, as well as information on the exchanges they are listed on. | `crypto2` ([Stoeckl 2022](https://www.tidy-finance.org/r/other-data-providers.html#ref-crypto2)) |
| [CoinGecko](https://www.coingecko.com/)  | CoinGecko is an alternative crypto data provider of current and historical data on a myriad of coins and exchanges. | `geckor` ([Mastitsky 2021](https://www.tidy-finance.org/r/other-data-providers.html#ref-geckor)) |
| Twitter                                  | Twitter provides (limited) access for academic research to extract and analyze Tweets. | `rtweet` ([Kearney 2019](https://www.tidy-finance.org/r/other-data-providers.html#ref-rtweet)) |
| SEC company fillings                     | The [EDGAR](https://www.sec.gov/edgar/about) database provides free public access to corporate information, allowing you to research a public company’s financial information and operations by reviewing the filings the company makes with the SEC. You can also research information provided by mutual funds (including money market funds), exchange-traded funds (ETFs), and variable annuities. | `edgarWebR` ([Waldstein 2021](https://www.tidy-finance.org/r/other-data-providers.html#ref-edgarWebR)) |
| Google trends                            | Google offers public access to global search volumes through its search engine through the [Google Trends portal.](https://trends.google.com/trends/?geo=DK) | `globaltrends` ([Puhr and Müllner 2021](https://www.tidy-finance.org/r/other-data-providers.html#ref-globaltrends)) and `gtrends` ([Massicotte and Eddelbuettel 2022](https://www.tidy-finance.org/r/other-data-providers.html#ref-gtrendsR)) |
```


## Prompt 2

```Markdown
更新：把 items 中的引文链接换成可以直接访问的网址，这些网址可以从我提供的参考文献列表中获取：

例如：
[Kleen 2021](https://www.tidy-finance.org/r/other-data-providers.html#ref-alfred)
替换成：
[Kleen 2021](https://cran.r-project.org/package=alfred)

--- 参考文献：
## References

Armstrong, Whit, Dirk Eddelbuettel, and John Laing. 2022. *Rblpapi: R Interface to ’Bloomberg’*. [https://CRAN.R-project.org/package=Rblpapi](https://cran.r-project.org/package=Rblpapi).

Boudt, Kris, Jonathan Cornelissen, Scott Payseur, Onno Kleen, and Emil Sjoerup. 2022. *Highfrequency: Tools for Highfrequency Data Analysis*. [https://CRAN.R-project.org/package=highfrequency](https://cran.r-project.org/package=highfrequency).

Boysel, Sam, and Davis Vaughan. 2021. *fredr: An R client for the ’FRED’ API*. [https://CRAN.R-project.org/package=fredr](https://cran.r-project.org/package=fredr).

Cara, Charles. 2021. *DatastreamDSWS2R: Provides a Link Between the ’Refinitiv Datastream’ System and r*. [https://CRAN.R-project.org/package=DatastreamDSWS2R](https://cran.r-project.org/package=DatastreamDSWS2R).

Chen, Andrew Y., and Tom Zimmermann. 2022. “Open Source Cross-Sectional Asset Pricing.” *Critical Finance Review* 11 (2): 207–64. <http://dx.doi.org/10.1561/104.00000112>.

Gomolka, Matthias. 2021. *Simfinapi: Accessing ’SimFin’ Data*. [https://CRAN.R-project.org/package=simfinapi](https://cran.r-project.org/package=simfinapi).

Ibrahim, Myriam. 2021. *Riex: IEX Stocks and Market Data*. [https://CRAN.R-project.org/package=Riex](https://cran.r-project.org/package=Riex).

Kearney, Michael W. 2019. “Rtweet: Collecting and Analyzing Twitter Data.” *Journal of Open Source Software* 4 (42): 1829. <https://joss.theoj.org/papers/10.21105/joss.01829>.

Kleen, Onno. 2021. *Alfred: Downloading Time Series from ALFRED Database for Various Vintages*. [https://CRAN.R-project.org/package=alfred](https://cran.r-project.org/package=alfred).

Massicotte, Philippe, and Dirk Eddelbuettel. 2022. *gtrendsR: Perform and Isplay Google Trends Queries*. [https://CRAN.R-project.org/package=gtrendsR](https://cran.r-project.org/package=gtrendsR).

Mastitsky, Sergey. 2021. *Geckor: R Client for the ’CoinGecko’ API*. [https://CRAN.R-project.org/package=geckor](https://cran.r-project.org/package=geckor).

McTaggart, Raymond, Gergely Daroczi, and Clement Leung. 2021. *Quandl: API Wrapper for Quandl.com*. [https://CRAN.R-project.org/package=Quandl](https://cran.r-project.org/package=Quandl).

Persson, Eric. 2021. *Ecb: Programmatic Access to the European Central Bank’s Statistical Data Warehouse*. [https://CRAN.R-project.org/package=ecb](https://cran.r-project.org/package=ecb).

Puhr, Harald, and Jakob Müllner. 2021. “Let me Google that for you: Capturing globalization using Google Trends.” *Working Paper*. <https://www.ssrn.com/abstract=3969013>.

Stoeckl, Sebastian. 2022. *Crypto2: Download Crypto Currency Data from ’CoinMarketCap’ Without ’API’*. [https://CRAN.R-project.org/package=crypto2](https://cran.r-project.org/package=crypto2).

Waldstein, Micah J. 2021. *edgarWebR: SEC Filings Access*. [https://CRAN.R-project.org/package=edgarWebR](https://cran.r-project.org/package=edgarWebR).
```


<br>
<br>

## 原始结果 
| Source                                   | Description                              | R packages                               |
| ---------------------------------------- | ---------------------------------------- | ---------------------------------------- |
|                                          | **Macroeconomic Variables**              |                                          |
| FED                                      | The Federal Reserve Bank of St. Louis provides more than 818,000 US and international time series from 109 sources via the API FRED. The data is freely available and can be browsed online on the [FRED homepage.](https://fred.stlouisfed.org/) | `fredr` ([Boysel and Vaughan 2021](https://www.tidy-finance.org/r/other-data-providers.html#ref-fredr)) and `alfred` ([Kleen 2021](https://www.tidy-finance.org/r/other-data-providers.html#ref-alfred)) |
| ECB                                      | The European Central Bank’s [Statistical Data Warehouse](https://sdw.ecb.europa.eu/) provides data on Euro area monetary policy, financial stability, and other topics relevant to the activities of the ECB and the European System of Central Banks (ESCB). | `ecb` ([Persson 2021](https://www.tidy-finance.org/r/other-data-providers.html#ref-ecb)) |
|                                          | **Financial data**                       |                                          |
| [Bloomberg](https://www.bloomberg.com/)  | Bloomberg’s Fundamental coverage includes current and normalized historical data for the balance sheet, income statement, cash flows statement, and financial ratios. Additionally, it provides industry-specific data for communications, consumer, energy, health care, and many more. In order to retrieve Bloomberg data, a paid subscription is needed. | `Rblpapi` ([Armstrong, Eddelbuettel, and Laing 2022](https://www.tidy-finance.org/r/other-data-providers.html#ref-Rblpapi)) |
| [Refinitiv Eikon](https://www.refinitiv.com/en/financial-data) | Eikon provides access to real-time market data, news, fundamental data, analytics, trading, and messaging tools. Refinitiv’s Eikon is a paid service. Apart from the CRAN version, there is also `https://github.com/philaris/eikonapir`. | `DatastreamDSWS2R` ([Cara 2021](https://www.tidy-finance.org/r/other-data-providers.html#ref-DatastreamDSWS2R)) and `eikonapir` |
| [Nasdaq Data Link (Quandl)](https://www.tidy-finance.org/r/data.nasdaq.com/publishers/qdl) | Quandl is a publisher of alternative data. Quandl publishes free data, scraped from many different sources from the web. However, some of the data requires specific subscriptions on the Quandl platform. | `Quandl` ([McTaggart, Daroczi, and Leung 2021](https://www.tidy-finance.org/r/other-data-providers.html#ref-Quandl)) |
| [Simfin](https://simfin.com/)            | Simfin make fundamental financial data freely available to private investors, researchers, and students. The data provider applies automating data collection processes to collect a large set of publicly available information from firms’ financial statements. | `simfinapi` ([Gomolka 2021](https://www.tidy-finance.org/r/other-data-providers.html#ref-simfinapi)) |
|                                          | **High-frequency data**                  |                                          |
| IEX                                      | The IEX Group operates the Investors Exchange (IEX), a stock exchange for US equities. IEX offers US reference and market data including end-of-day and *intraday pricing data*. IEX offers an API which is freely available. | `Riex` ([Ibrahim 2021](https://www.tidy-finance.org/r/other-data-providers.html#ref-Riex)) |
| TAQ                                      | TAQ data provides subscribed users access to all trades and quotes for all issues traded on NYSE, Nasdaq, and the regional exchanges. [TAQ data](https://www.nyse.com/market-data/historical) can be accessed from WRDS via Postgres. The `highfrequency` package delivers useful workflows to clean TAQ data. | `highfrequency` ([Boudt et al. 2022](https://www.tidy-finance.org/r/other-data-providers.html#ref-highfrequency)) |
|                                          | **Other (free) data**                    |                                          |
| [CoinMarketCap](https://coinmarketcap.com/) | The data provider CoinMarketCap provides cryptocurrency information and historical prices, as well as information on the exchanges they are listed on. | `crypto2` ([Stoeckl 2022](https://www.tidy-finance.org/r/other-data-providers.html#ref-crypto2)) |
| [CoinGecko](https://www.coingecko.com/)  | CoinGecko is an alternative crypto data provider of current and historical data on a myriad of coins and exchanges. | `geckor` ([Mastitsky 2021](https://www.tidy-finance.org/r/other-data-providers.html#ref-geckor)) |
| Twitter                                  | Twitter provides (limited) access for academic research to extract and analyze Tweets. | `rtweet` ([Kearney 2019](https://www.tidy-finance.org/r/other-data-providers.html#ref-rtweet)) |
| SEC company fillings                     | The [EDGAR](https://www.sec.gov/edgar/about) database provides free public access to corporate information, allowing you to research a public company’s financial information and operations by reviewing the filings the company makes with the SEC. You can also research information provided by mutual funds (including money market funds), exchange-traded funds (ETFs), and variable annuities. | `edgarWebR` ([Waldstein 2021](https://www.tidy-finance.org/r/other-data-providers.html#ref-edgarWebR)) |
| Google trends                            | Google offers public access to global search volumes through its search engine through the [Google Trends portal.](https://trends.google.com/trends/?geo=DK) | `globaltrends` ([Puhr and Müllner 2021](https://www.tidy-finance.org/r/other-data-providers.html#ref-globaltrends)) and `gtrends` ([Massicotte and Eddelbuettel 2022](https://www.tidy-finance.org/r/other-data-providers.html#ref-gtrendsR)) |

## 转换后的结果

- FED  
  - R packages: `fredr` ([Boysel and Vaughan 2021](https://cran.r-project.org/package=fredr)) and `alfred` ([Kleen 2021](https://cran.r-project.org/package=alfred))  
  - Description: The Federal Reserve Bank of St. Louis provides more than 818,000 US and international time series from 109 sources via the API FRED. The data is freely available and can be browsed online on the [FRED homepage.](https://fred.stlouisfed.org/)  
- ECB  
  - R packages: `ecb` ([Persson 2021](https://cran.r-project.org/package=ecb))  
  - Description: The European Central Bank’s [Statistical Data Warehouse](https://sdw.ecb.europa.eu/) provides data on Euro area monetary policy, financial stability, and other topics relevant to the activities of the ECB and the European System of Central Banks (ESCB).  
- Bloomberg  
  - R packages: `Rblpapi` ([Armstrong, Eddelbuettel, and Laing 2022](https://cran.r-project.org/package=Rblpapi))  
  - Description: Bloomberg’s Fundamental coverage includes current and normalized historical data for the balance sheet, income statement, cash flows statement, and financial ratios. Additionally, it provides industry-specific data for communications, consumer, energy, health care, and many more. In order to retrieve Bloomberg data, a paid subscription is needed.  
- Refinitiv Eikon  
  - R packages: `DatastreamDSWS2R` ([Cara 2021](https://cran.r-project.org/package=DatastreamDSWS2R)) and `eikonapir`  
  - Description: Eikon provides access to real-time market data, news, fundamental data, analytics, trading, and messaging tools. Refinitiv’s Eikon is a paid service. Apart from the CRAN version, there is also `https://github.com/philaris/eikonapir`.  
- Nasdaq Data Link (Quandl)  
  - R packages: `Quandl` ([McTaggart, Daroczi, and Leung 2021](https://cran.r-project.org/package=Quandl))  
  - Description: Quandl is a publisher of alternative data. Quandl publishes free data, scraped from many different sources from the web. However, some of the data requires specific subscriptions on the Quandl platform.  
- Simfin  
  - R packages: `simfinapi` ([Gomolka 2021](https://cran.r-project.org/package=simfinapi))  
  - Description: Simfin makes fundamental financial data freely available to private investors, researchers, and students. The data provider applies automating data collection processes to collect a large set of publicly available information from firms’ financial statements.  
- IEX  
  - R packages: `Riex` ([Ibrahim 2021](https://cran.r-project.org/package=Riex))  
  - Description: The IEX Group operates the Investors Exchange (IEX), a stock exchange for US equities. IEX offers US reference and market data including end-of-day and *intraday pricing data*. IEX offers an API which is freely available.  
- TAQ  
  - R packages: `highfrequency` ([Boudt et al. 2022](https://cran.r-project.org/package=highfrequency))  
  - Description: TAQ data provides subscribed users access to all trades and quotes for all issues traded on NYSE, Nasdaq, and the regional exchanges. [TAQ data](https://www.nyse.com/market-data/historical) can be accessed from WRDS via Postgres.  
- CoinMarketCap  
  - R packages: `crypto2` ([Stoeckl 2022](https://cran.r-project.org/package=crypto2))  
  - Description: The data provider CoinMarketCap provides cryptocurrency information and historical prices, as well as information on the exchanges they are listed on.  
- CoinGecko  
  - R packages: `geckor` ([Mastitsky 2021](https://cran.r-project.org/package=geckor))  
  - Description: CoinGecko is an alternative crypto data provider of current and historical data on a myriad of coins and exchanges.  
- Twitter  
  - R packages: `rtweet` ([Kearney 2019](https://joss.theoj.org/papers/10.21105/joss.01829))  
  - Description: Twitter provides (limited) access for academic research to extract and analyze Tweets.  
- SEC company fillings  
  - R packages: `edgarWebR` ([Waldstein 2021](https://cran.r-project.org/package=edgarWebR))  
  - Description: The [EDGAR](https://www.sec.gov/edgar/about) database provides free public access to corporate information, allowing you to research a public company’s financial information and operations by reviewing the filings the company makes with the SEC.  
- Google trends  
  - R packages: `globaltrends` ([Puhr and Müllner 2021](https://www.ssrn.com/abstract=3969013)) and `gtrends` ([Massicotte and Eddelbuettel 2022](https://cran.r-project.org/package=gtrendsR))  
  - Description: Google offers public access to global search volumes through its search engine through the [Google Trends portal.](https://trends.google.com/trends/?geo=DK)
