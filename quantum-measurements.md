Measuring quantum states changes them, so when we measure a s.

Suppose we have a two-quibit state $|\phi\rangle = a | 00\rangle + b | 01 \rangle + c | 10\rangle + d | 11 \rangle$, and we want to figure out the probability that the _parity_ of $\phi \rangle$ is $0$, ie. if the modulo two sum of the bits is zero or one. For this to be the case, the two qubits must be either $|00\rangle>$ or $|11\rangle$.

The measurement then entails projecting $|\phi>$ into the ${|00\rangle, |11\rangle>$ subspace and computing the squared norm of the result:
$$
  \begin{bmatrix} |00 \rangle // |11\rangle \end{bmatrix}^T |\phi \rangle = a | 00\rangle + d | 11 \rangle
$$
since all the subspaces are orthogonal. The squared norm of this vector is then $|a|^2 + |d|^2$.
To compute the post-measurement state, 
