# Limitations and Interpretation Guardrails

## 1) Historical Dependence
MMM reflects historical relationships from Jul 2, 2022 to Jun 28, 2025. Structural market shifts outside this pattern may change realized effectiveness.

## 2) Fit Metrics Are Not the Full Story
The model shows excellent in-sample metrics (R² 0.99, MAPE 2%, wMAPE 2%), but high fit alone does not guarantee out-of-sample performance or perfect causal certainty.

## 3) Channel Aggregation Trade-off
Grouping correlated channels improves stability and interpretability but can reduce granularity for platform-level execution decisions.

## 4) Optimization Is Scenario-Based
The optimization output is conditional on:
- fixed total budget,
- chosen movement bounds (-30% to +30%),
- observed response relationships.

Different constraints or business priorities could produce different recommendations.

## 5) Practical Implementation Effects
Operational factors (creative quality, timing, inventory, competition, and execution lag) can influence realized outcomes versus modeled expectations.

## Recommended Usage
Treat this case study as a decision-support framework for strategic allocation, then validate through ongoing performance tracking and periodic model refreshes.
