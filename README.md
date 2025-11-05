# Qiskit-Bernstein-Vazirani

## Overview
A Qiskit 2.x implementation of the **Bernstein–Vazirani** algorithm.  
The algorithm finds a hidden bit-string \( s \) in a Boolean function \( f(x) = s \cdot x \oplus b \) using a single quantum query.

This repository contains:
- `Bernstein_Vazirani.py` — a Qiskit 2.x script implementing the algorithm with example runs.
- (Optional) `Bernstein_Vazirani.ipynb` — you can convert the script into a notebook for interactive use.
- `README.md` — this file.

## Requirements
- Python >= 3.9  
- Qiskit 2.x and Aer:
```bash
pip install qiskit qiskit-aer matplotlib
```

## How to run
1. Clone the repository:
```bash
git clone https://github.com/<your-username>/Qiskit-Bernstein-Vazirani.git
cd Qiskit-Bernstein-Vazirani
```
2. Run the script:
```bash
python Bernstein_Vazirani.py
```
3. Observe printed counts and a histogram showing the recovered secret string.

## File: Bernstein_Vazirani.py (summary)
- Builds an oracle for a secret bit-string `s` (e.g., `s = "1011"`).
- Prepares `n` input qubits and one ancilla qubit.
- Applies Hadamard gates, calls the oracle once, then Hadamard again and measures.
- The measurement yields the secret string `s` (assuming ideal simulation).

## Programming Tasks (for students)
1. **Change the secret string `s`** and verify the measured output matches `s`.  
2. **Modify the oracle** to include an additional constant bit `b` (i.e., implement `f(x) = s·x ⊕ b`) and show how `b` affects the ancilla only.  
3. **Run on a real IBM backend** using `qiskit_ibm_runtime` and compare results with the simulator (Optional).  
4. **Add noise** via `qiskit_aer.noise.NoiseModel` and analyze robustness.  
5. **Create a notebook** that explains each step with visualizations and markdown.

## References
- Qiskit Textbook: Bernstein–Vazirani — https://qiskit.org/textbook/ch-algorithms/bernstein-vazirani.html
- Nielsen & Chuang, *Quantum Computation and Quantum Information*
