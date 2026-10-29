# Trustworthy Causal Inference

This repository contains my experiments with causal inference and Bayesian uncertainty using JAX.

The experiments use synthetic machine workload, operating speed, and energy consumption, so the true causal effects are known.

## Data generation

I start with workload $U$, speed $X$, and energy consumption $Y$:

$$
U\sim\mathcal N(0,1),\qquad X=0.8U+\epsilon_X
$$

$$
Y=2X+1.5U+0.5XU+\epsilon_Y
$$

Here, $\epsilon_X,\epsilon_Y\sim\mathcal N(0,1)$ are independent noise terms. Workload is a common cause of speed and energy use.

I also add a nonlinear outcome model:

$$
Y=2X+1.5U+0.5XU+0.3X^2+0.6\sin(X)+\epsilon_Y.
$$

For the nonlinear model, the effect of changing speed from $0$ to $1$ is:

$$
Y(1)-Y(0)=2.3+0.5U+0.6\sin(1).
$$

The generator also covers workload distribution shifts, hidden confounding, noisy workload measurements, and weak treatment overlap.

## Model comparisons

I compare ordinary regression, confounder-adjusted regression, interaction and nonlinear regression, and a JAX neural network. I examine prediction error and causal-effect error separately, using the known treatment effects as reference values.

## Bayesian analysis

I fit Bayesian regression models and examine posterior ATE estimates, credible intervals, and interval coverage. I also compare what happens when workload is included or omitted from the model.


