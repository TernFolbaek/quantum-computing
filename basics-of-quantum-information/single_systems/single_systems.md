## Classical Information
### Classical States and Probability Vectors
In classical information theory, a system's state can be described deterministically. However, when dealing with systems that have uncertain outcomes, we use probability vectors to represent the state of the system.

Example:

A classical bit can be in state 0 or state 1. The probability vector for a system that is equally likely to be in state 0 or state 1 is given by:

$$
p = \begin{bmatrix}
0.5 \\
0.5
\end{bmatrix}
$$

## Measuring Probabilistic States
### The process of measuring a probabilistic state involves determining the state of a system based on the probability distribution.


If we measure the above system, we expect to find it in state 0 with a probability of 0.5 and in state 1 with a probability of 0.5.

## Classical Operations
### Classical operations on bits include logical operations such as AND, OR, and XOR.

Example:

The AND operation can be represented as follows:

$$
\text{AND}(0, 1) = 0
$$

$$
\text{AND}(1, 1) = 1
$$

## Quantum Information
### Quantum State Vectors
In quantum mechanics, the state of a quantum system is described by a quantum state vector. This vector is a complex vector in a Hilbert space and contains amplitudes that represent the probability of finding the system in a particular state upon measurement.

Example:

The state vector for a quantum bit (qubit) in a superposition state can be written as:

$$
|\psi\rangle = \alpha|0\rangle + \beta|1\rangle
$$

where $\( |\alpha|^2 + |\beta|^2 = 1 \)$.

## Measuring Quantum States
### When a quantum state is measured, the outcome is probabilistic and is given by the square of the amplitudes in the state vector.

Example:

For the state $\( |\psi\rangle \)$ defined above, the probability of measuring the state $\( |0\rangle \)$ is $\( |\alpha|^2 \)$, and the probability of measuring the state $\( |1\rangle \)$ is $\( |\beta|^2 \)$.

## Unitary Operations
### Unitary operations are reversible transformations on quantum state vectors that preserve the inner product (and hence the probabilities).

Example:

A common unitary operation is the Hadamard gate, represented as:

$$
H = \frac{1}{\sqrt{2}}\begin{bmatrix}
1 & 1 \\
1 & -1
\end{bmatrix}
$$

This gate puts a qubit from state $\( |0\rangle \)$ to the superposition state $\( \frac{|0\rangle + |1\rangle}{\sqrt{2}} \)$.
