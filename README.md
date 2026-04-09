# Demand Forecasting For Logistics

This application provides demand forecasting for logistics across multiple US states using Facebook Prophet models. Users can generate forecasts at daily, weekly, monthly, or yearly granularity with interactive visualizations.

## How to Use

1. Install the app.
2. The Streamlit interface opens with two tabs: **Forecast** and **Historical Data**.

### Forecast Tab
1. Select a **State** from the dropdown (California, Texas, New York, Florida, Illinois).
2. Choose a **Frequency** (daily, weekly, monthly, yearly).
3. Enter the **Number of Periods** to forecast.
4. Click **Forecast** to view predicted demand and an interactive chart.

### Historical Data Tab (Data-Centric)
1. Go to the app **Settings** (gear icon) > **References** tab.
2. Grant SELECT access on your orders/demand data table (`consumer_orders_table` reference).
3. Return to the **Historical Data** tab to preview and compare against forecasts.

## Required Table Schema (Optional — for Historical Data tab)

| Column | Type | Description |
|--------|------|-------------|
| ORDER_DATE | DATE | Date of the order |
| STATE | VARCHAR | US state name |
| DEMAND | NUMBER | Demand quantity or order count |

## Features

- Pre-trained Prophet models for 5 US states
- Forecast at daily, weekly, monthly, or yearly frequency
- Interactive Plotly line charts
- Optional consumer data integration via References
- No external dependencies — runs entirely within Snowflake

## Requirements

- A warehouse for running the Streamlit app
