## Classical Information

To delve into the essence of quantum information, it's instructive to first explore the realm of classical information. While the domains of quantum and classical information diverge in several remarkable aspects, their mathematical frameworks bear a striking resemblance.

Classical information not only provides a relatable baseline for quantum studies but also offers a rich reservoir of analogies that significantly enhance our understanding of quantum phenomena. It's often the case that queries about quantum information find their parallels in classical contexts, where the answers are straightforward yet profoundly illuminating. Indeed, a thorough grasp of classical information is pivotal for truly comprehending quantum information.

This section is designed to cater to both novices and those with a prior acquaintance with classical information. Our aim is to shed light on the facets of classical information that are pivotal for an introductory foray into quantum information, alongside introducing the Dirac notation. This notation, predominantly associated with quantum contexts, is equally applicable to classical information and other scenarios involving vectors and matrices.

### Classical States and Probability Vectors

Imagine a system engineered to store information, capable of existing in a discrete set of classical states at any given moment. Here, a 'classical state' can be intuitively understood as a distinct configuration of the system that can be unequivocally identified and described.

A quintessential example is the binary system or 'bit', characterized by two classical states: 0 and 1. Other instances include a six-sided die with states ranging from 1 to 6, a nucleobase in DNA represented by A, C, G, or T, and the settings of an electric fan, typically high, medium, low, and off. Mathematically, the definition of a system's classical states is foundational; for instance, a bit is defined by its two states, 0 and 1.

Let's denote our system of interest as $\( \mathcal{X} \)$ and its set of classical states as $\( \Sigma \)$. It's assumed that $\( \Sigma \)$ is both finite and non-empty, as a system devoid of states is conceptually void. Although considering systems with an infinite array of states is viable, our discussion will be confined to those with a finite state set for simplicity.

Here are a few illustrative examples:

- For a bit $\( \mathcal{X} \), \( \Sigma = \{0, 1\} \)$, often referred to as the binary alphabet.
- For a six-sided die $\( \mathcal{X} \), \( \Sigma = \{1, 2, 3, 4, 5, 6\} \)$.
- For an electric fan switch $\( \mathcal{X} \), \( \Sigma = \{\text{high, medium, low, off}\} \)$.

When $\( \mathcal{X} \)$ is viewed as an information carrier, the distinct classical states can embody specific meanings, leading to varied outcomes. For example, knowing with certainty that an electric fan switch is set to 'high' is a direct state identification. However, our knowledge about $\( \mathcal{X} \)$'s state is often probabilistic rather than deterministic. This uncertainty is expressed by assigning probabilities to each classical state, forming a probabilistic state.

Consider $\( \mathcal{X} \)$ as a bit. Based on prior information or expectations, we might believe there's a $\( \frac{3}{4} \)$ chance of $\( \mathcal{X} \)$ being in state 0 and a $\( \frac{1}{4} \)$ chance of being in state 1. This belief can be succinctly represented as a probability vector:

$$
\begin{pmatrix}
\frac{3}{4} \\
\frac{1}{4} \\
\end{pmatrix}
$$

In this vector, the top entry signifies the probability of $\( \mathcal{X} \)$ being in state 0, and the bottom entry the probability of state 1, adhering to conventional ordering.

In general, the probabilistic state of any system with a defined set of classical states can be depicted similarly, as a vector of probabilities. The ordering of these probabilities is usually determined by the natural or default ordering of the classical states in question. To qualify as a probability vector, a column vector must satisfy two criteria:

1. All vector entries must be non-negative real numbers.
2. The sum of the vector entries must equal 1.

Thus, any column vector meeting these conditions can represent a probabilistic state, and such vectors are hereafter referred to as probability vectors. This notation's brevity and precision are advantageous, and when paired with matrix-vector multiplication, it elegantly facilitates operations on probabilistic states, a topic we'll explore further.
