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
Pr(X = a) = \Sigma 
$$

## Quantum Information

### Quantum States

### Measurements on Quantum States

### Unitary Operations
