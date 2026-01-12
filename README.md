# Investment Calculators Documentation and Methodology

This repository provides documentation and methodology notes for a public website that hosts multiple finance calculators. It explains what each calculator does, which inputs are used, how results are interpreted, and which assumptions apply. The production codebase that runs the live site is private and is not reproduced here.

This repository exists to document calculator behavior and assumptions in a stable, citable format for reference and review.

Live site: https://investment-calculator.net

## Calculators available

1. Investment Calculator (projection, goal, S&P 500 backtest): Models long term investment growth with recurring contributions. It supports forward projections using an assumed return, goal based planning, and historical backtests using S&P 500 monthly price data.
2. Compound Interest Calculator: Projects future value from an initial amount, an expected annual return, and optional recurring contributions, with a breakdown of contributions versus growth.
3. Dollar Cost Averaging Calculator: Simulates fixed recurring investments over time and shows how total contributions and investment growth accumulate.
4. Savings Calculator: Projects savings balance growth using an interest rate, recurring deposits, optional yearly contribution increases, and optional extra interest applied on a chosen cadence.
5. Crypto Investment Calculator: Backtests recurring investment plans for selected cryptocurrencies using historical monthly prices, with an optional assumed return applied beyond the last available data year.
6. Inflation Calculator: Compares purchasing power between two dates using official CPI series such as US CPI from BLS or UK CPI from ONS, showing inflation adjusted values and average annual rates.
7. Investment Income Calculator: Computes expected income from a yield and investment amount, or the required investment amount needed to reach a target income at a given yield.
8. ROI Calculator: Calculates gain or loss, total ROI, and annualized ROI using either start and end dates or a fixed holding period.
9. Loan Calculator: Estimates periodic loan payments and total cost based on loan amount, interest rate, and term, with an amortization style payoff breakdown.
10. VAT Calculator: Adds or removes VAT from an amount, supporting quantities and custom tax rates, and returning net, tax, and gross values.
11. Discount Calculator: Computes final price and savings for percentage discounts, fixed amount discounts, and buy X get Y free offers.
12. Age Calculator: Calculates exact age between two dates and presents multiple representations such as years and months, total days, and time until the next birthday.

## How calculations are interpreted

Projection calculators show outcomes assuming that inputs remain constant over time. Annual return or interest rates are converted to monthly equivalents for month by month compounding.

Backtests replay the same contribution schedule over historical monthly price movements. Results illustrate volatility and path dependence but are not predictions and do not represent guaranteed outcomes.

Fees are shown separately when applicable. Transaction costs are treated as costs paid alongside contributions rather than amounts invested. Ongoing fees are modeled as an expense ratio applied to the balance.

ROI outputs distinguish between total ROI and annualized ROI, where annualized ROI represents the constant yearly rate that would produce the same start to end change over the selected period.

Inflation results compare values using CPI index levels between the chosen dates and answer how purchasing power differs across time rather than tracking the price of a specific product.

## Method notes

Investment and compound projections use monthly compounding. Contribution frequencies are translated into monthly equivalents. Contribution increases are applied on a yearly schedule.

S&P 500 and crypto backtests use consecutive monthly closing prices. The S&P 500 backtest is based on index price data and does not represent a dividend reinvested total return series. When a selected end date exceeds the available historical data, an assumed return may be applied for subsequent months.

Inflation calculations are limited to the historical range of the selected CPI series and do not extrapolate beyond available data.

Currency selection affects display and formatting only. Calculations use numeric inputs as provided and do not perform foreign exchange conversion.

## Disclaimer

These calculators are educational tools and do not provide financial, investment, tax, or legal advice. Results depend on user inputs and simplifying assumptions and may omit real world factors such as taxes, spreads, dividends, changing rates, or fees. Outputs should be validated independently and discussed with qualified professionals where appropriate.

## Contact or contributions

If you identify a methodology issue, unclear documentation, or calculator behavior that should be explained more precisely, please open an issue or pull request in this repository. For questions related to the live website, use the email info@investment-calculator.net.
