# Bayesian Causal Inference Results

All numerical regression and posterior sampling use JAX. There is no scikit-learn dependency.

- `figures/`: visual diagnostics and calibrated/uncalibrated interval comparisons
- `reports/`: predictive metrics, ATE errors and repeated-simulation coverage
- `data/`: synthetic observed and oracle datasets
- `posterior_samples/`: posterior draws for reproducibility

**Important:** Interpreting regression coefficients as causal effects requires causal assumptions. The speed-only model is deliberately misspecified for causal inference.
