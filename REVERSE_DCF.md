# WD-40: Reverse DCF and Market-Price Expectations

**Independent study · 2026**  
**Historical valuation date:** 27 October 2025  
**Prepared:** 26 October 2026  
**Units:** USD millions, except per-share values and percentages

[Project report](README.md) · [Modeling process](MODELING_PROCESS.md) · [Editable Excel workbook](WD40_DCF_Portfolio.xlsx)

## What would support the reference price?

The annual base DCF values WD-40 at **$121.50 per share**, compared with the historical reference close of **$195.38**. A reverse DCF asks which assumptions would reconcile that difference within the model. It does not assume that the market price is correct or that the model's base assumptions are wrong.

The analysis below changes one driver at a time. The five-year operating forecast, enterprise-to-equity bridge and complete annual discount periods remain the starting point. The adopted **8.13% WACC and $121.50 base valuation remain unchanged** in the workbook; reverse calculations sit alongside them.

| Conditional experiment | Result needed to reach $195.38 | What remains fixed |
| --- | ---: | --- |
| Solve for WACC | **6.045566%** | Forecast FCFF; terminal growth 2.5%; cash, debt and shares |
| Translate that WACC into CAPM beta | **0.42105** | Risk-free rate, ERP, debt cost, tax and market capital weights |
| Solve for terminal FCFF growth | **4.87024%** | WACC 8.13%; explicit forecast FCFF; equity bridge |
| Shift every forecast EBIT margin | **+10.26048 percentage points** | Revenue path; other operating ratios; WACC 8.13%; terminal growth 2.5% |

These are **separate conditional solutions**. They are not jointly required, and combinations of smaller changes could also reproduce the same price. One observed price cannot uniquely identify growth, profitability and required returns.

## 1. Translate the price into a target enterprise value

The reference price and the adopted 13.528 million shares imply:

$$
Equity_{target}=195.38\times13.528=2{,}643.100640
$$

The model adds all cash and subtracts market debt when moving from enterprise value to equity value. Reversing that bridge gives:

$$
EV_{target}=Equity_{target}-Cash+Debt
$$

$$
=2{,}643.100640-58.130+82.200
=\boxed{2{,}667.170640}
$$

This target EV is compared with the base EV of **$1,667.724m**. Payables and other operating liabilities are already reflected in operating NWC; they are not deducted again as financing debt. Cash and debt retain their FY2025 balance dates, and shares remain the rounded October outstanding count.

## 2. Solve for the discount rate

Keep the full-precision FY2026–FY2030 FCFF forecasts, displayed as **80.259 / 85.911 / 92.290 / 99.111 / 105.790m**, and terminal growth of 2.5%. For a candidate discount rate $w$:

$$
P(w)=\frac{\displaystyle\sum_{t=1}^{5}\frac{FCFF_t}{(1+w)^t}
+\frac{FCFF_5(1+g)}{(w-g)(1+w)^5}+Cash-Debt}{Shares}
$$

Solving $P(w)=195.38$, with $w>g$, gives **6.0455664582%**. This is approximately **2.08 percentage points below** the adopted 8.13% base WACC.

| Candidate WACC | Value per share |
| --- | ---: |
| 6.04% | $195.69 |
| **6.0455664582%** | **$195.38** |
| 6.05% | $195.13 |
| 6.10% | $192.36 |

“Approximately 6.05%” is therefore an appropriate description. Entering exactly 6.05% does not reproduce the target exactly: it gives **$195.13**. The calculation retains more precision than the display.

For these positive cash flows and a positive WACC-minus-growth spread, a higher WACC reduces value. The prices on either side of the root provide a useful independent check on the numerical solution.

## 3. What beta corresponds to that WACC?

CAPM and market-value weights translate the solved WACC into a **conditional scenario beta**. The unchanged component assumptions are:

| Component | Value |
| --- | ---: |
| USD risk-free-rate proxy | 4.01% |
| Equity risk premium | 5.00% |
| Pretax marginal debt cost | 5.00% |
| Normalized tax rate | 23.90% |
| Equity / debt weights | 96.983819% / 3.016181% |

The weights use reference-price equity of $2,643.100640m and debt of $82.200m. They remain fixed throughout this experiment.

Rearrange the WACC formula to find the equity return consistent with the target:

$$
R_e^*=\frac{WACC^*-w_dR_d(1-T)}{w_e}=6.11524771\%
$$

Then rearrange CAPM:

$$
\beta^*=\frac{R_e^*-R_f}{ERP}
=\frac{6.11524771\%-4.01\%}{5.00\%}
=\boxed{0.42104954}
$$

This is not an empirical estimate of WD-40's beta, a uniquely inferred market belief, or its “true” beta. It is the beta corresponding to one target WACC under the stated risk-free rate, ERP, debt cost, tax and weights.

The following scenarios illustrate why empirical beta research is a useful next step. WACC is calculated at full precision before valuing the cash flows:

| Scenario beta | Component-derived WACC | Value per share |
| --- | ---: | ---: |
| 0.40 | 5.943493% | $201.30 |
| 0.50 | 6.428412% | $175.93 |
| 0.60 | 6.913331% | $156.13 |
| 0.70 | 7.398250% | $140.26 |
| 0.85 | 8.125629% | $121.60 |

The final row differs slightly from the **$121.50 active base**, which deliberately uses the rounded adopted **8.13%**. The table uses unrounded component-derived rates and does not overwrite that adopted input.

A subsequent beta study should use returns available through the historical valuation date, document its benchmark, frequency and lookback window, and test the estimate's stability. Stable business revenue alone does not establish a low equity beta.

## 4. Alternative operating and terminal expectations

### Terminal FCFF growth at an unchanged 8.13% WACC

Explicit forecast cash flows have a present value of **$364.769260m**. To reach target EV, the required terminal value at FY2030 year-end is:

$$
TV_{required}=(2{,}667.170640-364.769260)\times1.0813^5
=3{,}403.392612
$$

Let $F=FCFF_{2030}$. Rearranging $TV=F(1+g)/(w-g)$:

$$
g^*=\frac{TV_{required}w-F}{TV_{required}+F}
=\boxed{4.87024443\%}
$$

This is perpetual **FCFF growth**, not an explicit revenue-growth forecast. At g of 4.8% and 4.9%, modeled values are $191.68 and $197.00 respectively, bracketing the target.

A perpetual nominal USD growth assumption near 4.87% is materially stronger than the 2.5% base. The model does not independently establish that steady-state reinvestment could support it. Capital investment remains below D&A in the explicit forecast, and no independently justified terminal ROIC has been used to reconcile growth and reinvestment. Solving for a price does not resolve that limitation.

### Parallel change in five-year EBIT margins

Keep revenue growth and all other operating ratios fixed, but add the same decimal margin increment $dM$ in every forecast year. A 1.0 percentage-point increase means $dM=0.01$:

$$
FCFF_t(dM)=FCFF_t(0)+Revenue_t(1-T)dM
$$

A one-percentage-point margin increase adds approximately **$7.20 per share** under these fixed assumptions. The target requires **+10.26048 percentage points**, taking the margin path from 16.9%–18.0% to approximately **27.16048%–28.26048%**. This changes every forecast year and the terminal cash-flow anchor; it is not a FY2030-only margin solve.

That is a large operating improvement. Holding investment, working-capital intensity and revenue unchanged makes it a controlled stress scenario, not evidence that such profitability is attainable. It helps communicate how demanding a margin-only explanation would be within this model.

## 5. Workbook calculation trail and interpretation

The workbook's **Reverse DCF** sheet links to the existing forecast and shows a visible **36-step bisection** for WACC, plus exact algebraic terminal-growth and parallel-margin calculations. The target-price cell **F5** links to **Sensitivity Analysis!F58**. Results appear in:

| Cell | Result |
| --- | --- |
| G13 | Solved WACC |
| G14 | Conditional CAPM beta |
| G15 | Solved terminal FCFF growth |
| G16 | Parallel five-year EBIT-margin shift |
| G17 | Resulting FY2030 EBIT margin |

These calculations do not overwrite the base assumptions. Recalculate the workbook after changing linked inputs and check that each solved scenario returns the target price. Preserve the condition **WACC > terminal growth** and distinguish percentage-point shifts from percentage multipliers.

The practical finding is a sensitivity of expectations: a lower required return, much stronger terminal growth, or substantial profitability improvement could each close the gap under separate conditions. None is uniquely identified by the market price. The base model's approximately **78.1% terminal-value share of EV** reinforces the importance of capital-cost and long-run investment assumptions.

Finally, this remains a retrospective historical study prepared in 2026. The 27 October 2025 reference close preceded the FY2025 10-K's **16:12:49 after-close acceptance**. Cash and debt are August proxies, and annual periods simplify the October valuation timing. Assumptions were finalized retrospectively with access to subsequent outcomes, so hindsight bias cannot be excluded. Reverse DCF does not remove those information and timing limitations.

Historical inputs and their public sources are documented in the [project report's source bibliography](README.md#sources). This companion adds conditional calculations, not new market observations. The [workbook](WD40_DCF_Portfolio.xlsx) remains the editable calculation source; this document is a static snapshot.
