ADF Test
The ADF Test code performs analysis on a data file using time series techniques to determine the stationarity of a time series. The Augmented Dickey-Fuller (ADF) test is utilized, and the code provides summary statistics and test results including the ADF statistic, p-value, and critical values.

Prerequisites
Make sure you have the following libraries installed:

numpy
matplotlib
pmdarima
pandas
statsmodels
Usage
Place the data file in the same directory as the code or provide the full path as a string in the pd.read_csv method.
Run the code to analyze the data and obtain the ADF test results. Ensure that the data is formatted with a date column and a corresponding data column.
Code Explanation
The code begins by loading the data from the specified file using pandas. The date column is parsed as a datetime type and set as the index of the dataframe.

Next, the data is split into training and test sets, with the training set containing 80% of the data.

The ADF test is then performed on the training data to determine the stationarity of the time series. The ADF statistic, p-value, and critical values are calculated.

The summary statistics of the training data are printed, followed by the ADF test results. If the ADF statistic is lower than the critical value at a given significance level (e.g., 5%), the null hypothesis of non-stationarity is rejected, indicating that the time series is stationary. Conversely, if the ADF statistic is higher, the null hypothesis is not rejected, suggesting that the time series is not stationary.

Result Interpretation
The ADF test helps in understanding the stationarity of the time series data. Stationarity is a desirable property for many time series analysis techniques as it allows for more reliable forecasting and analysis.

By analyzing the ADF statistic, p-value, and critical values, you can determine whether the data exhibits stationarity or not. The summary statistics of the training data provide an overview of the data's distribution and central tendencies.
