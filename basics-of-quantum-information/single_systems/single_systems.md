# Information in Single Systems

#### Below will focus on the manipulation and information extraction which are done on single Systems. A system can be denoted various notations, however in this notebook we will be focusing on the system of bits and qubits, respective to the classical and quantum states. 
A system could for example be a bit X. This bit can be in two possible states, {0,1}, which is called the classical state set. Therefore the hierarchy is as follows: System, Set, State. A system which is in a state given its state set.

In this current notebook and the notebooks to follow will utilize the dirac-notation to describe our state vectors, both in the classical and quantum sense. The Dirac Notation utilizes the bra-ket, which are respective vector notations to a row vector and a column vector. Bra denoting a row vector, and ket denoting a column vector. These vectors will look as follows:

$$
|\psi\rangle = \alpha|0\rangle + \beta|1\rangle =  \begin{bmatrix}
\alpha \\
\beta
\end{bmatrix}
$$


$$
\langle\psi| = \langle0|\alpha + \langle1|\beta =\begin{bmatrix} \alpha & \beta \end{bmatrix}
$$

## Classical Information

### Classical States and Probability Vectors

In classical information theory, we often describe the state of a system in terms of probabilities. This is especially true for stochastic processes where the outcome is not deterministic. 

A probability vector contains non-negative entries that sum up to one and each entry in the vector represents the probability of the system being in a particular state. The length of the probability vector is equal to the number of possible states of the system.

For example, for a binary system (a bit) that can be in state 0 or state 1, the probability vector is a two-dimensional vector where each component represents the probability of the system being in state 0 or state 1, respectively.

The general form of a probability vector for a binary system is given by:

$$
p = \begin{bmatrix}
p_0 \\
p_1
\end{bmatrix}
$$

where $ p_0 + p_1 = 1 $.

The probabilities $\( p_0 \) and \( p_1 \)$ correspond to the likelihood of the system being in state 0 and state 1, respectively.

### Example of a Biased Coin

Consider a biased coin that has a 70% chance of landing heads (state 0) and a 30% chance of landing tails (state 1). The probability vector for this coin is:

$$
p = \begin{bmatrix}
0.7 \\
0.3
\end{bmatrix}
$$


## Measuring Probabilistic States

When dealing with the measurement of probabilistic states in classical systems, we can represent the uncertainty of a system's state with a probability distribution vector. This vector quantifies the likelihood of the system being found in each of its possible states upon measurement.

For example, consider a classical system that can be in one of three possible states: \(\{0, 1, 2\}\). Let's define a probability vector \( \mathbf{p} \) for this system as:

$$
\mathbf{p} = \begin{bmatrix}
p_0 \\
p_1 \\
p_2
\end{bmatrix}
$$

where \( p_0, p_1, \) and \( p_2 \) represent the probabilities of the system being in states 0, 1, and 2, respectively.

Suppose the system is twice as likely to be in state 0 than in state 1, and the probability of being in state 2 is the same as in state 1. If we normalize this probability vector such that the sum of probabilities equals 1 (as required by the axioms of probability), we obtain:

$$
\mathbf{p} = \begin{bmatrix}
\frac{2}{4} \\
\frac{1}{4} \\
\frac{1}{4}
\end{bmatrix} = \begin{bmatrix}
0.5 \\
0.25 \\
0.25
\end{bmatrix}
$$

The measurement process then involves observing the system's state according to this distribution. For instance, if we perform a measurement, the expected outcomes would be:

- The system is found in state 0 with a probability of \( p_0 = 0.5 \).
- The system is found in state 1 with a probability of \( p_1 = 0.25 \).
- The system is found in state 2 with a probability of \( p_2 = 0.25 \).

This probabilistic nature contrasts with quantum systems, where a qubit can exist in a superposition of states and the probabilities are derived from the square of the amplitudes of the state vector. Upon measurement, a quantum state collapses to one of the basis states, which is analogous to a classical bit being observed as either 0 or 1. However, the quantum measurement is governed by different principles, such as the Born rule, which uses the squared magnitude of the amplitudes to determine probabilities.


### Operations on Classical States
#### Deterministic operations

First, there are deterministic operations, where each classical state \( a \in \Sigma \) is transformed into \( f(a) \) for some function \( f \) of the form \( f: \Sigma \rightarrow \Sigma \).

For example, if \( \Sigma = \{0, 1\} \), there are four functions of this form, \( f_1, f_2, f_3 \), and \( f_4 \), which can be represented by tables of values as follows:

\[
\begin{array}{cc}
a & f_1(a) \\
\hline
0 & 0 \\
1 & 0 \\
\end{array}
\quad
\begin{array}{cc}
a & f_2(a) \\
\hline
0 & 0 \\
1 & 1 \\
\end{array}
\quad
\begin{array}{cc}
a & f_3(a) \\
\hline
0 & 1 \\
1 & 0 \\
\end{array}
\quad
\begin{array}{cc}
a & f_4(a) \\
\hline
0 & 1 \\
1 & 1 \\
\end{array}
\]

The first and last of these functions are _constant_: \( f_1(a) = 0 \) and \( f_4(a) = 1 \) for each \( a \in \Sigma \). The middle two are not constant, they are _balanced_, in the sense that the two possible output values occur the same number of times as we range over the possible inputs. The function \( f_2 \) is the identity function: \( f_2(a) = a \) for each \( a \in \Sigma \). And \( f_3 \) is the function \( f_3(0) = 1 \) and \( f_3(1) = 0 \), which is better-known as the NOT function.

The actions of deterministic operations on probabilistic states can be represented by matrix-vector multiplication. Specifically, the matrix \( \mathbf{M} \) that represents a given function \( f: \Sigma \rightarrow \Sigma \) is the one that satisfies

\[
\mathbf{M} |a\rangle = |f(a)\rangle
\]

for every \( a \in \Sigma \). Such a matrix always exists and is unique.

For example, the matrices \( \mathbf{M}_1, \mathbf{M}_2, \mathbf{M}_3 \), and \( \mathbf{M}_4 \) corresponding to the functions \( f_1, \ldots, f_4 \) above are as follows:

\[
\mathbf{M}_1 = \begin{bmatrix}
1 & 0 \\
0 & 0 \\
\end{bmatrix}, \quad
\mathbf{M}_2 = \begin{bmatrix}
1 & 0 \\
0 & 1 \\
\end{bmatrix}, \quad
\mathbf{M}_3 = \begin{bmatrix}
0 & 1 \\
1 & 0 \\
\end{bmatrix}, \quad
\mathbf{M}_4 = \begin{bmatrix}
0 & 0 \\
1 & 1 \\
\end{bmatrix}.
\]


#### Probabilistic Operations
Operations on classical states can be represented by matrices that transform one probability vector into another. These matrices must have non-negative entries and each column must sum up to one to preserve the total probability.

An example of an operation is a stochastic matrix that represents a noisy channel, which can alter the state of the bit with certain probabilities.

For instance, a bit flip channel that flips the state of the bit with a probability of 10% can be represented by the following matrix:

$$
M = \begin{bmatrix}
0.9 & 0.1 \\
0.1 & 0.9
\end{bmatrix}
$$

This matrix tells us that if our system is in state 0, there is a 90% chance it will stay in state 0 after passing through the channel and a 10% chance it will flip to state 1. The same probabilities apply to state 1.

If our system's initial state is given by the probability vector \( p \), the state after passing through the channel is given by:

$$
p' = M p = \begin{bmatrix}
0.9 & 0.1 \\
0.1 & 0.9
\end{bmatrix}
\begin{bmatrix}
p_0 \\
p_1
\end{bmatrix}
= \begin{bmatrix}
0.9p_0 + 0.1p_1 \\
0.1p_0 + 0.9p_1
\end{bmatrix}
$$

The new probability vector \( p' \) reflects the altered state probabilities due to the noisy channel.

## Quantum Information

### Quantum State Vectors

In quantum mechanics, the state of a quantum system is described by a quantum state vector. This vector is a complex vector in a Hilbert space and contains amplitudes that represent the probability of finding the system in a particular state upon measurement.

Example:

The state vector for a quantum bit (qubit) in a superposition state can be written as:

$$
|\psi\rangle = \alpha|0\rangle + \beta|1\rangle
$$

where \(|\alpha|^2 + |\beta|^2 = 1\).

These coefficients \( \alpha \) and \( \beta \) are complex numbers and can be represented as \( \alpha = a + bi \) and \( \beta = c + di \), where \( a, b, c, d \) are real numbers and \( i \) is the imaginary unit. The modulus squared of these coefficients, \( |\alpha|^2 \) and \( |\beta|^2 \), give the probability of the qubit being measured in the corresponding state.

### Measuring Quantum States

When a quantum state is measured, the outcome is probabilistic and is given by the square of the amplitudes in the state vector.

Let's explore another example, the state \( |\psi\rangle \) given by a general superposition of the basis states \( |0\rangle \) and \( |1\rangle \):

$$
|\psi\rangle = \frac{1}{\sqrt{3}}|0\rangle + \sqrt{\frac{2}{3}}|1\rangle
$$

Here, the probabilities of measuring the state in \( |0\rangle \) or \( |1\rangle \) are:

$$
\text{Pr(outcome is } 0) = \left|\left\langle 0 | \psi \right\rangle\right|^2 = \left|\frac{1}{\sqrt{3}}\right|^2 = \frac{1}{3}
$$

$$
\text{Pr(outcome is } 1) = \left|\left\langle 1 | \psi \right\rangle\right|^2 = \left|\sqrt{\frac{2}{3}}\right|^2 = \frac{2}{3}
$$

This example illustrates that the qubit is more likely to be found in state \( |1\rangle \) upon measurement.

### Bloch Sphere Representation

The state of a single qubit can also be represented on the Bloch sphere. Every point on the surface of this sphere corresponds to a possible state of the qubit.

A qubit state on the Bloch sphere is given by:

$$
|\psi\rangle = \cos\left(\frac{\theta}{2}\right)|0\rangle + e^{i\phi}\sin\left(\frac{\theta}{2}\right)|1\rangle
$$

where \( \theta \) and \( \phi \) are the polar and azimuthal angles, respectively.

### Quantum Gates and Operations

Quantum gates are the basic unitary operations that change the state of a single qubit. The most commonly used quantum gate is the Hadamard gate, which creates a superposition of states.

The Hadamard gate is represented as:

$$
H = \frac{1}{\sqrt{2}}\begin{bmatrix}
1 & 1 \\
1 & -1
\end{bmatrix}
$$

When applied to the state \( |0\rangle \), it yields the superposition state \( \frac{|0\rangle + |1\rangle}{\sqrt{2}} \), which corresponds to the \( |+\rangle \) state on the Bloch sphere.



