# QOSF Task

This repository contains an implementation of Grover's algorithm using Qiskit, a popular quantum computing framework. The example demonstrates how to encode a problem into a quantum circuit, specifically designed to find elements less than a given threshold `k` in a list of numbers.

## Overview

Grover's algorithm is a quantum algorithm for searching an unsorted database with quadratic speedup. This implementation focuses on using Grover's algorithm to find all elements in a list that are less than a specified value `k`. The algorithm constructs a quantum circuit that encodes the problem and uses Grover's operator to amplify the probability of the correct states.

## Dependencies

- Qiskit: A comprehensive open-source quantum computing framework.
- Qiskit Aer: A component of Qiskit for simulating quantum circuits.
- Qiskit IBM Runtime: Allows running quantum circuits on IBM quantum computers.

## Installation

Ensure you have Python 3.8 or later installed. Then, install Qiskit and its dependencies:

```bash
pip install qiskit qiskit-aer qiskit-ibm-runtime
```

## Usage

To run the example, execute the Python script. The script defines a list of numbers and a threshold `k`. It then constructs an oracle circuit that marks the states corresponding to numbers less than `k` and uses Grover's algorithm to amplify the probability of these states. Finally, it simulates the circuit and prints the results.

```python
list_n = [4,9,11,14,1,13,6,15]
k = 7
print(less_than_k(k, list_n))
```

## Circuit Diagrams

The repository includes visualizations of the oracle and Grover's circuit. To generate these diagrams, run the following commands:

```python
oracle = make_oracle(list_n, k, NUM_QBITS)
oracle.draw()

circuit = make_grover(oracle)
circuit.draw()
```

