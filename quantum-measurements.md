Measuring quantum systems changes them, so when we measure a probability that a quantum system is in some state, the system collapses to that state.

#### Example of a Complete Measurement
A _complete measurement_ is a measurement of an entire quantum system.

Suppose we have a two-quibit state $|\phi\rangle = a | 00\rangle + b | 01 \rangle + c | 10\rangle + d | 11 \rangle$, and we want to know the probability that the _parity_ of $\phi \rangle$ is $0$, ie. if the modulo two sum of the bits is zero or one. For this to be the case, the two qubits must be either $|00\rangle$ or $|11\rangle$.

The measurement then entails projecting $|\phi \rangle$ into the $|00\rangle, |11\rangle$ subspace and computing the squared norm of the result:
$$
  \begin{bmatrix} |00 \rangle \\ |11\rangle \end{bmatrix}^T |\phi \rangle = a | 00\rangle + d | 11 \rangle
$$
since all the subspaces are orthogonal. The squared norm of this vector is then $|a|^2 + |d|^2$.

To compute the post-measurement state, we recall that by measuring the two qubits, they've collapsed to the measurement—so in this sense we know what it is—but it needs to be renormalized to unit length:
$$
  |\phi \rangle' = \frac{a|00 \rangle + d |11 \rangle}{\sqrt{|a|^2 + |d|^2}}
$$

#### Measuring a Composite System
Suppose $|\psi \rangle \in V \otimes W$, and let $\mathcal{B} = \{|v_1 \rangle \dots |v_n \rangle \}$ be an orthonormal basis for $V$. Thus $|\psi \rangle = \sum_{i=1}^n |v_i \rangle | \xi_i \rangle$, where $| \xi_i \rangle \in W$ and are not necessarily normalized or orthogonal. How can we measure $|\psi \rangle$ with respect to the basis $\mathcal{B}$ of $V$?

The probability of the system being in state $i$ corresponding to some $|e_i \rangle \in V$ is then
$$
  P(i) = \langle \xi_i | \xi_ i \rangle = || \langle e_i | \psi \rangle ||_2^2
$$
and the post measurement state is $|\psi' \rangle = \frac{|e_i \rangle |\xi_i \rangle}{\sqrt{P(i)}$. Essentially, this is the original quantum system with the component from $V$ replaced with the measured state and the component from $W$ replaced with $|\xi_i \rangle$. 
