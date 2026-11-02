# The Failure Process

This lecture introduces the probability functions used to describe the failure process. The following table summarises these functions and their key properties. You should understand how to use them in calculations and how they are mathematically related to one another.

# **The unreliability function** $F(t)$

The unreliability function (or cumulative distribution function) $F(t)$ is the probability that a component will fail prior to time $t$.

$$
F(t) = P\{T<t\} = \int_0^t f(t')dt'.
$$

# **Reliability function $R(t)$**

The reliability function (or survival function) $R(t)$ is the probablity that a component will function for a given time period $t$.

$$
R(t)=p\{T \ge t\} = \int_t^\infty f(t')dt'.
$$

- Reliability function is the complementary to the unreliability function, thus, $R(t)= 1-F(t)$.
- Reliability function has such properties:
    
    $$
    0 \leq R(T) \leq 1, \qquad R(0)=0, \qquad \lim_{t \to \infty} R(t)=1.
    $$
    
- Reliability function is <u>one of the most important function</u> in this course.

# **Probability density function $f(t)$**

The probability density function $f(t)$ describes the shape of the failure times distribution.

$$
f(t) = \frac{dF(t)}{dt} = - \frac{dR(t)}{dt}.
$$

# **Hazard rate function $\lambda(t)$**

The hazard rate function (or failure rate function) at time $t$ is the **conditional probability** that a component will fail in the time interval $[t, t+ dt]$ when $dt \to 0$, given that it is still functioning at time $t$.

$$
\lambda(t)dt = P\{t\le T \le t+dt | T \ge t \} = \frac{R(t)-R(t+dt)}{R(t)}.
$$

$$
\lambda(t) = -\frac{dR(t)}{dt} \times \frac{1}{R(t)} = \frac{f(t)}{R(t)} = \frac{f(t)}{1-F(t)}.
$$

<aside>
💡

### **Probability density function (PDF) vs Hazard rate function:**

- The PDF tells us when failures tend to occur across the population. It is unconditional, and describes “<u>how densely</u> failure times are distributed around $t$”.
- The hazard rate tells us <u>how risky it is</u> for a component that has survived until now <u>to fail next</u>. It is conditional on survival until $t$, and is an instantaneous failure risk.
</aside>

# Other failure rates:

- **The Cumulative Failure Rates (CFR)**
    
    $$
    L(t) = \int_0^t\lambda(t')dt' = -\ln R(t) \implies R(t)= e^{-L(t)} = e^{-\int_0^t\lambda(t')dt}.
    $$
    
- **The Average Failure Rates (AFR)**
    
    $$
    AFR(t_1,t_2) = \frac{1}{t_2-t_1}\int_{t_1}^{t_2}\lambda(t')dt' = \frac{\ln R(t_1)-\ln R(t_2)}{t_2-t_1}.
    $$
    
    - If $t_1 = 0$ and $t_2 = t$, then $AFR(t) = \frac{L(t)}{t} = -\frac{\ln R(t)}{t}$.
    - AFR nondecreasing → Increasing Failure Rate Average (IFRA);
        
        AFR non-increasing → Decreasing Failure Rate Average (DFRA).
        
- What is the **design life** for a 0.95 reliability? → $R(t_R) = 0.95$ → solve the equation.