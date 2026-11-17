# Constant Failure Rate Models

This lecture covers two main topics:

- The exponential reliability function or Constant Failure Rate (CFR) model.
- The 2-parameter exponential reliability function.

Below is a summary of the key formulas that you may find useful when solving homework assignments and exam problems.

# The **Constant Failure Rate (CFR) Model**

- Failures due to random or chance events are well described by a constant failure rate model
- Items with no aging or wear-out.
- The rate at which the component fails is independent from its age (memoryless).

We can conclude that

$$
\lambda(t)=\lambda \implies \text{CFR Model}
$$

Thus,

$$
R(t) = e^{-\int_0^t\lambda(t')dt'} = e^{-\lambda t}, \qquad t \geq 0.
$$

$$
F(t) = 1-R(t) = 1-e^{-\lambda t}, \quad f(t) = -\frac{dR(t)}{dt} = \lambda e^{-\lambda t}.
$$

$$
MTTF = \frac{1}{\lambda} \to R(MTTF) = e^{-1} = 0.368; \quad \sigma^2 = \frac{1}{\lambda^2}.
$$

$$
t_{mode} = 0; \quad R(t_{med}) = e^{-\lambda (t_{med})} = 0.5 \to t_{med} = \frac{\ln0.5}{-\lambda}, \qquad t_R = \frac{\ln R}{-\lambda}.
$$

Where $t_R$ is the design life for a desired reliability $R$.

# **The 2-Parameter Exponential Reliability Function**

To be used if the component has a **“guaranteed lifetime”**,i.e., no failure will occur before a given time $t_0$.

- $t_0$: location parameter (does not affect variance and SD)
- $\lambda$: failure rate

$$
R(t) = e^{-\lambda (t-t_0)},\quad t\ge t_0.
$$

$$
MTTF = t_0 + \frac{1}{\lambda}, \quad \sigma^2 = \frac{1}{\lambda^2}.
$$

$$
t_{mode} = t_0, \quad t_{med} = t_0 + \frac{\ln 0.5}{- \lambda}, \quad t_R = t_0 + \frac{\ln R}{- \lambda}.
$$