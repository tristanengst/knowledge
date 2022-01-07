## REINFORCE
We can estimate $\frac{\partial}{\partial \theta} \mathbb{E}_{p(b | \theta)} f(b)$ as
$$
  \frac{\partial}{\partial \theta} \mathbb{E}_{p(b | \theta)} f(b) = \int p(b | \theta) f(b) \partial \theta = \mathbb{E}_{p(b | \theta)} [f(b) \frac{\partial}{\partial \theta} \log p(b | \theta)]
$$
using the log-derivative trick.

### Log Derivative Trick
Note that
$$
  \nabla_\theta \log f(\theta) = \frac{1}{f(\theta)} \nabla_\theta f(\theta)
$$
and we can rearrange this to
$$
  f(\theta) \nabla_\theta \log f(\theta) = \nabla_\theta f(\theta)
$$
