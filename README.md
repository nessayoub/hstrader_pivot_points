# HsTrader-Pivot-Points


This code demonstrates the usage of the `hstrader` library to fetch market data and calculate pivot points for the EURUSD currency pair.

About the HsTrader Library
-------------------------

The `hstrader` library is a Python package that provides a convenient interface to interact with the HotSpot trading platform. It allows you to fetch market data, place orders, and manage your trading account. The library abstracts the underlying API calls, making it easier for developers to build trading applications.

Pivot Points Calculation
-----------------------

The code calculates the following pivot points:

* **Pivot Point (P)**: `(High + Low + Close) / 3`
* **Resistance 1 (R1)**: `(2 * P) - Low`
* **Support 1 (S1)**: `(2 * P) - High`
* **Resistance 2 (R2)**: `P + (High - Low)`
* **Support 2 (S2)**: `P - (High - Low)`
* **Resistance 3 (R3)**: `High + 2 * (P - Low)`
* **Support 3 (S3)**: `Low - 2 * (High - P)`

These pivot points are used to identify potential support and resistance levels in the market.

Usage
-----

### Install dependencies
```pip install hstrader```

### Replace credentials

Replace the `CLIENT_ID` and `CLIENT_SECRET` variables with your own HotSpot trading platform credentials.

### Run the script

Run the notebook to fetch the market data, calculate the pivot points, and display the results in both Matplotlib and Plotly visualizations.

Visualizations
--------------

The code provides two types of visualizations:

### Matplotlib Candlestick Chart with Pivot Points

This chart displays the candlestick pattern of the EURUSD currency pair along with the calculated pivot points.

### Plotly Candlestick Chart with Pivot Points

This chart also displays the candlestick pattern of the EURUSD currency pair, but the pivot points are added as horizontal lines for better visibility.

These visualizations can help traders identify potential support and resistance levels in the market.
