# Information in multiple systems

## Classical Information

#### As in the section for single systems, we will begin with our understanding of multiple systems within classical information, thereafter expanding onto the quantum realm.

### Classical states via the Cartesian product

We can describe the classical states of systems via the Cartesian product. We will begin by formalizing the notation with two systems, for simplicities sake, thereafter with n-amount of systems. Let us discuss this notation with system $X$ and system $Y$, where system X has a classical state set $\Sigma$, and system Y with a classical state set $\Gamma$. We can denote the joint system of $X$ and $Y$ as $(X,Y)$ or simply $XY$.

To describe the joint states of these two systems, we will be using the $Cartesian$ $product$ of both systems.

$$
\Sigma x \Gamma = {(a,b) : a \in \Sigma and b \in \Gamma}
$$

### Probabilistic states

If we were to work further with the states of our two bits $XY$, we can then setup the following probabilistic states:

$$
P((X,Y) = (0,0)) = \frac{1}{2}
$$

$$
P((X,Y) = (0,1)) = 0
$$

$$
P((X,Y) = (1,0)) = 0
$$

$$
P((X,Y) = (1,1)) = \frac{1}{2}
$$

The above states show that there is an equal probability of both systems being in state 0 and state 1. This is an example of _correlation_ between these systems. Probabilistic states of systems are represented by probability vectors, which are column vectors having indices that have been placed in correspondence with the underlying classical state set of the system being considered. As aforementioned when we have to do with the cartesian product of two sets, the rank of importance runs from left to right, fx. given set ${(1,2,3)}$ & ${(0,1)}$ would be ordered as follows:

$$
(1,0), (1,1), (2,0), (2,1), (3,0), (3,1)
$$

To work further on our probabilistic states, I will label each entry to clarify further:

$$
\mathbf{p} = \begin{bmatrix}
\frac{1}{2}, \mathbf{entry}\ 00 \\
0, \mathbf{entry}\ 01 \\
0, \mathbf{entry}\ 10 \\
\frac{1}{2}, \mathbf{entry}\ 11
\end{bmatrix}
$$

### Measurements of probabilistic states

When we choose to view multiple systems as a single system, as we did above with our $(X,Y)$ system, we immediately receive on the specifications on how to obtain the measurements of multiple systems. For example is the multiple system $(X,Y)$ that is described as follows:

$$
\frac{1}{2} \left( |00\rangle + |11\rangle \right)
$$

Reading this above as a single system simplifies the process, as we can see that the probability that $X$ is in state 0 simultaneously with $Y$ being in state 0 is $\frac{1}{2}$ and the probability that $X$ is in state 1 whilst $Y$ is in state 1 is also $\frac{1}{2}$.

#### Partial Measurements

We can decide not to measure the state of all systems but only a proper _subset_ of the systems. Where we will focus on two systems where we measure only the one. We will continue with our two systems $(X,Y)$, both systems having classical state sets, $\Sigma$ and $\Gamma$ where we decide to only measure the state of system X. We know that the probability of observing system $X$ in state $a$, must still align with the assumption that Y is also being measured:

$$
Pr(X = a) = \sum_{b \in \Gamma} Pr((X, Y) = (a, b)).
$$

This is the formula for the so-called reduced (or marginal) probabilistic state of $X$ alone. If we for example want to measure the probability of $X$ being in state 0, then we will then accumulate all the probabilities where the state of X is present, which is state 00 and state 01. Which is what the above formula describes. If we then want to find the probability that system $Y$ will be in a specific state b given that system $X$ is in state a, we will then use below formula:

$$
Pr(Y = b | X = a) = \frac{Pr((X, Y) = (a, b))}{Pr(X = a)}
$$

In a classical system, consider two variables $X$ and $Y$. Each can take on values of 0 or 1. We have a joint probability distribution indicating the likelihood of each combination of states for $X$ and $Y$:

- $Pr((X, Y) = (0, 0)) = 0.25$
- $Pr((X, Y) = (1, 1)) = 0.25$
- $Pr((X, Y) = (0, 1)) = 0.25$
- $Pr((X, Y) = (1, 0)) = 0.25$

To find the marginal probability of $X$ being in a specific state (say $X = 0$), we can use the formula:

$Pr(X = 0) = \sum_{b \in \{0, 1\}} Pr((X, Y) = (0, b))$

This means we sum the probabilities where $X$ is 0 and $Y$ takes on all possible values:

$Pr(X = 0) = Pr((X, Y) = (0, 0)) + Pr((X, Y) = (0, 1)) = 0.25 + 0.25 = 0.5$

Similarly, for $X = 1$:

$Pr(X = 1) = \sum_{b \in \{0, 1\}} Pr((X, Y) = (1, b))$
$Pr(X = 1) = Pr((X, Y) = (1, 0)) + Pr((X, Y) = (1, 1)) = 0.25 + 0.25 = 0.5$

These probabilities give us the marginal distributions for $X$ without consideration of the specific state of $Y$.

The conditional probability of $Y$ being in a specific state $b$, given $X$ is in state $a$, is calculated using the formula:

$Pr(Y = b | X = a) = \frac{Pr((X, Y) = (a, b))}{Pr(X = a)}$

So for our example, to calculate $Pr(Y = 0 | X = 0)$, we would use:

$Pr(Y = 0 | X = 0) = \frac{Pr((X, Y) = (0, 0))}{Pr(X = 0)} = \frac{0.25}{0.5} = 0.5$

### Operations on probabilistic states

When dealing with multiple classical systems in probabilistic states, we can treat them as single, compound systems. Operations on these systems are represented by stochastic matrices, indexed by the Cartesian product of the individual state spaces.

### Controlled-NOT Operation

For two bits, $X$ and $Y$, a controlled-NOT operation can be described as:

- If $X=1$, apply a NOT operation on $Y$.
- If $X=0$, do nothing.

Matrix representation:

$$
\begin{bmatrix}
1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
0 & 0 & 0 & 1 \\
0 & 0 & 1 & 0
\end{bmatrix}
$$

Its action on standard basis states:

$$
|00\rangle \mapsto |00\rangle \\
|01\rangle \mapsto |01\rangle \\
|10\rangle \mapsto |11\rangle \\
|11\rangle \mapsto |10\rangle
$$

## Probabilistic Operations

Consider a probabilistic operation where:

- With probability $1/2$, set $Y$ to be equal to $X$.
- With probability $1/2$, set $X$ to be equal to $Y$.

Matrix representation:

$$
\frac{1}{2} \left(
\begin{bmatrix}
1 & 0 \\
0 & 1
\end{bmatrix}
+
\begin{bmatrix}
1 & 1 \\
0 & 0
\end{bmatrix}
\right)
$$

The action of this operation on standard basis vectors:

$$
|00\rangle \mapsto |00\rangle
$$

$$
|01\rangle \mapsto \frac{1}{2} |00\rangle + \frac{1}{2} |11\rangle
$$

$$
|10\rangle \mapsto \frac{1}{2} |00\rangle + \frac{1}{2} |11\rangle
$$

$$
|11\rangle \mapsto |11\rangle
$$

### Tensor Products of Matrices

The tensor product of matrices $M$ and $N$ is denoted as $M \otimes N$. If $M$ represents an operation on $X$, and $N$ represents an operation on $Y$, the combined operation on the compound system $(X, Y)$ is the tensor product $M \otimes N$.

Example of tensor product:

$$
\begin{bmatrix}
a & b \\
c & d
\end{bmatrix}
\otimes
\begin{bmatrix}
e & f \\
g & h
\end{bmatrix}
\mathbf{=}
\begin{bmatrix}
ae & af & be & bf \\
ag & ah & bg & bh \\
ce & cf & de & df \\
cg & ch & dg & dh
\end{bmatrix}
$$

### Independent Operations

If $M$ is a probabilistic operation on $X$, and $N$ is a probabilistic operation on $Y$, performed independently, the operation on $(X,Y)$ is $M \otimes N$.

- The tensor product of stochastic matrices is always stochastic.
- The tensor product represents independent operations on a compound system.

#### Example

For a bit reset operation on $X$ and doing nothing on $Y$:

Matrix for $X$ (reset to 0):

$$
\begin{bmatrix}
1 & 0 \\
1 & 0
\end{bmatrix}
$$

Identity matrix for $Y$:

$$
\begin{bmatrix}
1 & 0 \\
0 & 1
\end{bmatrix}
$$

The joint operation:

$$
\begin{bmatrix}
1 & 0 \\
1 & 0
\end{bmatrix}
\otimes
\begin{bmatrix}
1 & 0 \\
0 & 1
\end{bmatrix}
\mathbf{=}
\begin{bmatrix}
1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0
\end{bmatrix}
$$

This summarizes the operations on probabilistic states for multiple systems in classical information.

## Quantum Information

### Quantum States

In the quantum domain, similar to the classical probabilistic case, multiple systems can be considered as a single, compound system. The quantum states of multiple systems are described by column vectors with complex number entries and a Euclidean norm of 1, just like quantum states of single systems.



For instance, if \(X\) and \(Y\) are qubits, the classical state set of the pair $(X, Y)$, viewed collectively, is the Cartesian product $\{0, 1\} \times \{0, 1\}$. Representing pairs of binary values as strings, we associate this set with $\{00, 01, 10, 11\}$. The vectors below are examples of quantum state vectors of the pair $(X, Y)$:

- $\frac{1}{\sqrt{2}} |00\rangle - \frac{1}{6} |01\rangle + \frac{i}{6} |10\rangle + \frac{1}{6} |11\rangle$
- $\frac{3}{5} |00\rangle - \frac{4}{5} |11\rangle$
- $|01\rangle$

These states can be expressed in various forms, including using tensor products:

$$
\frac{1}{\sqrt{2}} |0\rangle \otimes |0\rangle - \frac{1}{6} |0\rangle \otimes |1\rangle + \frac{i}{6} |1\rangle \otimes |0\rangle + \frac{1}{6} |1\rangle \otimes |1\rangle
$$

And as column vectors:

$$
\begin{pmatrix}
\frac{1}{\sqrt{2}} \\
-\frac{1}{6} \\
\frac{i}{6} \\
\frac{1}{6}
\end{pmatrix}
$$

## Tensor Products of Quantum State Vectors

The tensor product of state vectors represents the independence of quantum systems. If $|ϕ\rangle$ is a quantum state vector of system $X$ and $|ψ\rangle$ is for system $Y$, the joint system $(X, Y)$ is in the state $|ϕ\rangle \otimes |ψ\rangle$.

### Entangled States

Not all states are separable product states. An entangled state, like

$$
\frac{1}{\sqrt{2}}|00\rangle + \frac{1}{\sqrt{2}}|11\rangle
$$

cannot be factored into individual states of the system $X$ and $Y$, signifying a quantum correlation between them.

## Bell States

Bell states are quintessential examples of entangled states for two qubits:

$$
|\phi^+\rangle = \frac{1}{\sqrt{2}}(|00\rangle + |11\rangle)
$$
$$
|\phi^-\rangle = \frac{1}{\sqrt{2}}(|00\rangle - |11\rangle)
$$
$$
|\psi^+\rangle = \frac{1}{\sqrt{2}}(|01\rangle + |10\rangle)
$$
$$
|\psi^-\rangle = \frac{1}{\sqrt{2}}(|01\rangle - |10\rangle)
$$

Each Bell state cannot be written as a product of two separate state vectors, indicating entanglement.

## GHZ and W States

Examples of multi-qubit entangled states include the GHZ and W states for three qubits:

The GHZ state:

$$
\frac{1}{\sqrt{2}}(|000\rangle + |111\rangle)
$$

The W state:

$$
\frac{1}{\sqrt{3}}(|001\rangle + |010\rangle + |100\rangle)
$$

Both states are entangled, indicating they cannot be decomposed into a tensor product of individual qubit states.

This introduction sets the stage for a deeper exploration into the fascinating realm of quantum information and entanglement.


## Measurements on Quantum States


In quantum mechanics, the measurement process is crucial for understanding the state of a system. Here we will explore standard basis measurements of single and multiple quantum systems.

### Standard Basis Measurements

For a single system with a classical state set $\Sigma$, a quantum state represented by the vector $|\psi\rangle$, yields measurement outcomes in $\Sigma$ with probabilities given by the squared magnitudes of the vector's components:

$$
P(a \in \Sigma) = |\langle a | \psi \rangle|^2
$$

### Measurements in Multiple Systems

Considering multiple systems $X_1, \ldots, X_n$ with classical state sets $\Sigma_1, \ldots, \Sigma_n$, the collective system can be viewed as one with a classical state set as the Cartesian product $\Sigma_1 \times \cdots \times \Sigma_n$. For a quantum state $|\psi\rangle$ of this compound system, the probability of each outcome $(a_1, \ldots, a_n)$ appearing upon measurement is:

$$
P((a_1, \ldots, a_n)) = |\langle a_1 \cdots a_n | \psi \rangle|^2
$$

### Example

For systems $X$ and $Y$ in the state:

$$
\frac{3}{5} |0\rangle | \heartsuit \rangle - \frac{4i}{5} |1\rangle | \spadesuit \rangle
$$

the outcomes $(0, \heartsuit)$ and $(1, \spadesuit)$ appear with probabilities $\frac{9}{25}$ and $\frac{16}{25}$, respectively.

## Partial Measurements

For partial measurements involving only a subset of systems, the probability for a particular outcome $a \in \Sigma$ when measuring system $X$ is:

$$
P(a) = \sum_{b \in \Gamma} |\langle a b | \psi \rangle|^2
$$

Upon measuring $X$ and obtaining $a$, the post-measurement state vector $|\phi_a\rangle$ for the remaining system(s) is:

$$
|\phi_a\rangle = \sum_{b \in \Gamma} \alpha_{ab} |b\rangle
$$

normalized to unit length. This new state $|\phi_a\rangle$ is then scaled by its Euclidean norm which gives the updated state for the unmeasured systems.

### Example with GHZ and W States

Consider the GHZ state:

$$
\frac{1}{\sqrt{2}} (|000\rangle + |111\rangle)
$$

Measuring the first qubit in the state $|0\rangle$ or $|1\rangle$ leaves the remaining qubits in a correlated state $|00\rangle$ or $|11\rangle$, respectively.

For the W state:

$$
\frac{1}{\sqrt{3}} (|001\rangle + |010\rangle + |100\rangle)
$$

measuring the first qubit and finding it in state $|0\rangle$ results in the remaining qubits being in the state:

$$
\frac{1}{\sqrt{2}} (|01\rangle + |10\rangle)
$$

which can also be expressed as $|0\rangle | \psi^+ \rangle$ where $| \psi^+ \rangle$ is a Bell state.

## Unitary Operations on Quantum Systems

Unitary operations are fundamental to quantum mechanics as they describe the evolution of quantum states without any loss of information.

### Unitary Operations Overview

Unitary operations on multiple systems can be represented by unitary matrices acting on the state vector of the combined system. For a system $X$ with state set $\Sigma$ and system $Y$ with state set $\Gamma$, the state set of the joint system $(X,Y)$ is $\Sigma \times \Gamma$. Thus, operations on $(X,Y)$ correspond to unitary matrices with rows and columns indexed by $\Sigma \times \Gamma$.

### Example of a Unitary Matrix

Suppose $\Sigma = \{1, 2, 3\}$ and $\Gamma = \{0, 1\}$. The Cartesian product $\Sigma \times \Gamma$ has the order $(1,0), (1,1), (2,0), (2,1), (3,0), (3,1)$. A unitary matrix $U$ representing an operation on $(X,Y)$ could be:

$$
U = \left(
\begin{array}{cccc}
\frac{1}{\sqrt{2}} & \frac{1}{\sqrt{2}} & 0 & 0 \\
\frac{1}{\sqrt{2}} & -\frac{1}{\sqrt{2}} & 0 & 0 \\
0 & 0 & \frac{1}{\sqrt{2}} & \frac{1}{\sqrt{2}} \\
0 & 0 & \frac{1}{\sqrt{2}} & -\frac{1}{\sqrt{2}}
\end{array}
\right)
$$

### Controlled Operations

Controlled operations are a type of unitary operation where the action on one subsystem depends on the state of another. The controlled NOT (CNOT) operation is a common example used in quantum computing.

## #Swap Operation

The swap operation exchanges the state of two systems. For systems with state set $\Sigma$, the operation for states $a, b \in \Sigma$ is:

$$
\text{SWAP} |a\rangle |b\rangle = |b\rangle |a\rangle
$$

### Controlled-Unitary Operations

For a qubit system $Q$ and a system $R$ with unitary operation $U$, the controlled-$U$ operation on $(Q, R)$ is defined as:

$$
CU = |0\rangle \langle 0| \otimes I + |1\rangle \langle 1| \otimes U
$$

For example, with $R$ as a qubit and $U$ as a Pauli-X operation, the controlled-$U$ operation (CNOT) is:

$$
CNOT = |0\rangle \langle 0| \otimes I + |1\rangle \langle 1| \otimes X
$$

### Toffoli Gate

The Toffoli gate, a universal quantum gate, applies a NOT to one qubit conditional on the state of two other qubits.

$$
CCX = |00\rangle \langle 00| \otimes I + |01\rangle \langle 01| \otimes I + |10\rangle \langle 10| \otimes I + |11\rangle \langle 11| \otimes X
$$

This is a simplified introduction to unitary operations on quantum systems. Such operations are key to manipulating quantum information and realizing quantum algorithms.

