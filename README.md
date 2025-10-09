# Quantum Finance Lab

### Exploring Quantum Algorithms for Financial Modeling

**Quantum Finance Lab** is a compact research and coding project that demonstrates how quantum algorithms can be applied to key problems in quantitative finance.  
The goal is to build intuitive, reproducible examples that bridge **quantum computing** and **financial optimization**, highlighting both potential advantages and current limitations of near-term quantum hardware.

This project currently contains two core modules:

---

## 1. Quantum Portfolio Optimization

Portfolio optimization is a cornerstone of modern finance, where the objective is to allocate capital among assets to achieve an optimal balance between risk and return.  
In this module, we express the classical *mean–variance optimization* problem as a **Quadratic Unconstrained Binary Optimization (QUBO)** model, which can be solved using **quantum algorithms** such as the *Quantum Approximate Optimization Algorithm (QAOA)*.

The implementation includes:
- Classical baseline using **CVXPY** for convex optimization  
- Quantum solvers implemented via **Qiskit’s QAOA** and **VQE** frameworks  
- Visualizations comparing energy landscapes, convergence, and asset weight distributions  

This module serves as an introduction to **quantum combinatorial optimization** in a financial context.

---

## 2. Quantum Option Pricing

Option pricing typically relies on Monte Carlo simulations or analytical models such as Black–Scholes.  
This module explores how **Quantum Amplitude Estimation (QAE)** can accelerate the computation of expected option payoffs, offering a theoretical **quadratic speedup** over classical Monte Carlo.

The implementation demonstrates:
- Classical Monte Carlo pricing for a European call option  
- Quantum Amplitude Estimation (simulated with Qiskit) for expected payoff estimation  
- Comparison of convergence rates and sampling efficiency  

This example shows how **quantum algorithms for amplitude estimation** can enhance financial simulations, even on small-scale quantum devices or simulators.

---

