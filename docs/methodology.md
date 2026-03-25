# Methodology

## 1) Problem Framing
The case study was designed to answer a practical planning question: **how to improve incremental revenue through media reallocation while holding total spend constant**. This moved the analysis beyond historical attribution and into forward-looking decision support.

## 2) Modeling Framework
Google Meridian was used as the MMM engine in a Bayesian framework to estimate:
- baseline and incremental effects,
- channel-level contribution,
- ROI and marginal ROI,
- response curves for saturation and headroom assessment.

## 3) Data Scope and Variable Design
### Analysis Window
- Jul 2, 2022 – Jun 28, 2025

### Core variable groups
- **Outcome:** revenue/sales target for Brand B
- **Media inputs:** channel-level spend variables (including Digital_Social, TV, Radio, Print in final reporting)
- **Non-media controls:** price index, festival index, rainfall index
- **Treatment-like business driver:** Trade_Spend

The inclusion of non-media controls was essential to avoid over-attributing business variation to paid media.

## 4) Model Refinement Logic
The model development process prioritized both statistical credibility and business interpretability:
- diagnostics for variable relationships,
- channel grouping decisions where correlation was high,
- consistent interpretation checks against business context.

The purpose was to avoid producing attractive but fragile output.

## 5) Evaluation Approach
Model evaluation included fit metrics (R², MAPE, wMAPE) and practical validation logic. The project explicitly treated high fit as one component of confidence rather than the sole decision criterion.

## 6) Decision Layer: Response and Optimization
Two layers were used for recommendations:
1. **Response curves + marginal ROI** to understand channel saturation and next-dollar efficiency.
2. **Constrained optimization** to simulate realistic budget shifts under fixed total budget and movement bounds.

This ensured recommendations were operationally feasible, not purely theoretical.
