# Math Fundamentals

### Complex Hilbert Space
Notes distilled from [this Quantiki artile](https://www.quantiki.org/wiki/hilbert-spaces).

Every inner product $\langle \cdot, \cdot \rangle$ on a real or complex vector space gives rise to a norm defined as
$$
  ||x|| = \sqrt{\langle x, x\rangle}
$$
A vector space $H$ is a **Hilbert space** if it is complete with respect to this norm.

### Groups, Rings, and Fields
A great resource [is this PDF](https://www-users.cse.umn.edu/~brubaker/docs/152/152groups.pdf).
**Groups** are described by a set $G$ and a binary operation $G\times G \rightarrow G$ that is _associative_, has an _identity_, and has an _inverse_. Note that by definition this operation is closed.

**Rings** are described by a set $R$ and binary operations $ + : R\times R \rightarrow R$ and $\cdot : \times R \rightarrow R$hat satisfy the following _ring axioms_:
  1. $R$ is an Abelian group, meaning that $+$ is associative, commutative, there exists an additive identity, and an additive inverse in $R$.
  2. $R$ is a monoid under multiplication, meaning that $\cdot$ is associative and there exists in $R$ a multiplicative identity.
  3. Multiplication is distributive with respect to addition, meaning that $a\cdot (b+c) = (a\cdot b) + (a\cdot c)$ and $(b+c)\cdot a = (b\cdot a) + (c\cdot a)$
Note that (1) means that all rings are groups.

**Fields** are a set on which addition, subtraction, multiplication, and division are defined and behave as the corresponding operations on rational and real numbers do. More formally, a field is a set $F$ together with _addition_ and _multiplication_, to binary operations of the form $F\times F \rightarrow F$. These functions must satisfy
  1. $F$ is an Abelian group under $(+)$ (ie. it is a group)
  2. $F - \{0\}$ (ie. $F$ without the additive identity) is an Abelian group under $\cdot$. Note that this means that for $a,b,c \in F$, $a\cdot b = c$ implies some $b^{-1} \in F$ such that $c\cdot b^{-1}=a$—a multiplicative inverse—_and_ that multiplication is associative and has an identity. This, with (1) means that all fields are rings!
_Note: a "vector field" violates a ton of these properties and isn't a proper field!_

When we have a "vector space $V$ over a field", we mean the following: consider the quadruple $(V, K, +, \cdot)$ where $V$ is a set of vectors, $K$ is a field, and $+: V\times V \rightarrow V$ and $\cdot : K \times V \rightarrow V$ satisfy properties to make the quadruple a _vector space_. 

### Dirac Bra-Ket Notation
**Linear Maps**: For vector spaces $V$ and $W$over the same field $K$, a function $f : V \rightarrow W$ is a linear map if for all $u,v \in V$ and $c \in K$ if $f(u+v)=f(u) + f(v)$ and $cf(u) = f(cu)$.

**Dual Space**: Given any vector space $V$ over field $F$, the algebraic dual space $V'$ is defined as the set of all linear maps (aka linear functionals) $\varphi : V \rightarrow F$.

**Conjugate Transpose**: Suppose we have an $m\times n$ matrix $A$ with complex entries. The conjugate transpose $A^\dagger$ of $A$ is found by first transposing $A$, and then taking every complex element $a+ib$ and replacing it with its conjugate $a-ib$.

Now we can actually discuss _bra-kets_!
  - A _ket_ is a vector $|v \rangle$ defined as $a|0\rangle + b|1\rangle = \begin{pmatrix}a \\ b\end{pmatrix}$ where $|0\rangle$ and $|1\rangle$ are analogous to $\vec{e}_1$ and $\vec{e}_2$. Here, $v$ is is just a symbol, and we can write others, eg. axes to represent photon polarizations.
  - A _bra_ is the conjugate transpose $|v\rangle^\dagger$ of a _ket_ vector $|v\rangle$, so $\langle v| = |v\rangle^\dagger = a\langle 0| + b \langle 1| = (a^*,b^*)$

The **inner product** of a _bra_ vector and a _ket_ vector is written as $\langle v| w \rangle = (a^*, b^*)\begin{pmatrix}c \\ d\end{pmatrix} = a^* c + b^* d$ 
 
 **Tensor products and compound systems**:
 - Given vectors $\vec{v}$ and $\vec{w}$, the tensor product $\vec{v}\otimes\vec{w}=\vec{v}\vec{w}^\top$ is (an abstraction of) their outer product. It is an element of the space of all tensors that can be built from vectors in the vectors' respective vector spaces.
 - Suppose we have two systems  $V$ and $W$ of dimensions $k_1$ and $k_2$. Their joint system is described by $V\otimes W$ which has dimension $k_1k_2$.
  - If $V$ and $W$ have bases $|e_i \rangle$ and $|f_j\rangle$, a formal basis for $V\otimes W$ is $|e_i\rangle \otimes |f_j\rangle$. Suppose $|v\rangle$ and   $|w\rangle$ are states in $V$ and $W$, such that
    $$
      |v\rangle = \sum_{i=1}^{k_1} v_i |e_i\rangle
    $$
    and similarly for $|w\rangle$. Then
    $$
      |v\rangle \otimes |w\rangle = \sum_{i=1}^{k_1}\sum_{j=1}^{k_2} v_iw_j |e_i \rangle \otimes |f_j\rangle
    $$
    - $(|v\rangle, |w\rangle) \rightarrow |v\rangle \otimes |w\rangle$ is a bilinear embedding of the form $V\times W \rightarrow V \otimes W$
    - The state space of an $n$-qubit system is $\otimes_n \mathbb{C}^2$ which is asymptotically equal to $\mathbb{C}^{2^n}$, and has basis $|b_1 \rangle \otimes \dots \otimes |b_n\rangle$ which is asymptotically equal to $|\vec{b}\rangle$ with $\vec{b}\in \{0,1\}^n$

# Quantum Systems
- **Qubits**
  - A qubit is represented by a unit vector $|\psi \rangle = a|0\rangle + b|1\rangle \in \mathbb{C}^2$
  - It can exist in a superposition of $0$ and $1$
- **Quantum measurements and Transformations**
  - States of a system describe its properties, and multuiple qubits can exist in entanglement
  - Measurements of quantum systems are _inherently probabilistic_, _cause state to collapse_ (destroy information), _exhibit incompatibility_, are modelled by _projection operators_
  -   
