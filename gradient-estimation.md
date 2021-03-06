## REINFORCE
We can estimate $\frac{\partial}{\partial \theta} \mathbb{E}_{p(b | \theta)} f(b)$ as
$$
  \frac{\partial}{\partial \theta} \mathbb{E}_{p(b | \theta)} f(b) = \int \frac{\partial}{\partial \theta} p(b | \theta) f(b) \partial \theta = \mathbb{E}_{p(b | \theta)} [f(b) \frac{\partial}{\partial \theta} \log p(b | \theta)]
$$
using the log-derivative trick.

### Log Derivative Trick
Note that we can rearrange $\nabla_\theta \log f(\theta) = \frac{1}{f(\theta)} \nabla_\theta f(\theta)$ to $f(\theta) \nabla_\theta \log f(\theta) = \nabla_\theta f(\theta)$.
