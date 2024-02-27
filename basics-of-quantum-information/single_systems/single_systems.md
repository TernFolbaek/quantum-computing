# Single Systems in Quantum Information

The explanation of single systems within quantum information can be facilitated by our understanding of classical information to begin with. Therefore, the first section will focus on our understanding of systems within the classical "realm."

## Classical Information

### Classical States and Probability Vectors

Suppose that we have a system that stores information. More specifically, let's assume that this system can be in one of a finite number of classical states at each instant. Here, the term "classical state" should be understood in intuitive terms, as a configuration that can be recognized and described unambiguously.

The archetypal example, which we will come back to repeatedly, is that of a bit, which is a system whose classical states are `0` and `1`. Other examples include:

- A standard six-sided die, whose classical states are `1`, `2`, `3`, `4`, `5`, and `6`.
- A nucleobase in a strand of DNA, whose classical states are `A`, `C`, `G`, and `T`.
- A switch on an electric fan, whose classical states are (commonly) `high`, `medium`, `low`, and `off`.

In mathematical terms, we define a system and its classical states as follows:

- Let \( \Sigma \) be the set of classical states of a system \( X \).
- We assume \( \Sigma \) is finite and nonempty.

#### Examples:

- If \( X \) is a bit, then \( \Sigma = \{0, 1\} \).
- If \( X \) is a six-sided die, then \( \Sigma = \{1, 2, 3, 4, 5, 6\} \).
- If \( X \) is an electric fan switch, then \( \Sigma = \{\text{high}, \text{medium}, \text{low}, \text{off}\} \).

When thinking about \( X \) as a carrier of information, the different classical states of \( X \) could be assigned certain meanings, leading to different outcomes or consequences.

### Representing Uncertainty

Often in information processing, our knowledge of \( X \) is uncertain. We represent our knowledge of the classical state of \( X \) by assigning probabilities to each classical state, resulting in a probabilistic state. 

For example, suppose \( X \) is a bit. We might believe:

- \( Pr(X = 0) = \frac{3}{4} \)
- \( Pr(X = 1) = \frac{1}{4} \)

This can be succinctly represented by a column vector:

\[ \begin{pmatrix} \frac{3}{4} \\ \frac{1}{4} \end{pmatrix} \]

Where the probability of the bit being `0` is at the top, and the probability of it being `1` is at the bottom.

#### Properties of Probability Vectors:

1. All entries are nonnegative real numbers.
2. The sum of the entries equals `1`.

This format allows for operations on probabilistic states to be represented through matrix–vector multiplication, facilitating calculations and analysis.
