Project Overview

This project evaluates the long-term growth trajectory of Tumblr following its 2013 acquisition by Yahoo. Using historical user data (2013–2016), I developed a suite of time-series models to forecast worldwide user growth through 2026. This analysis replaces traditional Excel-based modeling with a fully reproducible Python workflow.

Modeling Strategy

To account for the high volatility of social media growth, I utilized a Hybrid Ensemble approach:

-Prophet (Meta): Captures non-linear growth and historical trend shifts (e.g., the post-acquisition surge).

-ETS (Exponential Smoothing): Provides a conservative "Damped Trend" baseline to account for market saturation.

-Ensemble Model: A strategic average of both models, providing a balanced "Most Likely" scenario for business evaluation.

Key Findings

-Historical Context: The data begins at the May 2013 acquisition (Month 0) and tracks the platform through its peak growth phases.

-Predictive Insight: While aggressive models suggest a path to 600M users, the Damped ETS model indicates a more realistic saturation point near 225M.

-Model Accuracy: Validated via Rolling Origin Cross-Validation, achieving a Mean Absolute Percentage Error (MAPE) of ~5.2% on short-term horizons.

Technical Implementation

Language: Python 3.12

Libraries: pandas, prophet, statsmodels, matplotlib, scikit-learn

Workflow: Data cleaning → Date mapping → Grid search for ETS parameters → Prophet training → Cross-validation → Ensemble forecasting.
