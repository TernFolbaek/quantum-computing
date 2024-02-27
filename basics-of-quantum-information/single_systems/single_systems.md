# Classical Information

To describe quantum information and how it works, we will begin with an overview of classical information. Despite the focus on quantum information, understanding classical information is crucial due to their mathematical similarities and the foundational role classical concepts play in understanding quantum phenomena.

Classical information serves as a familiar point of reference and a source of analogy for quantum information. It's often the case that questions about quantum information find their analogs in classical contexts, providing clarity and insight.

Understanding classical information is essential for grasping the nuances of quantum information. This section not only highlights key aspects of classical information relevant to quantum studies but also introduces the Dirac notation, a versatile tool used across various domains, including quantum information, to describe vectors and matrices.

## Classical States and Probability Vectors

Imagine a system designed to store information, capable of existing in one of several distinct classical states at any given moment. A "classical state" refers to a clearly identifiable and describable configuration of the system.

### Examples

- **Bit**: The fundamental example with two classical states, `0` and `1`.
- **Six-sided Die**: With classical states numbered `1` through `6`.
- **Nucleobase in DNA**: With classical states `A`, `C`, `G`, and `T`.
- **Electric Fan Switch**: Commonly having states such as `high`, `medium`, `low`, and `off`.

In mathematical terms, we define these systems based on their classical states. For instance, a bit is defined by its two possible states, `0` and `1`.

Let's denote our system of interest as `X` and the set of its classical states as `Σ`. We assume `Σ` is finite and nonempty, focusing on systems with a limited number of states for simplicity.

### Representing Uncertainty with Probability Vectors

Often, our knowledge about the system's exact state is uncertain. We express this uncertainty by assigning probabilities to each possible state, forming a probabilistic state representation.

For example, for a bit `X`, we might believe:

- `Pr(X = 0) = 3/4`
- `Pr(X = 1) = 1/4`

This probabilistic state can be neatly represented as a column vector using LaTeX in a Markdown document:

```latex
\begin{pmatrix}
3/4 \\
1/4 \\
\end{pmatrix}
```
Here, the probability of X being in state 0 is listed first, followed by the probability of it being in state 1, adhering to the conventional ordering.

Properties of Probability Vectors
All vector entries are nonnegative real numbers.
The sum of the entries equals 1.
This approach of using column vectors not only provides a succinct notation but also facilitates the use of matrix-vector multiplication to represent operations on probabilistic states, which we will explore further.