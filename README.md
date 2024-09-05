Discounted Cash Flow (DCF) Model
Overview
This script performs a discounted cash flow (DCF) analysis to estimate the intrinsic value of a stock. It uses historical financial data from Yahoo Finance (yfinance) to calculate future cash flows, Weighted Average Cost of Capital (WACC), and other essential metrics.

Requirements
You'll need the following Python libraries:

pandas
numpy
yfinance

Usage
Input the stock symbol: Provide the ticker symbol of the stock (e.g., aapl).
Forecasting period: Input the number of years for forecasting future cash flows.
Perpetuity growth rate: Provide the expected perpetuity percentage (e.g., 0.02 for 2%).

Steps:
Data Fetching: The script retrieves the stock’s cash flow, shares outstanding, balance sheet, and income statement data.
Cash Flow Growth Calculation: Determines the average change in cash flows over the past 5 years, then adjusts for bearish, normal, and bullish scenarios.
Cost of Equity: Calculates the cost of equity using the stock’s beta and risk-free rate.
WACC Calculation: Computes the Weighted Average Cost of Capital based on the company’s debt and equity.
Future Cash Flow Projection: Forecasts future cash flows for each scenario (bearish, normal, bullish).
Discounted Cash Flow: Applies WACC to calculate the present value of future cash flows, including a terminal value based on the perpetuity growth rate.
Intrinsic Value Calculation: Divides the total discounted cash flows by the number of shares outstanding to estimate the intrinsic stock value.

Outputs:
Intrinsic Stock Values: Estimated prices for bearish, normal, and bullish scenarios.
