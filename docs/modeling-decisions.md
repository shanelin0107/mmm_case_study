# Modeling Decisions

## Decision 1: Use Google Meridian for Bayesian MMM Estimation
This project used Google Meridian to estimate channel-level contribution and ROI in a Bayesian MMM framework. The choice aligned with the need to evaluate both historical impact and forward-looking budget decisions through response and optimization outputs.

## Decision 2: Scope the Model to Brand B Only
The model was scoped to Brand B rather than pooling all brands. This was a deliberate decision to improve recommendation relevance for the specific business unit and avoid dilution of brand-specific dynamics.

## Decision 3: Include Non-Media Context Controls
Controls included:
- price index,
- festival index,
- rainfall index.

These variables were included to separate media effects from contextual demand movements and improve attribution credibility.

## Decision 4: Treat Trade_Spend as a Material Driver
Trade_Spend was modeled as an important non-media treatment/driver because it materially affected sales. Excluding it would risk inflating apparent media contribution.

## Decision 5: Address Multicollinearity Proactively
Multicollinearity across digital variables was a major concern. High co-movement can make channel coefficients unstable and reduce interpretability.

### How this was handled
- Used correlation checks and VIF diagnostics as support tools.
- Grouped highly correlated media variables into broader channels when needed.
- Example grouping logic: Facebook + Instagram into Meta; broader Digital Social grouping depending on the final model version.

The intent was not to maximize granularity at any cost, but to preserve stable, decision-usable estimates.

## Decision 6: Do Not Rely on Fit Metrics Alone
The model showed very high in-sample fit (R² 0.99, MAPE/wMAPE 2%), but the project did not treat fit alone as proof of practical certainty. Final interpretation also considered variable logic, multicollinearity handling, and response behavior.

## Decision 7: Separate “Scale” from “Efficiency” in Recommendations
Response curves and marginal ROI were used to distinguish:
- channels that drive meaningful volume,
- channels that deliver strong efficiency,
- channels that may be nearing saturation.

This prevented simplistic “highest ROI wins” conclusions.

## Decision 8: Frame Optimization as Constrained Reallocation
Optimization was framed as a **constrained reallocation** exercise, not a blanket reduction of lower-ROI channels. Channel movement bounds (-30% to +30%) were used to reflect operational and strategic realities.
