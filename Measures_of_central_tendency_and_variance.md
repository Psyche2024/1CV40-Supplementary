# Measures of Central Tendency and Variance

This lecture covers two main topics:

- **Measures of central tendency:** MTTF, median, mode, conditional reliability, and residual MTTF.
- **Measures of the dispersion of failure times around their mean:** variance

Below is a summary of the key formulas that you may find useful when solving homework assignments and exam problems.

- **The Mean Time To Failure (MTTF):** the <u>expected value</u> of the failure time distribution defined by $f(t)$.
    
    $$
    MTTF = E(T) = \int_0^\infty tf(t)dt = \int_0^\infty R(t)dt.
    $$
    
- **Median time to failure $t_{med}$:** the <u>time</u> at which the reliability is 0.5.
    
    $$
    R(t_{med}) = P\{T \ge t_{med}\} = 0.5 \implies \text{solve the equation.}
    $$
    
- **Mode $t_{mode}$:** the most likely observed failure <u>time</u>.
    
    $$
    f(t_{mode}) = \max_{0 \le t \le \infty} f(t) \implies t_{mode} = \arg \max_{0 \leq t\leq \infty} f(t).
    $$
    
- **The variance of the $f(t)$:** measure the <u>variability</u> around the value of the MTTF.
    
    $$
    \sigma^2 = \int_0^\infty (t-MTTF)^2 f(t)dt = \int_0^\infty t^2f(t)dt -MTTF^2.
    $$
    
- **Conditional <u>Reliability</u> $R(t|t_0)$:** the <u>probability</u> that an item of age $T_0$ will operate for an additional time $t$.
    
    $$
    R(t|T_0) = Pr\{T>T_0+t|T>T_0\} = \frac{R(T_0+t)}{R(T_0)} = e^{-\int_{T_0}^{T_0+t}\lambda(t')dt'}.
    $$
    
    - $T_0$ might be burn-in period, warranty period or simply the age of an item;
- **Residual MTTF (or Mean Residual Life):** the <u>expected value</u> of the remaining life of a component that it has already survived until time $t_0$.
    
    $$
    MTTF(t_0) = \int_0^\infty (t-t_0)f(t|t_0)dt = \int_0^\infty R(t|t_0)dt = \frac{1}{R(t_0)}\int_{t_0}^\infty R(t_0 + t)d(t_0+t).
    $$
    
    - The mean residual life of a component of age $t_0$.