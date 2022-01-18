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
  2. $F - \{0\}$ (ie. $F$ without the additive identity) is an Abelian group under $\cdot$. Note that this means that for $a,b,c \in F$, $a\cdot b = c$ implies some $b^{-1} \in F$ such that $c\cdot b^{-1}=a$---a multiplicative inverse---_and_ that multiplication is associative and has an identity. This, with (1) means that all fields are rings!
_Note: a "vector field" violates a ton of these properties and isn't a proper field! If _

We can have a "vector space $V$ over a field" in the following way: 
### Dual Space


### Dirac Bra-Ket Notation
 - A _bra_
 - A _ket_ is a vector $|v>$
