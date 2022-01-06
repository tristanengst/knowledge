## REINFORCE
We can estimate $\frac{\partial}{\partial \theta} \mathbb{E}_{p(b | \theta)} f(b)$ as
$$
  \frac{\partial}{\partial \theta} \mathbb{E}_{p(b | \theta)} f(b) = \int p(b | \theta) f(b) \partial \theta = \mathbb{E}_{p(b | \theta)} [f(b) \frac{\partial}{\partial \theta} \log p(b | \theta)]
$$
