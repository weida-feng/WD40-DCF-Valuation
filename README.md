# WD-40: Financial Statement Analysis and DCF Valuation

**Self-directed learning project · 2026**  
**Historical valuation date:** 27 October 2025, incorporating the FY2025 10-K filed after the market close  
**Report prepared:** 26 October 2026  
**Units:** USD millions unless stated otherwise

[Open the editable Excel model](WD40_DCF_Portfolio.xlsx) · [Modeling process and calculation walkthrough](MODELING_PROCESS.md) · [Reverse DCF comparison](REVERSE_DCF.md)

## Executive assessment

WD-40's FY2025 reported earnings grew faster than its cash generation. Net income increased **30.7%**, while cash from operations declined **4.5%**. A one-off tax benefit and changes in operating assets and liabilities help explain this divergence. Understanding those drivers is the starting point for the valuation, rather than extrapolating reported net income directly into future cash flow.

The five-year FCFF model produces a base equity value of **$121.50 per share**, using an **8.13% WACC**, **2.5% terminal growth**, and annual year-end discount periods of one to five years. Terminal value contributes **78.1%** of enterprise value. The result is therefore highly dependent on assumptions beyond the explicit forecast period.

The modeled value is **37.8% below** the historical reference close of **$195.38** on 27 October 2025. That difference identifies a gap between the model's assumptions and the reference market valuation; it does not by itself establish mispricing. The reference close also predates the after-close 10-K filing used in this study. [S2], [S4]

## 1. Scope and information set

This project connects financial-statement analysis to a transparent operating forecast and an enterprise-to-equity valuation. WD-40 provides a manageable case because maintenance products account for approximately **95.3%** of FY2025 revenue and production is substantially outsourced. Product concentration and international exposure remain relevant operating risks. [S1]

The financial model starts from FY2025 disclosures. FY2026 actual results are not used as numerical inputs. The FY2026 guidance cited here was published in October 2025 and was available by the historical source cutoff. [S5]

**Study design:** this retrospective valuation was prepared in 2026. Assumptions were finalized with access to subsequent outcomes, so hindsight bias cannot be excluded. FY2026 actual results are not numerical model inputs. The results should be evaluated as a historical scenario valuation, without treating them as evidence of predictive performance.

| Item | Convention |
| --- | --- |
| Historical financial statements | FY2023–FY2025; fiscal years end 31 August |
| Forecast | FY2026–FY2030 |
| Historical-source cutoff for model inputs | FY2025 10-K accepted on 27 October 2025 at 16:12:49 |
| Cash and debt | 31 August 2025 reported balances, retained as valuation-date proxies |
| Shares | 13.527835m as of 21 October 2025, rounded to 13.528m |
| Reference share price | 27 October 2025 regular-session close of $195.38 |
| Main discount convention | Complete annual periods of 1–5 years |

The filing was accepted after the regular trading session. This is a historical filing-date study with explicit timing simplifications, rather than an intraday trading backtest. [S1], [S2], [S4]

## 2. Financial-statement findings

### Profit growth did not translate into higher operating cash flow

| USD millions, except ratios | FY2023 | FY2024 | FY2025 |
| --- | ---: | ---: | ---: |
| Revenue | 537.255 | 590.557 | 619.985 |
| EBIT | 89.724 | 96.351 | 103.793 |
| Gross margin | 51.0% | 53.4% | 55.1% |
| EBIT margin | 16.7% | 16.3% | 16.7% |
| Net income | 65.993 | 69.644 | 90.994 |
| Cash from operations | 98.391 | 92.034 | 87.925 |
| Cash PP&E purchases | 6.871 | 4.206 | 4.528 |
| CFO less cash PP&E purchases | 91.520 | 87.828 | 83.397 |

*Source: reported figures in the FY2025 10-K; margins and CFO less PP&E purchases are calculated in the workbook. [S1]*

FY2025 net income includes a **$11.929m favorable tax release**. The cash-flow statement reverses that benefit when reconciling net income to operating cash flow. For forecasting, the model therefore uses a **23.9% normalized tax assumption**, approximately the FY2024 effective rate, rather than extrapolating FY2025's roughly 10.5% reported tax rate. [S1]

The cash-flow reconciliation makes the main drivers visible:

| USD millions | FY2024 | FY2025 | Change |
| --- | ---: | ---: | ---: |
| Net income | 69.644 | 90.994 | 21.350 |
| Total noncash adjustments | 17.765 | 7.438 | (10.327) |
| Operating asset / liability cash adjustments | 4.625 | (10.507) | (15.132) |
| Cash from operations | 92.034 | 87.925 | (4.109) |

Although net income rose by **$21.350m**, the combined deterioration in noncash adjustments and operating asset / liability cash adjustments more than offset that increase. The tax release explains part of the noncash comparison; inventory and other-asset cash outflows also contributed to weaker cash generation. [S1]

**CFO less PP&E purchases is a useful cash-generation measure, but it is not the unlevered FCFF used in the DCF.** The forecast is built from EBIT, normalized operating taxes, capital investment and operating NWC instead.

### Gross-margin gains were partly absorbed by operating expenses

Gross margin increased from **53.4% to 55.1%** between FY2024 and FY2025, while EBIT margin increased only from **16.3% to 16.7%**. This limits the case for mechanically passing future gross-margin improvements through to operating profit. [S1]

The forecast assumes modest operating leverage: systems investment and market-entry costs can be spread over a larger revenue base, while payroll, marketing, compliance and ongoing support costs continue.

### Operating NWC depends on classification

The model estimates operating NWC as receivables, inventory and adjusted other current assets, less payables, adjusted accrued liabilities and accrued payroll. It excludes cash, financing debt, income tax balances, held-for-sale assets and current operating lease liabilities. Remaining other current assets are treated as operating for this estimate. [S1]

| Adjusted operating NWC estimate | FY2024 | FY2025 |
| --- | ---: | ---: |
| Adjusted other current assets | 11.661 | 14.176 |
| Adjusted accrued liabilities | 28.978 | 31.948 |
| Operating NWC | 117.249 | 116.318 |
| Operating NWC / revenue | 19.9% | 18.8% |

The estimated balance decreased by **$0.931m**. This balance-sheet change is distinct from the cash-flow statement's operating asset / liability adjustments: exchange-rate movements, asset reclassifications and other noncash effects can make the two differ. Tax receivables used in this estimate are approximate disclosures. [S1]

The DCF retains **$116.318m as opening FY2026 NWC**. Applying the forecast 18.8% ratio retroactively to FY2025 revenue would change that opening balance and the first forecast year's FCFF. The workbook preserves the historical estimate and applies the forecast ratio prospectively.

## 3. Forecast assumptions and rationale

These are analyst assumptions, not company guidance.

| Driver | Base assumption | Rationale |
| --- | --- | --- |
| Revenue growth | 5.0% in FY2026; 5.5% thereafter | Focus on core maintenance-product volumes, distribution and market expansion. |
| EBIT margin | 16.9% → 17.2% → 17.5% → 17.8% → 18.0% | Gradual operating leverage while continuing operating costs remain. |
| Normalized tax | 23.9% | Avoid perpetuating the unusual FY2025 tax benefit. |
| D&A / revenue | 1.6% | Includes cloud implementation amortization; close to FY2025 historical intensity. |
| PP&E investment / revenue | 0.8% | Moderate physical investment for an outsourced production model. |
| Other capitalized investment / revenue | 0.4% | A normalized cloud / systems estimate, not a disclosed historical spending ratio. |
| Total capital investment / revenue | 1.2% | PP&E investment plus other capitalized investment, separate from NWC. |
| Closing operating NWC / revenue | 18.8% | Approximate recent operating-capital intensity; opening NWC remains $116.318m. |
| Terminal growth | 2.5% | A provisional moderate nominal USD perpetuity assumption. |

The FY2025 disclosures record a completed UK cleaning-business sale and an Americas disposal plan. Their associated FY2025 sales represented approximately **1.0%** and **2.2%** of group revenue, respectively. That scale supports treating divestitures as a secondary forecast consideration. The **5.0% / 5.5% path represents modeled consolidated revenue growth**; divested sales are not deducted separately. This basis differs from the company's divestiture-adjusted pro forma guidance. [S1], [S5]

Capital investment of 1.2% is **not solely PP&E capex**. The additional 0.4% captures estimated other capitalized investment because the D&A add-back includes cloud amortization. Forecast operating NWC is treated as excluding that separately modeled cloud investment, avoiding a second deduction for the same forecast spending. This separation is an assumption; cloud-related amounts within historical residual other current assets have not been fully isolated.

## 4. Five-year FCFF forecast

The operating model uses:

$$
FCFF_t = EBIT_t(1-T_t) + D\&A_t - \text{Capital investment}_t - \Delta ONWC_t
$$

| USD millions, except rates | FY2026E | FY2027E | FY2028E | FY2029E | FY2030E |
| --- | ---: | ---: | ---: | ---: | ---: |
| Revenue growth | 5.0% | 5.5% | 5.5% | 5.5% | 5.5% |
| Revenue | 650.984 | 686.788 | 724.562 | 764.413 | 806.455 |
| EBIT margin | 16.9% | 17.2% | 17.5% | 17.8% | 18.0% |
| EBIT | 110.016 | 118.128 | 126.798 | 136.065 | 145.162 |
| NOPAT | 83.722 | 89.895 | 96.494 | 103.546 | 110.468 |
| Add: D&A | 10.416 | 10.989 | 11.593 | 12.231 | 12.903 |
| Less: capital investment | (7.812) | (8.241) | (8.695) | (9.173) | (9.677) |
| Closing operating NWC | 122.385 | 129.116 | 136.218 | 143.710 | 151.614 |
| Less: increase in operating NWC | (6.067) | (6.731) | (7.101) | (7.492) | (7.904) |
| **FCFF** | **80.259** | **85.911** | **92.290** | **99.111** | **105.790** |

*Parentheses indicate cash outflows. Figures are calculated using unrounded inputs and displayed to three decimals.*

For FY2026, closing NWC is **$122.385m**, compared with opening NWC of **$116.318m**. The **$6.067m** incremental investment reduces FCFF to **$80.259m**, despite higher operating profit. This illustrates why cash available to capital providers should be forecast separately from earnings growth.

Financing debt and operating liabilities are treated separately. Payables already influence NWC and are not deducted again as financing debt in the enterprise-to-equity bridge.

## 5. Provisional WACC

The reference calculation uses CAPM and market-value capital weights:

$$
R_e = R_f + \beta ERP
$$

$$
WACC = w_e R_e + w_d R_d(1-T)
$$

| Parameter | Value | Basis |
| --- | ---: | --- |
| USD risk-free-rate proxy | 4.01% | 10-year Treasury par yield on 27 October 2025. [S3] |
| Beta | 0.85 | Provisional scenario assumption; no historical regression has been completed. |
| Equity risk premium | 5.00% | Assumption. |
| Cost of equity | 8.26% | CAPM calculation. |
| Pretax cost of debt | 5.00% | Estimated marginal borrowing cost, not a historical coupon average. |
| Tax rate | 23.90% | Normalized modeling assumption. |
| Equity market value | $2,643.101m | Reference close × rounded shares. |
| Debt market value | $82.200m | Rounded FY2025 fair-value estimate. [S1] |
| Equity / debt weights | 96.98% / 3.02% | Market-value weights. |
| Component-derived WACC | 8.1256% | Unrounded reference calculation. |
| **Active DCF WACC** | **8.13%** | Adopted rounded base input. |

The workbook keeps the active WACC editable in **Sensitivity Analysis!F6**. Its lower reference build explains the components; changing beta, ERP or debt-cost assumptions does not automatically overwrite F6. A revised adopted WACC must be entered there explicitly.

The next empirical improvement is to estimate beta using returns available through the valuation date and assess its sensitivity to the benchmark, return frequency and lookback window.

## 6. DCF valuation

The base model discounts FY2026–FY2030 FCFF at annual year-end periods and uses Gordon growth for the terminal value:

$$
TV_{2030}=\frac{FCFF_{2030}(1+g)}{WACC-g}
$$

$$
EV=\sum_{t=1}^{5}\frac{FCFF_t}{(1+WACC)^t}+\frac{TV_{2030}}{(1+WACC)^5}
$$

| Base valuation | USD millions, except per share |
| --- | ---: |
| PV of FY2026–FY2030 FCFF | 364.769 |
| Terminal enterprise value at FY2030 year-end | 1,926.018 |
| PV of terminal value | 1,302.955 |
| Enterprise value | 1,667.724 |
| Add: cash | 58.130 |
| Less: debt market value | (82.200) |
| Equity value | 1,643.654 |
| Shares outstanding (millions) | 13.528 |
| **Equity value per share** | **$121.50** |

Debt is estimated from **$61.2m** of senior-note fair value plus **$20.995m** of revolver borrowings, rounded to **$82.2m**. Cash and debt retain their FY2025 balance dates. The bridge uses 13.528m shares, rounding the 21 October count, rather than diluted weighted-average shares used for EPS. [S1]

### Discount-timing comparison

| Convention | FY2026 discount period | Equity value per share |
| --- | ---: | ---: |
| Annual base | 1.0000 years | **$121.50** |
| Actual/365 timing comparison | 308 / 365 = 0.8438 years | **$122.99** |

The second calculation discounts to the stated 27 October date using actual day counts. It changes **timing only**: complete fiscal-year FCFF and the same balance-sheet proxies are retained. It does not remove cash flows attributable to the elapsed part of FY2026 or construct an interim balance sheet. It is therefore a timing comparison, not a fully rolled-forward valuation.

## 7. Sensitivity and interpretation

### WACC × terminal growth

The following excerpt comes from the workbook's native two-variable Data Table. Values are USD per share; bold marks the base case.

| WACC / terminal g | 1.50% | 2.00% | 2.50% | 3.00% | 3.50% |
| --- | ---: | ---: | ---: | ---: | ---: |
| 7.13% | $125.86 | $136.13 | $148.63 | $164.16 | $183.96 |
| 7.63% | $115.21 | $123.65 | $133.74 | $146.01 | $161.25 |
| 8.13% | $106.17 | $113.21 | **$121.50** | $131.40 | $143.45 |
| 8.63% | $98.41 | $104.35 | $111.26 | $119.40 | $129.12 |
| 9.13% | $91.67 | $96.73 | $102.57 | $109.35 | $117.34 |

Holding terminal growth at 2.5%, changing WACC from **7.13% to 9.13%** moves value from **$148.63 to $102.57**. The approximately **78.1%** terminal-value share of EV makes capital-cost and long-run growth assumptions central to the result.

### Revenue growth × EBIT margin

Rows apply parallel percentage-point shifts to every forecast revenue-growth assumption. Columns shift every forecast EBIT margin. WACC remains 8.13% and terminal growth remains 2.5%.

| Revenue-growth shift / EBIT-margin shift | -1.0 pp | -0.5 pp | 0.0 pp | +0.5 pp | +1.0 pp |
| --- | ---: | ---: | ---: | ---: | ---: |
| -1.0 pp | $110.91 | $114.36 | $117.81 | $121.26 | $124.70 |
| -0.5 pp | $112.60 | $116.12 | $119.64 | $123.17 | $126.69 |
| 0.0 pp | $114.30 | $117.90 | **$121.50** | $125.10 | $128.70 |
| +0.5 pp | $116.02 | $119.70 | $123.38 | $127.06 | $130.73 |
| +1.0 pp | $117.76 | $121.52 | $125.28 | $129.03 | $132.79 |

For example, a +1.0 pp revenue-growth shift changes FY2026 growth from 5.0% to 6.0% and later growth from 5.5% to 6.5%. A +1.0 pp margin shift raises the FY2030 EBIT margin from 18.0% to 19.0%. Together, these changes produce **$132.79 per share**.

Within this operating test range, value remains below the reference close. A higher market valuation could reflect stronger operating expectations, different reinvestment economics, lower required returns or a combination of these. The selected grids describe assumption sensitivity, not probabilities assigned to future prices.

### Market-implied expectations and reverse DCF

The $195.38 reference price corresponds to equity value of **$2,643.101m** and required enterprise value of **$2,667.171m** using the same shares, cash and market debt. Reversing the annual-base DCF shows how much a selected input must change to reproduce that price:

| Conditional experiment | Adopted base | Price-matching input | Assumptions held fixed |
| --- | --- | --- | --- |
| Solve WACC | 8.13% | **6.0456%**, approximately **6.05%** | All five FCFF amounts and terminal g of 2.5%. |
| Map that WACC into CAPM beta | Provisional beta 0.85 | **0.421** | Risk-free rate, ERP, debt cost, tax and reference-price market weights. |
| Solve terminal FCFF growth | 2.50% | **4.8702%** | WACC of 8.13% and explicit five-year FCFF. |
| Shift all five EBIT margins | No shift; FY2030 margin 18.0% | **+10.2605 pp**; FY2030 margin **28.2605%** | Revenue, tax, investment, NWC, WACC and terminal g. |

These are separate conditional matches; the beta row translates the solved WACC rather than adding another independent requirement. One price cannot identify investors' actual assumptions. In particular, **0.421 is not an estimated historical beta**, and a lower empirical beta must be established from return data rather than selected to reproduce the price.

The capital-cost result supports making beta estimation the next research priority. The operating and terminal-growth alternatives require materially stronger assumptions and do not resolve the model's terminal-reinvestment limitation. Solving the price equation establishes numerical consistency, not economic plausibility or market mispricing.

The [reverse DCF comparison](REVERSE_DCF.md) explains the equations, beta scenarios and interpretation. The **Reverse DCF** worksheet links to the active forecast and shows a 36-step WACC bisection trail. It preserves full precision: entering exactly 6.05% yields about $195.13, while the unrounded root reproduces $195.38. The adopted 8.13% base case is unchanged.

## 8. Material limitations

- **Terminal reinvestment:** extending FY2030 FCFF at 2.5% does not demonstrate sufficient steady-state investment. Capital investment remains below D&A in the explicit forecast; terminal growth has not been reconciled with an independently justified ROIC and reinvestment rate.
- **Provisional capital costs:** beta, ERP and marginal debt cost are assumptions. The 8.13% result should be interpreted as a scenario input rather than a statistically established required return.
- **Operating-capital estimates:** the NWC definition uses approximate tax receivables and limited detail within other current assets. Forecasting a fixed sales ratio is a simplification.
- **Date alignment:** the main DCF retains complete annual periods. Historical cash / debt proxies, an October share count and a pre-filing reference close do not constitute a fully synchronized market snapshot.
- **Equity and lease treatment:** all cash is treated as excess; no minimum operating-cash balance is deducted. Stock compensation remains in EBIT without an add-back, but future share issuance, award dilution and repurchases are not separately forecast. Operating leases remain in operating costs and are not deducted again as debt.
- **Business aggregation:** the forecast does not separately model FX, individual products, acquisitions or divestiture timing.
- **Retrospective design:** assumptions were finalized after subsequent outcomes became available. Excluding later actuals from numerical inputs does not remove potential hindsight bias. The study does not establish a forecasting record made in 2025.

## 9. Using and reproducing the model

The [Excel workbook](WD40_DCF_Portfolio.xlsx) is the calculation source. This report is a static snapshot of its base case as prepared on 26 October 2026.

| Worksheet | Role |
| --- | --- |
| Analysis Overview | Financial findings, assumptions and valuation interpretation. |
| DCF Model | Operating forecast, FCFF, discounting, equity bridge and timing comparison. |
| Sensitivity Analysis | Active valuation controls, two native sensitivity tables and WACC reference calculation. |
| Reverse DCF | Conditional WACC, CAPM-beta, terminal-growth and margin matches to the reference price. |
| Historical Financials | Source financials, adjusted NWC, CFO reconciliation and historical FCFF-method comparison. |
| Checks | Source tie-outs, bridges, sensitivity centers and base-case reconciliation. |
| Sources and Notes | Input provenance, dates, methods and limitations. |

Edit the blue numbers in amber cells, then use Excel Automatic calculation including Data Tables and recalculate. Historical source inputs also use blue text but should be changed only when updating the underlying data. The report's tables must be refreshed if the adopted workbook assumptions change.

Forecasts, valuation bridges, timing calculations, representative non-base sensitivities and reverse price matches were checked against independent numerical calculations. The historical FCFF accounting bridge was also reconciled. Exported formulas, native Data Table definitions and recalculation after reopening were checked. Testing inside the native Excel application has not been completed.

## Project Purpose and AI Assistance

This project documents my self-directed learning in financial statement analysis and discounted cash flow valuation, using WD-40 as a practical case study. My objective was to understand the full process: interpreting financial statements, explaining cash-flow drivers, developing forecast assumptions, and assessing valuation uncertainty.

I worked through key calculations, questioned proposed assumptions, and made the final modeling choices. The accompanying modeling-process document records important calculations, changes in judgment, and the reasoning behind the adopted assumptions.

GPT supported the learning process through explanations, public-source research, analytical suggestions, calculation cross-checks, Excel implementation, and documentation assistance. Some approaches and assumptions were developed collaboratively.

This is a retrospective educational case study. I am responsible for the adopted modeling choices and interpretation; sources, provisional assumptions, and methodological limitations are documented throughout the project.

## Sources

- **S1 — [WD-40 FY2025 Form 10-K](https://www.sec.gov/Archives/edgar/data/105132/000010513225000067/wdfc-20250831.htm).** Statements F-3, F-4 and F-7; cover-page shares; business and revenue disclosures; notes on tax, leases, capitalized cloud costs and debt fair value. Monetary source data are generally USD thousands and are converted to millions in the workbook.
- **S2 — [SEC filing index and acceptance timestamp](https://www.sec.gov/Archives/edgar/data/105132/000010513225000067/0000105132-25-000067-index.html).** Filed 27 October 2025; accepted 16:12:49.
- **S3 — [US Treasury daily par yield curve, October 2025](https://home.treasury.gov/resource-center/data-chart-center/interest-rates/TextView?field_tdr_date_value_month=202510&type=daily_treasury_yield_curve).** 27 October observation, 10-year column.
- **S4 — [ChartExchange WDFC historical prices](https://chartexchange.com/symbol/nasdaq-wdfc/historical/).** 27 October 2025 regular-session close.
- **S5 — [WD-40 FY2025 earnings release](https://investor.wd40company.com/news/news-details/2025/WD-40-Company-Reports-Fourth-Quarter-and-Fiscal-Year-2025-Financial-Results/default.aspx).** Released 22 October 2025. Company FY2026 guidance used a divestiture-adjusted pro forma basis and a 22.5%–23.5% tax range; this study's consolidated starting point and 23.9% tax assumption differ from that basis.

Public disclosures support the historical facts. Forecast growth, margins, normalized capital investment, NWC intensity, beta, ERP, debt cost and terminal growth are explicitly identified analyst assumptions.

[S1]: https://www.sec.gov/Archives/edgar/data/105132/000010513225000067/wdfc-20250831.htm
[S2]: https://www.sec.gov/Archives/edgar/data/105132/000010513225000067/0000105132-25-000067-index.html
[S3]: https://home.treasury.gov/resource-center/data-chart-center/interest-rates/TextView?field_tdr_date_value_month=202510&type=daily_treasury_yield_curve
[S4]: https://chartexchange.com/symbol/nasdaq-wdfc/historical/
[S5]: https://investor.wd40company.com/news/news-details/2025/WD-40-Company-Reports-Fourth-Quarter-and-Fiscal-Year-2025-Financial-Results/default.aspx
