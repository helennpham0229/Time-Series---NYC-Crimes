# Time-Series-NYC-Crimes

## 1. Introduction

US has been grappling with crimes for decades now and has made significant improvements. However, crime remains to be one of the core societal problems in the US and in New York City (NYC) specifically. To build a safer society, we can analyze crime patterns and forecast future occurrences of crime. In addition, there have been multiple research studies examining the relationship between socioeconomic status and crime statistics which can help to improve relations with the local communities.

In this project, we will explore the patterns of crimes in each NYC borough (the Bronx, Brooklyn, Manhattan, Queens, and Staten Island) and observe how socioeconomic factors (incomes, unemployment rate, and educational attainment) impact the number of crimes. This can help criminal justice professionals and government officials understand whether their initiatives are successful. It also allows for a dialogue between law enforcement and the public they serve.

## 2. Data

NYPD Arrests Data (Historic) - https://catalog.data.gov/dataset/nypd-arrests-data-historic

Median Incomes - https://data.cccnewyork.org/data/map/66/median-incomes#66/39/2/107/62/a/a

Unemployment Rate - https://data.cccnewyork.org/data/map/85/unemployment-rate#85/a/2/131/62/a/a

Educational Attainment - https://data.cccnewyork.org/data/map/1243/educational-attainment#1243/182/2/1419/62/a/a

## 3. Methods

In this project, we will forecast number of crimes in each borough in NYC using 
- ARIMA: Past time points of time series data can impact current and future time points. ARIMA models take this concept into account when forecasting current and future values. ARIMA uses a number of lagged observations of time series to forecast observations. A weight is applied to each of the past term and the weights can vary based on how recent they are.

- Facebook Prophet: Prophet is a procedure for forecasting time series data based on an additive model where non-linear trends are fit with yearly, weekly, and daily seasonality, plus holiday effects. It works best with time series that have strong seasonal effects and several seasons of historical data. Prophet is robust to missing data and shifts in the trend, and typically handles outliers well.

- Holt-Winters Exponential Smoothing: Exponential smoothing assigns exponentially decreasing weights and values against historical data to decrease the value of the weight for the older data. It is used for forecasting time series data that exhibits both a trend and a seasonal variation.

## 4. Exploratory Data Analysis

### Crime categories

![](https://raw.githubusercontent.com/helennpham0229/Time-Series-NYC-Crimes/main/images/crime_categories.png)

### Number of crimes in each borough

![](https://raw.githubusercontent.com/helennpham0229/Time-Series-NYC-Crimes/master/images/crimes_by_borough.png)

### Genders

![](https://raw.githubusercontent.com/helennpham0229/Time-Series-NYC-Crimes/master/images/crimes_by_genders.png)

### Races

![](https://raw.githubusercontent.com/helennpham0229/Time-Series-NYC-Crimes/master/images/crimes_by_races.png)

### Total number of crimes by year

![](https://raw.githubusercontent.com/helennpham0229/Time-Series-NYC-Crimes/master/images/crimes_by_year.png)

### Crimes in each borough by year

![](https://raw.githubusercontent.com/helennpham0229/Time-Series-NYC-Crimes/master/images/crimes_by_borough_by_year.png)

### Education attainment: Less than high school degree

![](https://raw.githubusercontent.com/helennpham0229/Time-Series-NYC-Crimes/master/images/less_than_hs.png)

### Education attainment: Bachelor's degree or higher

![](https://raw.githubusercontent.com/helennpham0229/Time-Series-NYC-Crimes/master/images/bach_degree.png)

### Median household income

![](https://raw.githubusercontent.com/helennpham0229/Time-Series-NYC-Crimes/master/images/income.png)

### Unemployment rate

![](https://raw.githubusercontent.com/helennpham0229/Time-Series-NYC-Crimes/master/images/unemployment.png)

## 5. Results
### ARIMA
#### Bronx

![](https://raw.githubusercontent.com/helennpham0229/Time-Series-NYC-Crimes/master/images/sarimax_bronx.png)

#### Brooklyn
![](https://raw.githubusercontent.com/helennpham0229/Time-Series-NYC-Crimes/master/images/sarimax_brooklyn.png)

#### Manhattan

![](https://raw.githubusercontent.com/helennpham0229/Time-Series-NYC-Crimes/master/images/sarimax_manhattan.png)

#### Queens

![](https://raw.githubusercontent.com/helennpham0229/Time-Series-NYC-Crimes/master/images/sarimax_queens.png)

#### Staten Island

![](https://raw.githubusercontent.com/helennpham0229/Time-Series-NYC-Crimes/master/images/sarimax_staten.png)

### Facebook Prophet
#### Bronx

![](https://raw.githubusercontent.com/helennpham0229/Time-Series-NYC-Crimes/master/images/prophet_bronx.png)

#### Brooklyn

![](https://raw.githubusercontent.com/helennpham0229/Time-Series-NYC-Crimes/master/images/prophet_brooklyn.png)

#### Manhattan

![](https://raw.githubusercontent.com/helennpham0229/Time-Series-NYC-Crimes/master/images/prophet_manhattan.png)

#### Queens

![](https://raw.githubusercontent.com/helennpham0229/Time-Series-NYC-Crimes/master/images/prophet_queens.png)

#### Staten Island

![](https://raw.githubusercontent.com/helennpham0229/Time-Series-NYC-Crimes/master/images/prophet_staten.png)

### Holt-Winters Exponential Smoothing
#### Bronx

![](https://raw.githubusercontent.com/helennpham0229/Time-Series-NYC-Crimes/master/images/hwes_bronx.png)

#### Brooklyn

![](https://raw.githubusercontent.com/helennpham0229/Time-Series-NYC-Crimes/master/images/hwes_brooklyn.png)

#### Manhattan

![](https://raw.githubusercontent.com/helennpham0229/Time-Series-NYC-Crimes/master/images/hwes_manhattan.png)

#### Queens

![](https://raw.githubusercontent.com/helennpham0229/Time-Series-NYC-Crimes/master/images/hwes_queens.png)

#### Staten Island

![](https://raw.githubusercontent.com/helennpham0229/Time-Series-NYC-Crimes/master/images/hwes_staten.png)

## 6. Conclusion and Recommendations
- SARIMAX is the best model for predicting crimes in NYC.
- The number of crimes continue to have decreasing trend in the next 5 years
- SARIMAX - handles seasonality component better but takes longer to learn/train
- Prophet - show outliers and seasonality each year
- HWES - shorter amount of time to train the time series
- Increase law enforcement officials in all boroughs in early winter (late November - late Dec). Also early spring (March/April) for Staten Island and Queens
- Establish programs to support the Bronx because it has the lowest income/education and highest unemployment/crime


## 7. Future Works
- Model with LSTM neural networks
- Obtain 2020 data and adjust models for pandemic-related factors
- Incorporate longitude and latitude data to observe the more dangerous spots/areas
