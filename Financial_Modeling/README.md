# Financial Modeling: Forecasting Securities

This project showcases an attempt to forecast securities using technical indicators (historical stock data) and, in a sense, the potential to earn capital using filings types from the United States Securities & Exchange Commission (SEC).

------

## Table of Contents

- [Problem Statement](#Problem-Statement)
- [Assumptions](#Assumptions)
- [Introduction](#Introduction)
- [Built with](#Built-with)
- [Directory Structure](#Directory-Structure)
- [Exploratory Data Analysis](#Exploratory-Data-Analysis)
- [Feature Engineering](#Feature-Engineering)
- [Preprocessing Data](#Preprocessing-Data)
- [Optimal Model](#Optimal-Model)
- [Conclusion](#Conclusion)
- [Credits](#Credits)

-----
<a class="anchor" id="Problem-Statement"></a>
## Problem Statement 



The problem at hand is to evaluate and predict securities using statistical analyses of market activity (e.g. price & volume) and SEC filings.

-----
<a class="anchor" id="Assumptions"></a>
## Assumptions


The initial assumption is that the market moves in trends, therefore engineering short, medium, and long term patterns/trends (moving averages) will be a good indicator and trading strategy.

-------
<a class="anchor" id="Introduction"></a>
## Introduction

This project is broken down into two main sub-directories. Beginning with, [Stocks](https://github.com/adam-delreal/Capstone/tree/master/stocks), which is the indicative dataset containing the historical price of a security. The second, is the [SEC](https://github.com/adam-delreal/Capstone/tree/master/sec), directory, where the data concerning with SEC filings is scraped and analyzed. Below, is a more extensive introduction and overview of the project and it's to sub-directories.

#### Stock Data:
 The indicative, or stock, data is sourced from [Quandle](https://www.quandl.com/)'s API and is a data set of historical stock data since the company's Initial Price Offering, which is the very first sale of stock issued by a company to the public.

Subsequently,  [Exploratory Data Analysis](https://github.com/adam-delreal/Capstone/blob/master/stocks/Apple_EDA.ipynb) (EDA) is performed. During this stage the data is analyzed, visualized, and feature engineering. Feature engineering is the process of transforming the raw data into to effectively represent the underlying problem in predictive modeling. In the attempt to engineer the data, *moving averages*, *percent changes*, and *difference* in values are calculated--if these concepts are foreign to you, please do not worry as these concepts will be discussed in further detail  later. 

Upon analyzing and engineering the features, the data is [preprocessed](https://github.com/adam-delreal/Capstone/blob/master/stocks/Apple_Model_1_Data_Prep.ipynb) and prepared for predictive modeling.  Since the stock data is sequential and dealing with time, the training and testing set were done manually. 

Thereafter, the data is trained using machine learning models such as: [Linear](https://github.com/adam-delreal/Capstone/blob/master/stocks/Apple_Model_2_Linear_Regression.ipynb) Regression, [Random Forest](https://github.com/adam-delreal/Capstone/blob/master/stocks/Apple_Model_3_Random_Forest.ipynb) Regression, [Bagging Regression](https://github.com/adam-delreal/Capstone/blob/master/stocks/Apple_Model_4_Bagging_Regressor.ipynb) on a Random Forest, and Regression using Facebook's [Prophet](https://github.com/adam-delreal/Capstone/blob/master/stocks/Apple_Model_5_Prophet.ipynb). 

#### SEC Data:

The [SEC](https://github.com/adam-delreal/Capstone/tree/master/sec) data is sourced from the [SEC website](https://www.sec.gov/), where the data was scraped using the *BeautifulSoup* library. Upon obtaining the documentation types, some brief [Exploratory Data Analysis](https://github.com/adam-delreal/Capstone/blob/master/sec/Apple_SEC_EDA.ipynb). During this brief analysis, some of document types where grouped accordingly and visualized to understand the frequency of filing. 

 Moreover, the SEC data was [merged](https://github.com/adam-delreal/Capstone/blob/master/stocks/Apple_EDA_wSEC.ipynb) with the stock data to further analyze, visualize, and feature engineer the data. The objective was to find whether an type of SEC filing was correlated to the price of the security.

Following the EDA, the data was [prepared](https://github.com/adam-delreal/Capstone/blob/master/stocks/Apple_Model_Classification_1_Prep.ipynb), turning files into binary values and manually splitting the train and test sets. Subsequently, the data was ready to be modeled using a [Random Forest](https://github.com/adam-delreal/Capstone/blob/master/stocks/Apple_Model_Classification_3_Random_Forest.ipynb) Classification Model.

----------
<a class="anchor" id="Built-With"></a>
## Built with


#### This project was built with the following tools:
- [Python](https://www.python.org/)
- [Jupyter Notebook/Lab](http://jupyter.org/index.html)
- [Seaborn](https://seaborn.pydata.org/introduction.html)
- [Matplotlib](https://matplotlib.org/)
- [Numpy](http://www.numpy.org/)
- [Pandas](https://pandas.pydata.org/)
- [BeautifulSoup](https://www.crummy.com/software/BeautifulSoup/bs4/doc/)
- [Quandle](https://www.quandl.com/): An API for financial, economic, and alternative datasets for investment professionals.
- [Scikit Learn](http://scikit-learn.org/stable/index.html#)
- [Facebook Prophet](https://research.fb.com/prophet-forecasting-at-scale/)
- [BeakerX](http://beakerx.com/)


#### Installations
If the repository is downloaded and the notebooks would liked to be ran using Jupyter Notebook/Lab, please install the dependencies below:

- [Quandle](https://docs.quandl.com/docs/python-installation)
- [Installing Quandle](https://docs.quandl.com/docs/python-installation)
- [Installing Scikit Learn](http://scikit-learn.org/stable/install.html)
- [Installing Prophet](https://github.com/facebook/prophet)
- [BeakerX](http://beakerx.com/)
----------

<a class="anchor" id="Directory-Structure"></a>

## Directory Structure

An index of both directories are provided below.
### Stocks:

The [Stocks](https://github.com/adam-delreal/Capstone/tree/master/stocks) directory has notebooks analyzing *Apple, Inc.* and are broken down as:

#### Continuous Data Analysis, Preprocessing, and Modeling:

- Apple [Exploratory Data Analysis](https://github.com/adam-delreal/Capstone/blob/master/stocks/Apple_EDA.ipynb) on Historical Stock Data.
- Apple Exploratory Data Analysis [Interactive Graphs](https://github.com/adam-delreal/Capstone/blob/master/stocks/Apple_EDA_BeakerX.ipynb).
- Apple [Preparing the Data](https://github.com/adam-delreal/Capstone/blob/master/stocks/Apple_Model_1_Data_Prep.ipynb) for Regression Modeling.
- Apple Modeling: [Linear Regression](https://github.com/adam-delreal/Capstone/blob/master/stocks/Apple_Model_2_Linear_Regression.ipynb).
- Apple Modeling: [Random Forest Regression](https://github.com/adam-delreal/Capstone/blob/master/stocks/Apple_Model_3_Random_Forest.ipynb)
- Apple Modeling: [Bagging Regression on a Random Forest](https://github.com/adam-delreal/Capstone/blob/master/stocks/Apple_Model_4_Bagging_Regressor.ipynb).
- Apple Modeling: [Facebook Prophet](https://github.com/adam-delreal/Capstone/blob/master/stocks/Apple_Model_5_Prophet.ipynb).

#### Classification Data Analysis, Preprocessing, and Modeling:

-  Apple Exploratory Data Analysis [with the SEC Data](https://github.com/adam-delreal/Capstone/blob/master/sec/Apple_SEC_EDA.ipynb).
- Apple [Preparing the Data](https://github.com/adam-delreal/Capstone/blob/master/stocks/Apple_Model_Classification_1_Prep.ipynb) for Classification Modeling.
- Apple [Preprocessing the Data](https://github.com/adam-delreal/Capstone/blob/master/stocks/Apple_Model_Classification_2_Data_Preprocessing.ipynb) for Classification Modeling.
- Apple Modeling: [Random Forest Classification](https://github.com/adam-delreal/Capstone/blob/master/stocks/Apple_Model_Classification_3_Random_Forest.ipynb).

---------

### SEC:

The [SEC](https://github.com/adam-delreal/Capstone/tree/master/sec) directory, has notebooks scraping and analyzing Apple's SEC Filings.

- SEC [Scraper](https://github.com/adam-delreal/Capstone/blob/master/sec/Apple_SEC_Scraper.ipynb).
- SEC [Exploratory Data Analysis](https://github.com/adam-delreal/Capstone/blob/master/sec/Apple_SEC_EDA.ipynb).

------- 
<a class="anchor" id="Exploratory-Data-Analysis"></a>
## Exploratory Data Analysis 

When inspecting the raw data frame from Quandle, we can see that thirteen features are provided: Date, Open, High, Low, Close, Volume, Dividends , Split Ratio, Adjusted Open, Adjusted High, Adjusted Low, Adjusted Close, Adjusted Volume. These features can be categorized into four classes: the date, the regular prices, the adjusted prices, and the miscellaneous. The date range on the stock data begins on Apple's IPO date, December 12, 1980, and ends on March 27, 2018. Each day the stock market was open, four aspects of the price were taken into account, these are known as the *regular prices*:

-   *Open*: the price of the security when the market opens.
    
-   *High*: the highest price of the security within a given day.
    
-   *Low*: the lowest price of the security within a given day.
    
-   *Close*: the final price of the security when the market closes.
    
- *Volume*: the amount of shares exchanged during a given day.

<img src="https://github.com/adam-delreal/Capstone/tree/master/images/open_close.png">

During the course of a given day, many factors may affect the price of a security. For instance, a well-regarded announcement of new product, bad news relating to the company, or any distributions made to investors. Distributions refer to a company's payment of stock to its shareholders or, *dividends*. Dividends may be paid in the form of cash, stock, or stock splits--a stock split is a corporate action to boost the liquidity (assets) of the shares by dividing its existing shares into multiple shares. When distributions are made, the adjusted prices are amended using the value of the dividends and deducting them from the regular price. Therefore, adjusted prices are often used to examine and analyze historical returns.

When analyzing Apple's stocks, we can see the sudden drop in 2014. This is the result of splitting shares. In the EDA, we can see the fluctuation in the regular prices during 2014 as a sudden drop occurred. However, when analyzing the adjusted prices, we can see the distributions causing the data to be regularized. 

-------
<a class="anchor" id="Feature-Engineering"></a>
## Feature Engineering


In order to do an indicative technical analysis, a few types of trends were engineered using the data provided. Moving averages were calculated for a short (12-Day), medium (26-Day), and long (85-Day) trend. 
A *moving average* helps smoothen a price by filtering out the *noise* from random fluctuations in price as it follows a trend, or lag, based on historical prices. Two types of moving averages were calculated: a **simple moving average** (SMA), which is calculated by adding the most recent price and dividing that value by the number of time periods computing the average. And, an **exponential moving average**, which is similar to the SMA, but an exponential weight is applied to all observations in a period of time. 

My prior assumptions presumed these features would be a good indicator in forecasting the adjusted price of a security and this was put to the test after processing the data.

------- 

<a class="anchor" id="Preprocessing-Data"></a>

## Preprocessing Data

Given that the data is structured in time-sequence, slitting the data into a train and test set was done manually. Reason being, the training data is based on  sequential historical prices and cannot be shuffled. 

After splitting the data, the data was preprocessed using scikit learn's *MinMaxScaler*, which serves as an estimator as it scales and translates each feature individually assigning the feature a value accordingly between negative one and positive one.

-----
#### Lessons Learnt: 

During this stage of the project, I struggled figuring out a decisive strategy to split the data. Thankfully, I had the guidance and help of my local instructor Douglas, who explained the reasoning behind not only splitting the data manually, but also, *shifting* the data frame one day into the future to forecast the last day in the dataset, March 27, 2018. 

-----

 Once the data was engineered and featured, the adjusted closing price was set as the label/target to be predicted. At this point the data was ready to be modeled.


------- 
<a class="anchor" id="Optimal-Model"></a>

## Optimal Model

After attempting several models and obtaining relatively mediocre results, Facebook's Prophet library resulted in a decent prediction. The model has the ability to predict certain periods into the future. Although the dataset ended on March 27, 2018, the Prophet has the capability to predict many periods. As of today, June 13, 2018, Apple's closing price stock is priced at $191.33, while prophet forecasted this date as $188.20. Although the predicted value is off by approximately $3, this a great prediction! 

------- 
<a class="anchor" id="Conclusion"></a>

## Conclusion

In conclusion, my assumptions were proven wrong when using the scikit-learn models, but may have been great features for the Prophet model. Forecasting the stock market is not a feasible task. In addition to this analysis, I hope to provide a lessons learnt log explains the hard tasks encountered, the discussion with my instructors and teacher assistants, and from books/articles I read. I hope the concepts are clear and the navigation through the notebook was intuitive. Thanks for taking the time to read this!

------

<a class="anchor" id="Credits"></a>
## Credits

Special thanks to:

- Douglas Strodtman for providing the guidance, assistance, and mentorship to complete the project. 
- Wesley Bosse for his assistance, recommendations, and for taking the time to explain high-level developer practices.

Both Douglas and Wes were crucial for the completion of this project and I am very grateful for their constant help throughout the course.
