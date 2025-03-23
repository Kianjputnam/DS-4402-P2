# DS4002 Project 2

#### Kian Putnam, Tenzin Nargee, Visal Kamalakrishnan 

## Goal

Our project seeks to understand the relationship between economic indicators and housing prices in Virginia counties. By leveraging time series forecasting through the SARIMA[^fn1] model and performing correlation analysis, we aim to identify the key factors driving housing price changes and predict future trends. This will provide valuable insights for policymakers and potential homebuyers.

This dataset was obtained from the Redfin Data Center, which provides comprehensive housing prices and sales data across various regions[^fn2]. It includes key variables such as state codes, zip codes, property types, median sale prices, median list prices, and other metrics like homes sold, inventory, and days on the market.

## Software / Platform

We are using Jupter Notebooks for this program that run on Python 3 (prefferably 3.10+). Our code can be run on **Google Colab** by importing our notebooks. The following files require access to a GPU (or else will be very slow):

1. sarima_model.ipynb

For this file, a **Windows** or **Linux** environment is needed with `statsmodels`, `scikitlearn`, packages and access to a Nvidia GPU and respective drivers. Additonal packages will be included in the files themselves as a runtime dependency. These files can alternatively be run on **Google Colab** or **Rivanna**. 

All additional files will need a Python environment with the packages `Pandas`, `Numpy`, `Matplotlib`, and with support for `Jupyter Notebooks` and can be run on **Windows**, **Linux**, or **Mac**

## Documentation

The files and folders are broken down into this structure

```
- root
  -- data
    -- va_filtered_listings_albemarle.csv
    -- va_filtered_listings.csv
  -- scripts
    -- script files for data analysis
  -- otuput
    -- charts
  -- README.md
  -- LICENSE
```

The `data` folder contains the datasets which we used in our project. This is filtered data based on the original dataset from Redfin[^fn2] which is far too large to be uploaded on Github. The `scripts` folder contains multiple `Jupyter Notebooks` that have been used to analyse the data, graph market trends, run SARIMA, and do error analysis. The `output` folder contains generated graphs from SARIMA and graphs of the market trends.


## Steps To Reproduce

To reproduce the results of the project first clone the repository the following command in your terminal 
```
git clone https://github.com/Kianjputnam/DS-4402-P2.git
```

You can run the individual files locally (provided you follow the specifications listed in - [Software / Platform](##Software%20/%20Platform)) or can run them in **Rivanna** or **Google Colab**. All data files are provided, except for the Redfin data set, and all outputs will overwrite the output images or files will overwrite previously existing output files.

* How to download the Redfin Data set: Go to the Redfin database[^fn2] and navigate to the `Redfin Monthly Housing Market Data` section. Click on the `download` tab in the chart and choose a format to download (prefferably excel). This should give a zip archive which can be filtered using `real_estate_initial_notebook.ipynb`

The scripts can be run in the order shown by their filenames. While this is not a strict requirements, note that some files need to be run before others in the order shown below

1. compress_va_listings_code.ipynb, real_estate_initial_notebook.ipynb, zipcode_listings.ipynb
2. va_listing_visualizations_p1.ipynb, va_listing_visualizations_p2.ipynb
3. sarima_model.ipynb

## References

[^fn1]:S. Do, "Time Series Forecasting: ARIMA and SARIMA," Latinx in AI - Medium, Dec. 11, 2023. [Online]. Available: https://medium.com/latinxinai/time-series-forecasting-arima-and-sarima-450fb18a9941. [Accessed: Feb. 24, 2025].

[^fn2]: Redfin, "Redfin Data Center," Redfin News, 2025. [Online]. Available: https://www.redfin.com/news/data-center/. [Accessed: Feb. 24, 2025].


