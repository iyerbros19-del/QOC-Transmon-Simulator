# QOC-Transmon-Simulator
An open-loop Quantum Optimal Control (QOC) pipeline using Qiskit Dynamics to optimize Gaussian microwave pulses and mitigate multi-axis coherent errors in superconducting transmon qubits.
# Quantum Pulse Optimal Control & Coherent Error Mitigation

I implement a full open-loop Quantum Optimal Control and simulation pipeline designed to protect single-qubit gate operations against non-commuting hardware noise in superconducting transmon systems. 

Driven by an automated classical feedback loop, the framework numerical solves the time-dependent Schrödinger equation to dynamically reshape microwave pulse geometries—bypassing the limitations of rigid analytical pulse programming without requiring invasive hardware recalibration.

##  Structure
* `quantum_pulse_optimal_control.ipynb` — Core Jupyter notebook containing the physics engine, optimization loop, and data visualizations.
* `QOC-Writeup-2.pdf` — Complete LaTeX-grade technical writeup structured as an academic preprint analyzing the underlying mechanics and physical intuition of the optimization space.
