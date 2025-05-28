# Minimum-Variance Portfolio Optimizer

This project implements a minimum-variance portfolio optimizer in Python using NumPy. It solves both:

- The **standard minimum-variance portfolio** problem (without return constraint)
- The **minimum-variance portfolio with a specified expected return**, optionally allowing short-selling

It uses the Lagrangian/KKT formulation and includes numerical stability handling (pseudoinverse fallback for ill-conditioned systems).

---

## 🧠 What It Does

Given:
- A covariance matrix of asset returns $\Sigma$
- A vector of expected returns $\mu$
- An optional target return $\mu^*$

The optimizer solves:

$$
\min_w \ w^T \Sigma w \quad \text{subject to} \quad w^T \mu = \mu^*, \quad \sum w_i = 1
$$

If no target return is provided, it computes the global minimum-variance portfolio.

---

## 🧪 Features

- ✅ Supports arbitrary number of assets
- ✅ Handles singular or ill-conditioned matrices using pseudoinverse
- ✅ Returns optimal weights and portfolio risk
- ✅ Easily extendable to include long-only constraints or regularization
- ✅ Plots efficient frontier for visualization

---

## 📦 Requirements

- Python 3.x
- NumPy
- cvxpy
- matplotlib

Install dependencies:

```bash
pip install numpy
