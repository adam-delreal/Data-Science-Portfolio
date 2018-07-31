# Financial Modeling: Forecasting Securities

This project showcases an attempt to forecast securities using technical indicators, such as historical stock data and reports from the United States Securities & Exchange Commission (SEC). In doing so, various supervised regression & classification machine learning models have been tested and interpreted.


## Table of Contents

- [Project Scope](#Scope)
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

<a class="anchor" id="Scope"></a>
## Project Scope 



The problem at hand is to forecast securities using various supervied machine learning models on historical stock data and SEC Report Filings. 

<a class="anchor" id="Assumptions"></a>
## Assumptions


**Initial Assumption:** the market moves in trends, therefore engineering short, medium, and long term trends (moving averages) will be proved signal for the machine learning model and will serve as a decent trading strategy. 

<a class="anchor" id="Introduction"></a>
## Introduction

This project is broken down into two main sub-directories both containing: Data Acquisition,  Data Analysis, Data Engineering, Data Processing, and Supervised Machine Learning Models.
- [Supervised Regression Models](https://github.com/adam-delreal/Capstone/tree/master/1_Predicting_Stock_Prices)

- [Supervised Classification Models](https://github.com/adam-delreal/Capstone/tree/master/2_Classification_Modeling)

### Data Acquisition:

**[Quandle's API](https://www.quandl.com/)**:
 The stock data was sourced from [Quandle's API](https://www.quandl.com/) and contains historical stock prices since the company's Initial Price Offering (IPO), which is the very first offering of the stock a company issues to the public.

**[SEC Website](https://www.sec.gov/)**:
The [SEC website](https://www.sec.gov/) was scraped using the *BeautifulSoup* and *Requests* libraries. 

<a class="anchor" id="Built-With"></a>
## Built with


#### Tools:
- [Python](https://www.python.org/)
- [Jupyter Notebook/Lab](http://jupyter.org/index.html)
- [Seaborn](https://seaborn.pydata.org/introduction.html)
- [Matplotlib](https://matplotlib.org/)
- [Numpy](http://www.numpy.org/)
- [Pandas](https://pandas.pydata.org/)
- [BeautifulSoup](https://www.crummy.com/software/BeautifulSoup/bs4/doc/)
- [Quandle](https://www.quandl.com/)
- [Scikit Learn](http://scikit-learn.org/stable/index.html#)
- [Facebook Prophet](https://research.fb.com/prophet-forecasting-at-scale/)



#### Installations:
If the repository is downloaded and the notebooks would liked to be ran using Jupyter Notebook/Lab, please install the following dependencies:

- [Installing Jupyter](http://jupyter.org/install)
- [Installing Quandle](https://docs.quandl.com/docs/python-installation)
- [Installing Scikit Learn](http://scikit-learn.org/stable/install.html)
- [Installing Prophet](https://github.com/facebook/prophet)


<a class="anchor" id="Directory-Structure"></a>

## Directory Structure



### Supervised Regression Models:
 #### [Predicting Stock Prices:](https://github.com/adam-delreal/Capstone/tree/master/1_Predicting_Stock_Prices)
   - [Exploratory Data Analysis on the Stock Data](https://github.com/adam-delreal/Capstone/blob/master/1_Predicting_Stock_Prices/1_EDA.ipynb)
	   - [Visualization](#VS)
	   - [Data Engineering](#FE2)
    - [Preparing the Data](https://github.com/adam-delreal/Capstone/blob/master/1_Predicting_Stock_Prices/2_Data_Prep.ipynb)
	    - [Shifting the Dates & Data Engineering](#Shifting)
    - [Facebook Prophet Models:](https://github.com/adam-delreal/Capstone/blob/master/1_Predicting_Stock_Prices//3_Prophet.ipynb)
	    - [Prophet Regression Model](#FBProphet)
	    - [Visualizing Results](#FBProphetVIS)
    - [Linear Regression Models](https://github.com/adam-delreal/Capstone/blob/master/1_Predicting_Stock_Prices/5_Linear_Regression_Models.ipynb):	
		 - [(OLS) Linear Regression Model](http://localhost:8888/notebooks/Desktop/Portfolio/Financial_Modeling/1_Predicting_Stock_Prices/5_Linear_Regression_Models.ipynb#LRModeling)
		- [Principal Component Analysis on an OLS Model](http://localhost:8888/notebooks/Desktop/Portfolio/Financial_Modeling/1_Predicting_Stock_Prices/5_Linear_Regression_Models.ipynb#PCA)
		-  [Bagging Regression Model](http://localhost:8888/notebooks/Desktop/Portfolio/Financial_Modeling/1_Predicting_Stock_Prices/5_Linear_Regression_Models.ipynb#Bagging)
		- [AdaBoost](http://localhost:8888/notebooks/Desktop/Portfolio/Financial_Modeling/1_Predicting_Stock_Prices/5_Linear_Regression_Models.ipynb#Adaboost)
    - [Random Forest Regression Models:](https://github.com/adam-delreal/Capstone/blob/master/1_Predicting_Stock_Prices/6_Random_Forest_Reg_Models.ipynb)
	    -  [Random Forest Regression Model](#RFModel)
	    - [Principal Component Analysis](#PCA)
	    - [Gridsearch Pipeline](#Gridsearch)
	- [Bagging Regression Models with a Random Forest Estimator:](https://github.com/adam-delreal/Capstone/blob/master/1_Predicting_Stock_Prices/6_Random_Forest_Reg_Models.ipynb)
		-  [Bagging Model](#Bagging)
	    - [Principal Component Analysis](#PCA)
	    - [Gridsearch Pipeline](#Gridsearch)

### Supervised Classification Models:

- [Scraping the Data](https://github.com/adam-delreal/Capstone/blob/master/1_SEC_Scraper.ipynb)
	-  [Scraping the SEC](#Scraping)
-  [SEC: Exploratory Data Analysis](https://github.com/adam-delreal/Capstone/blob/master/2a_EDA_SEC.ipynb)
	-   [Data Visualization](http://localhost:8888/notebooks/Desktop/Portfolio/Financial_Modeling/2_Classification_Modeling/2a_EDA_SEC.ipynb#VIS)
	-   [Data Engineering](http://localhost:8888/notebooks/Desktop/Portfolio/Financial_Modeling/2_Classification_Modeling/2a_EDA_SEC.ipynb#FE)
- [Exploratory Data Analysis with the Stock Data](https://github.com/adam-delreal/Capstone/blob/master/2b_EDA_wStock_Data.ipynb)
	- [Data Visualization](#8K)
- [Preparing the Data](https://github.com/adam-delreal/Capstone/blob/master/3a_Data_Prep.ipynb)
	- [Data Engineering](#FE)
	- [Merging the Engineered Stock Data & SEC](#PCT)
- [Preprocessing the Data](https://github.com/adam-delreal/Capstone/blob/master/3b_Data_Preprocessing.ipynb) 
	- [Shifting the Dates](http://localhost:8888/notebooks/Desktop/Portfolio/Financial_Modeling/2_Classification_Modeling/3b_Data_Preprocessing.ipynb#Shifting)
	-  [Splitting the Data](http://localhost:8888/notebooks/Desktop/Portfolio/Financial_Modeling/2_Classification_Modeling/3b_Data_Preprocessing.ipynb#Splitting)
- [Random Forest Classification Models](https://github.com/adam-delreal/Capstone/blob/master/4_Random_Forest_Models.ipynb)
	-  [Random Forest Classification](#RFC)
    - [Bagging Classification](#Bagging)
    - [GridSearching a Random Forest](#Gridsearch)
    - [GridSearching a Bagging Classifier](#Gridsearch2)


<a class="anchor" id="Exploratory-Data-Analysis"></a>
## Exploratory Data Analysis 

### Historical Stock Data:

When inspecting the raw data frame from Quandle, we can see that thirteen features are provided: Date, Open, High, Low, Close, Volume, Dividends, Split Ratio, Adjusted Open, Adjusted High, Adjusted Low, Adjusted Close, Adjusted Volume. These features can be categorized into four classes: date, regular prices, adjusted prices, and miscellaneous. 

For each day the stock market was open, four aspects of the price were taken into account, known as the *regular prices*. Additionally, *volume* is another attribute:

-   *Open*: the price of the security when the market opens.
    
-   *High*: the highest price of the security within a given day.
    
-   *Low*: the lowest price of the security within a given day.
    
-   *Close*: the final price of the security when the market closes

- *Volume*: the amount of shares exchanged during a given day.


During the course of a given day, many factors may affect the price of a security. For instance, a well-regarded announcement of new product, bad news related to the company, or any distributions made to investors.

 - **Distributions** refer to a company's payment of stock to its shareholders,  known as *dividends*. Dividends may be paid in the form of cash, stock, or stock splits.
 - **Stock Splits:** a stock split is a corporate action to boost the liquidity (assets) of the shares by dividing its existing shares into multiple shares. 

When distributions are made, the **Adjusted Prices** are amended by using the value of the dividends and deducting them from the regular price. Therefore, adjusted prices are often used to examine and analyze historical returns.

When analyzing Apple's stocks, we can see the sudden drop of value in 2014. This is the result of *splitting shares*. However, when analyzing the adjusted prices, the drop is normalized and the drop is not apparent.


<a class="anchor" id="Feature-Engineering"></a>
## Feature Engineering


A few types of trends were engineered to perform an indicative technical analysis. 

**Moving Averages** were calculated for a short (12-Day), medium (26-Day), and long (85-Day) trend. 
A *moving average* helps smoothen a price by filtering out the *noise* from random fluctuations in the price as it follows a trend/lag based on historical prices. Two types of moving averages were calculated:
- **Simple Moving Average (SMA):** is calculated by adding the most recent price and dividing that value by the number of time periods computing the average. 
- **Exponential Moving Average (EMA):** similar to the SMA, but an exponential weight is applied to all observations in the period of time. 

The initial assumption presumed these features would serve as a signal for a machine learning model.


<a class="anchor" id="Preprocessing-Data"></a>

## Preprocessing Data
### Train/Test Split:
Given the data is structured in time-series sequence, a simple train/test split would with cross validation will not be ideal because the data should not be shuffled; therefore, manually splitting the data into a Training and Testing set was the correct approach.
### Normalizing the Data:
After splitting the data, the data was preprocessed using scikit learn's *MinMaxScaler*, which serves as an estimator as it scales and translates each feature individually assigning the feature a value accordingly between zero and positive one. 
###  Label:
The *Adjusted Closing Price* was set as the target to be predicted. 

-----
#### Lessons Learned: 

During this stage of the project, I struggled figuring out a decisive strategy to split the data. Thankfully, I had the guidance and help of my local instructor Douglas, who explained the reasoning behind not only splitting the data manually, but also, *shifting* the data frame one day into the future to forecast the last day in the dataset.



<a class="anchor" id="Optimal-Model"></a>

## Optimal Model

Facebook's Prophet does a decent job forecasting stock prices.  Although a stock dataset may end months ago, the model has the ability to predict certain periods into the future via adjusting a parameter. 

### Forecast:
Today, is July 28, 2018 and the model forecasted:
|Date | Current Price | Predicted |
|------|------|------|
| 2018/07/28| 190.98 | 189.64 

#### Evaluation: 
- The illustration below demonstrates the model is relatively overfit. An overfit model generally takes the form of the idiosyncrasies in the data too well, as we can see in the blue line labeled as `yhat`.
    - **Overfitting** is a modeling error that occurs when a function is excessively closely fitting to the data points in the training set. 
    
    - **Idiosyncratic Error** describes the error in sequential data that changes over time and across units; this can be perceived as trends.

<a class="anchor" id="Conclusion"></a>

## Conclusion

In conclusion, my assumptions were proven wrong when I trained shallow supervised models. 


<a class="anchor" id="Credits"></a>
## Credits

Special thanks to:

- Douglas Strodtman for providing the guidance, assistance, and mentorship to complete the project. 
- Wesley Bosse for his assistance, recommendations, and for taking the time to explain high-level developer practices.

Both Douglas and Wes were crucial for the completion of this project and I am very grateful for their help when I approached them.
