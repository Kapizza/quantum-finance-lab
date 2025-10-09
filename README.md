# quantum-finance-lab — Quantum Portfolio Optimization (QAOA vs Classical)

Short, reproducible demo that formulates mean–variance portfolio selection as a QUBO, then solves it with:
1) a classical mixed-integer optimizer (CVXPY), and
2) **QAOA** on a quantum simulator (Qiskit).

You will get side-by-side solutions, weights, risk, return, and a quick timing comparison.

## Problem
Given expected returns vector $\mu \in \mathbb{R}^n$ and covariance matrix $\Sigma \in \mathbb{R}^{n \times n}$, choose a subset of assets (binary decision $x_i \in \{0,1\}$) with a budget of exactly $k$ assets that balances return and risk. Objective:

\\[
\min_{x \in \{0,1\}^n}\; x^\top \Sigma x - \lambda\, \mu^\top x
\quad \text{s.t.} \quad \sum_i x_i = k
\\]

Turn this into a **QUBO** with a penalty for the budget constraint:
\\[
\min_x\; x^\top \Sigma x - \lambda\, \mu^\top x + A\left(\sum_i x_i - k\right)^2
\\]
with $A$ large enough to enforce the budget.

## What this repo shows
- Building the QUBO matrix $Q$ from $\mu, \Sigma, \lambda, k, A$.
- Solving with CVXPY (binary variables) as a classical baseline.
- Solving the same QUBO with QAOA on the Aer simulator.
- Comparing objective values and chosen assets.


