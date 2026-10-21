# Pairs Trading: does cointegration hold up out of sample?

Tests whether cointegration-based pairs trading survives proper validation, using daily prices (Yahoo Finance, 2015-2024) of 20 US large caps in four sectors.

## What I did
1. Full-sample Engle-Granger test on MCD/YUM (p = 0.0129)
2. Formation (2015-2019) / trading (2020-2024) split with frozen parameters
3. Rolling-beta diagnostic (beta drifts between about 0.2 and 0.65 from 2018 onward)
4. Batch screening of 40 within-sector pairs
5. Walk-forward backtest (2-year estimation, 1-year trading, rules fixed in advance)

## Main findings
- A significant full-sample p-value (0.0129) did not hold out of sample.
- All six pairs passing the formation screen (p < 0.05) failed out of sample.
- Walk-forward gross return 2017-2024: about -0.29% (before costs).

## Limitations
Small hand-picked pool, two-year estimation window, results gross of costs, no multiple-testing correction.
