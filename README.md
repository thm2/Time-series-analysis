# Time-series-analysis

This project concerns the Wisconsin CO2 dataset. It focuses on the monthly CO2 emissions of Wisconsin,
and analyzes it using time-series analysis techniques. The methods that will be used will be time-series analysis methods and spectral analysis methods. The former concerns analyzing time-series such as the Wisconsin dataset, and this analysis will be made in section
Analysis B that follows. The analysis includes splitting the data into train and testing datasets, and using
the train dataset to fit two models. Then, the performance of these models will be used on the test dataset.
The best of these models will be used to predict the CO2 emissions for the five time points, that is, for the
next five months. Moreover, after plotting the time-series in question, there seems to be seasonality existing in the CO2
emissions versus month as the timescale. For this reason, in section Analysis C, Spectral Analysis will be
used, which is suited for finding underlying periodicity patterns.


# Results

In the Analysis B section the ARIMA(0,2,2)x(0,1,1)(12) model was picked as the best model but the
ARIMA(0,1,1)x(0,1,1)(12) was not far behind. Even though the former is better from a statistical point
of view, the latter is perhaps closer to what someone would expect from looking at the time-series plot
in Analysis B. This is because, there seems to be an increasing linear trend, which is made stationary by
differencing once, that is, by using d = 1. However, the plot could hide that the trend is in fact quadratic,
hence the twice-trend-differenced model. The seasonality is 12 for both.

The Analysis C section confirmed the existence of a trend with the existence of the 0 frequency in the
periodogram. It also verified the existence of the 12-month seasonality of the CO2 emission time-series,
with a strong frequency at 0.083333333, which significes a period of the inverse of the frequency, that is, a
CO2-emission period of 12 months.
