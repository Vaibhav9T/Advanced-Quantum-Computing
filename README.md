# Advanced Quantum Computing

A collection of quantum computing practicals implemented using [Qiskit](https://qiskit.org/) and simulated on [Google Colab](https://colab.research.google.com/). This repository covers foundational and advanced quantum algorithms, including search algorithms, quantum transforms, factoring, machine learning, and cryptography.

---

## 📁 Repository Contents

| File | Description |
|------|-------------|
| `ac1-8.py` | Python source for all 8 practicals (auto-exported from Colab) |
| `AC1-8.ipynb` | Jupyter/Colab notebook with all practicals |
| `AC18.pdf` / `AC18.docx` | Report document for the practicals |
| `CA_pro.pdf` | Additional course/project reference |

---

## 🧪 Practicals Overview

### Practical 1 – Bernstein-Vazirani Algorithm
Finds a hidden binary string `s` in a single query using quantum parallelism.  
- Encodes the hidden string `"110"` into an oracle  
- Uses Hadamard gates and a single oracle call to recover `s` deterministically  
- Demonstrates **quantum advantage** over classical algorithms that require `n` queries

### Practical 2 – Simon's Algorithm (Hidden String)
Solves Simon's problem: given a 2-to-1 function `f(x) = f(x ⊕ s)`, find the hidden period `s`.  
- Creates a superposition over input register and applies an oracle  
- Post-processes measurement results classically to recover `s`  
- Provides **exponential speedup** over any classical algorithm

### Practical 3 – Grover's Search Algorithm (2-Qubit)
Searches an unstructured database to find the marked state `|11⟩` with high probability.  
- Applies Hadamard gates for superposition, a phase-flip oracle, and a diffusion operator  
- Achieves a **quadratic speedup** compared to classical linear search  
- Demonstrates the key steps of amplitude amplification

### Practical 4 – Grover's Search (3-Qubit Extension)
Extends Grover's algorithm to 3 qubits, searching for the marked state `|101⟩`.  
- Uses a multi-controlled Toffoli (MCX) gate in the diffusion operator  
- Applies the optimal number of Grover iterations (2 iterations for 3 qubits)  
- Illustrates the scalability of the Grover framework

### Practical 5 – Quantum Fourier Transform (QFT) & Inverse QFT
Implements the Quantum Fourier Transform and its inverse on 3 qubits.  
- Prepares the input state `|5⟩` and applies QFT  
- Reverses the transform using Inverse QFT to recover the original state  
- QFT is a core subroutine in Shor's algorithm and phase estimation

### Practical 6 – Shor's Algorithm (Integer Factoring)
Factors the integer `N = 15` using Shor's quantum period-finding algorithm.  
- Uses 8 counting qubits and 4 target qubits  
- Implements controlled modular exponentiation `2^x mod 15`  
- Applies Inverse QFT to extract the period `r`, then classically computes GCD to find factors  
- Demonstrates **exponential speedup** over the best known classical factoring algorithms

### Practical 7 – Quantum Support Vector Machine (QSVM)
Classifies synthetic 2-feature data using a quantum kernel-based SVM.  
- Encodes data with the `ZZFeatureMap` into quantum states  
- Computes a quantum kernel via state fidelity using `ComputeUncompute`  
- Trains and evaluates a `QSVC` classifier from `qiskit-machine-learning`  
- Explores the potential of **quantum-enhanced machine learning**

### Practical 8 – BB84 Quantum Key Distribution (QKD)
Simulates the BB84 quantum cryptography protocol between Alice and Bob.  
- Alice encodes random bits in randomly chosen Z or X bases  
- Bob measures in randomly chosen bases  
- Key sifting retains only bits where bases match, producing a shared secret key  
- Demonstrates the foundations of **quantum-secure communication**

---

## 🛠️ Technologies & Dependencies

- **Python 3.8+**
- [Qiskit](https://qiskit.org/) – core quantum computing framework
- [qiskit-aer](https://github.com/Qiskit/qiskit-aer) – high-performance quantum circuit simulator
- [qiskit-machine-learning](https://github.com/qiskit-community/qiskit-machine-learning) – quantum ML algorithms
- [NumPy](https://numpy.org/)
- [scikit-learn](https://scikit-learn.org/)
- [Matplotlib](https://matplotlib.org/)

---

## 🚀 Getting Started

### Run on Google Colab (Recommended)

1. Open `AC1-8.ipynb` in [Google Colab](https://colab.research.google.com/)
2. Install dependencies by running the setup cells:
   ```python
   pip install qiskit qiskit_aer qiskit-machine-learning
   ```
3. Run each practical cell by cell

### Run Locally

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Vaibhav9T/Advanced-Quantum-Computing.git
   cd Advanced-Quantum-Computing
   ```

2. **Install dependencies:**
   ```bash
   pip install qiskit qiskit_aer qiskit-machine-learning scikit-learn matplotlib numpy
   ```

3. **Run the practicals:**
   ```bash
   python ac1-8.py
   ```

---

## 📚 Key Concepts

| Concept | Practicals |
|---------|-----------|
| Quantum Superposition & Entanglement | All |
| Oracle-based Query Algorithms | 1, 2, 3, 4 |
| Amplitude Amplification | 3, 4 |
| Quantum Fourier Transform | 5, 6 |
| Period Finding & Number Theory | 6 |
| Quantum Machine Learning | 7 |
| Quantum Cryptography | 8 |

---

## 📄 License

This project is intended for educational purposes as part of an Advanced Quantum Computing course.
