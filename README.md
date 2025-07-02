# ErdosQC25-5qubitcode

We implement a Qiskit function `fiveq_ecc` that illustrates the use of the 5-qubit code to correct random Pauli errors. Specifically, this function takes as input a boolean $x \in \mathbb{F}_2$ and an error probability $p$, and outputs a circuit which
- prepares (not fault tolerantly) the logical $|x_L\rangle$ state for the 5-qubit code,
- runs this logical state through a uniform Pauli error channel, with error rate $p$ for each physical qubit,
- measures syndromes for the 5-qubit,
- applies the recovery operations as appropriate, and
- measures the data qubits and decodes the result.

The 5-qubit code is a $[[5,1,3]]$ stabilizer code. It is the smallest quantum error correcting code that can detect and correct an arbitrary single (physical) qubit error.

The Qiskit function and further documentation is contained in the Jupyter notebook `5qubit code.ipynb`. A later part of the notebook visualizes the success probability (as empirically observed from simulations) as a function of $p$. Here the success probabilty is the probabilty that we measure a component of $|x_L\rangle$ at the end. 
