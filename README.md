# HsTrader-Pivot-Points

![Pivot points](img/Visualization.png)

This code demonstrates the usage of the `hstrader` library to fetch market data and calculate pivot points for the EURUSD currency pair.

## About the HsTrader Library

The `hstrader` library is a Python package that provides a convenient interface to interact with the HsTrader trading platform. It allows you to fetch market data, place orders, and manage your trading account. The library abstracts the underlying API calls, making it easier for developers to build trading applications.

## Pivot Points Calculation

The code calculates the following pivot points:

- **Pivot Point (P)**: `(High + Low + Close) / 3`
  The pivot point is a weighted average of the high, low, and close prices of a security. It's a key level that indicates the overall trend and is used as a reference point for calculating resistance and support levels.
- **Resistance 1 (R1)**: `(2 * P) - Low`
  R1 is a level of resistance above the pivot point. It's calculated by taking the pivot point and subtracting the low price. This level is expected to act as a barrier to upward price movement.
- **Support 1 (S1)**: `(2 * P) - High`
  S1 is a level of support below the pivot point. It's calculated by taking the pivot point and subtracting the high price. This level is expected to act as a floor to downward price movement.
- **Resistance 2 (R2)**: `P + (High - Low)`
  R2 is a stronger level of resistance above R1. It's calculated by adding the range of the high and low prices to the pivot point. This level is expected to be a more significant barrier to upward price movement.
- **Support 2 (S2)**: `P - (High - Low)`
  S2 is a stronger level of support below S1. It's calculated by subtracting the range of the high and low prices from the pivot point. This level is expected to be a more significant floor to downward price movement.
- **Resistance 3 (R3)**: `High + 2 * (P - Low)`
  R3 is an even stronger level of resistance above R2. It's calculated by adding twice the difference between the pivot point and the low price to the high price. This level is expected to be a significant barrier to upward price movement.
- **Support 3 (S3)**: `Low - 2 * (High - P)`
  S3 is an even stronger level of support below S2. It's calculated by subtracting twice the difference between the high price and the pivot point from the low price. This level is expected to be a significant floor to downward price movement.

These pivot points are used to identify potential support and resistance levels in the market.

## Usage

### Install dependencies

`pip install hstrader`

### Replace credentials

Replace the `CLIENT_ID` and `CLIENT_SECRET` variables with your own HsTrader trading platform credentials.

### Run the script

Run the notebook to fetch the market data, calculate the pivot points, and display the results in both Matplotlib and Plotly visualizations.

## Visualizations

The code provides two types of visualizations:

### Matplotlib Candlestick Chart with Pivot Points

This chart displays the candlestick pattern of the EURUSD currency pair along with the calculated pivot points.

### Plotly Candlestick Chart with Pivot Points

This chart also displays the candlestick pattern of the EURUSD currency pair, but the pivot points are added as horizontal lines for better visibility.

These visualizations can help traders identify potential support and resistance levels in the market.
