# ETF price snapshots

Downloaded on 2026-10-25 using `yfinance==1.7.0`, with `interval="1d"` and `auto_adjust=True`. Values are Yahoo Finance adjusted `Close` prices in USD, including historical split/distribution adjustments. Provider revisions can change a later download.

| File | Symbols | Requested dates, inclusive | Rows |
| --- | --- | --- | ---: |
| `etf_ccf_2025-01-01_2026-09-30.csv` | XLK, XLV, SMH, SOXX, FXE, XLY | 2025-01-01 through 2026-09-30 | 437 |
| `etf_models_2020-01-01_2026-09-30.csv` | SPY, IVV, VOO, GLD, TLT | 2020-01-01 through 2026-09-30 | 1695 |

The first trading dates are January 2, 2025 and January 2, 2020 respectively. The download uses the exclusive end argument `2026-10-01`. All requested symbols have complete observations on the shared dates. Weekends and exchange holidays are not filled or interpolated. The snapshots allow the notebook to run without a network connection; it downloads through yfinance only when the corresponding snapshot is absent.

API reference: [yfinance.download](https://ranaroussi.github.io/yfinance/reference/api/yfinance.download.html).
