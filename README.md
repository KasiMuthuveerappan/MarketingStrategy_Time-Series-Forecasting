# Time-Series-Forecasting

<h1 align='center'> <font color='grey'><font size=7>⏳💰MarketingStrategy <font color="orange"><b>AdEase</font> - Time Series Forcasting💰⏳</b></font> </font></h1>

  <kbd>

  ![maxresdefault](https://github.com/user-attachments/assets/73c0d047-8d58-4d7e-b285-5a3094e5fd12)

  </kbd>  

> ### ❕About:
Ad Ease is an ads and marketing based company helping businesses elicit maximum clicks @ minimum cost. AdEase is an ad infrastructure to help businesses promote themselves easily, effectively, and economically. The interplay of 3 AI modules - Design, Dispense, and Decipher, come together to make it this an end-to-end 3 step process digital advertising solution for all.

> ### 🤔Problem Statement:
You are working in the Data Science team of Ad ease trying to understand the per page view report for different wikipedia pages for 550 days, and forecasting the number of views so that you can predict and optimize the ad placement for your clients. You are provided with the data of 145k wikipedia pages and daily view count for each of them. Your clients belong to different regions and need data on how their ads will perform on pages in different languages.


> ### 🗒️Dataset:

https://drive.google.com/drive/folders/1mdgQscjqnCtdg7LGItomyK0abN6lcHBb


> ### 📖Data Dictionary:

There are two csv files given

- train_1.csv: In the csv file, each row corresponds to a particular article and each column corresponds to a particular date. The values are the number of visits on that date.

The page name contains data in this format:

SPECIFIC NAME _ LANGUAGE.wikipedia.org _ ACCESS TYPE _ ACCESS ORIGIN

having information about the page name, the main domain, the device type used to access the page, and also the request origin(spider or browser agent)


- Exog_Campaign_eng: This file contains data for the dates which had a campaign or significant event that could affect the views for that day. The data is just for pages in English.

There’s 1 for dates with campaigns and 0 for remaining dates. It is to be treated as an exogenous variable for models when training and forecasting data for pages in English



> ### 📒 Methodology:

- Exploratory data analysis

- Time Series forecasting- ARIMA, SARIMAX, and Prophet

> ### 📦 Business Context:
To understand the per page view report for different wikipedia pages for 550 days.

To forecast the number of views to predict and optimize the ad placement for clients.

To provide clients (different regions) with data on how their ads will perform on pages in different languages.

> ### 📒 Steps Performed:

**Data Pre-processing:** Cleaned and transformed raw data for analysis.

**Exploratory Data Analysis:** Explored key patterns, relationships, and trends in the dataset.

**Feature Engineering:** Created new features to enhance model predictions.

**Data Aggregation by Language:** Grouped data by language to identify specific trends and insights.

**Graphical Data Analysis:** Visualized data, including ACF & PACF plots, to identify correlations and lags.

**Time Series Decomposition:** Analyzed trends, seasonality, and residuals using decomposition.

**Stationarity Tests:** Performed Dickey-Fuller test to confirm data stationarity.

**Forecasting Techniques:** Applied several time series forecasting models to achieve MAPE < 5%:

      i. Simple Exponential Smoothing
      
      ii. Double Exponential Smoothing
      
      iii. Triple Exponential Smoothing
      
      iv. Auto Regression, Moving Average, ARIMA, SARIMA, and SARIMAX models
      
      v. Facebook Prophet Library


> ### ♾️Inferences:

  The dataset includes mediawiki and commons.wikimedia pages that host media content.
  
**Language Distribution:** Out of 7 languages, English has the highest proportion, followed closely by Japanese. Other languages have a similar proportion of around ~12%.

**Access Origin:** 24% of the pages are accessed via spiders (automated tools), while 76% are accessed by all-agents (general users).

**Access Type:** About 50% of the pages are accessed via "all-access" (combined), with the remaining ~25% each for desktop and mobile-web.

**View Spikes:**

    In August 2016, a spike in daily average views is observed for both English and Russian pages.
    
    Another spike is observed in November 2016, this time for Spanish, Russian, and German pages.
    
**Trend & Seasonality:**

    English page views show both trend and seasonality.
    
    Other languages primarily show seasonality without significant trending patterns.
    
**Median Daily Views:**

    Spanish language pages have higher median daily views compared to others.
    
    A noticeable drop is seen in median daily views for Spanish, Russian, and English pages.
    
    Towards the later months of 2016, English median daily views are on par with Spanish.

> ### 🪈Recommendations:
**Increase Ads on English Pages:** Since English pages have higher average daily views, more ad campaigns should be targeted towards these pages for better reach.

**Leverage All-Access Pages:** With over 50% of pages in the all-access category, this provides a broader reach compared to targeting only desktop or mobile-web users.

**Enhance Training Data:** Adding language information for mediawiki and commons.wikimedia pages could further improve model accuracy.

**Utilize Exogenous Data:** Just like the inclusion of campaign data improved English page predictions, obtaining exogenous data for other languages will enhance model performance.

**Further Experimentation with Prophet:** With more time and resources, experimenting with Prophet parameters could yield even lower MAPE values and better forecasts.
