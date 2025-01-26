# grover_quantum_inspire.ipynb
This file contains the code which is used to print out Quantum Inspire's cQASM code which, using Quantum Inspire, 
generates the N-qubit linear-nearest-neighbour version of Grover's algorithm when putting in an element 
to search for and the number of qubits N. This algorithm also adds the optimal number of Grover iterations.

# grover_ibm.ipynb

### grover_qiskit(n: int, element: int):
This method contains the code to generate the N-qubit linear-nearest-neighbour version of Grover's algorithm when putting in an element 
to search for and the number of qubits N in QiSkit. This algorithm does *NOT* the optimal number of Grover iterations, due to noise accumulation.

### grover(n: int, element: int):
This method contains the code to generate the N-qubit all-to-all version of Grover's algorithm when putting in an element 
to search for and the number of qubits N in QiSkit. This algorithm does *NOT* the optimal number of Grover iterations, due to noise accumulation.

The rest of the code is used to run Grover's algorithm, either the all-to-all or linear-nearest-neighbour version, 10 times with 4096 shots each, 
and provide a histogram with the aggregated data over all 10 runs, which contains the probability for each possible qubit state to be measured.

# grover_fake_backend.ipynb
This file contains the code which runs Grover's algorithm for N qubits on a fake back-end and compares the performance of all-to-all connectivity 
to linear-nearest-neighbour connectivity
