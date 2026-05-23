# QOC-Transmon-Simulator
An open-loop Quantum Optimal Control (QOC) pipeline using Qiskit Dynamics to optimize Gaussian microwave pulses and mitigate multi-axis coherent errors in superconducting transmon qubits.
# Quantum Pulse Optimal Control & Coherent Error Mitigation

This repository implements a full open-loop Quantum Optimal Control (QOC) and simulation pipeline designed to protect single-qubit gate operations against non-commuting hardware noise in superconducting transmon systems. 

Driven by an automated classical feedback loop, the framework numerical solves the time-dependent Schrödinger equation to dynamically reshape microwave pulse geometries—bypassing the limitations of rigid analytical pulse programming without requiring invasive hardware recalibration.

## Key Features
* **Time-Dependent Hamiltonian Simulation:** Models a truncated two-level transmon qubit in the rotating frame using `Qiskit Dynamics`.
* **Multi-Axis Coherent Noise Engine:** Simulates compound experimental errors by coupling an $X$-axis systematic control amplitude calibration bias ($+15\%$) with a non-commuting static $Z$-axis detuning drift ($\delta$).
* **Derivative-Free Optimization Pipeline:** Deploys a classical Nelder-Mead downhill simplex heuristic over a 2D parameter landscape (peak amplitude $A$ and temporal width $\sigma$) to minimize quantum state infidelity ($1 - \mathcal{F}$).
* **Error-Canceling Geometric Tracking:** Reshapes standard Gaussian control pulses to execute a corrected geometric trajectory on the Bloch sphere, restoring target $\pi$-gate fidelity from an error-dominated state ($<95\%$) back into the fault-tolerant threshold ($>99.5\%$).

## Project Structure
* `quantum_pulse_optimal_control.ipynb` — Core Jupyter notebook containing the physics engine, optimization loop, and data visualizations.
* `paper/` — Complete LaTeX-grade technical writeup structured as an academic preprint analyzing the underlying mechanics and physical intuition of the optimization space.
