## Use part one of the fundamental theorem of calculus to find the derivative of the function

$$
f(x) = \int^0_x\sqrt{5+\sec{8t}}\ dt
$$

This initially doesn't look like an equation that can use [[The Fundamental Theorem of Calculus#Fundamental Theorem of Calculus Part 1#Definition|FTC1]], as $x$ is on the lower side of the integral. But, using the properties of integrals:

$$
f(x) = \int^0_x\sqrt{5+\sec{8t}}\ dt = -\int^x_0\sqrt{5+\sec{8t}}\ dt
$$

Which now FTC1 can apply to
$$\begin{align}
f(t) = \sqrt{5+\sec{8t}} &&\text{f(t) is continuous}\\
\therefore f^\prime(x)=-\sqrt{5+\sec{8x}} &&\text{by FTC1}
\end{align}$$

## Evaluate the integral
$$
\int^1_0(u+3)(u-4)\ du
$$

$$\begin{align}
\int^1_0(u+3)(u-4)\ du&=\int^1_0u^2-u-12\ du\\
&=\int^1_0u^2\ du - \int^1_0u\ du-\int^1_012\ du\\
&={1\over3}-{1\over2}-12 &&\text{12 comes from c(b-a) where c = 12}\\

&=73/6

\end{align}$$
## Consider the following

$$f(x)=\int^4_1{6+x^2\over\sqrt{x}}\ dx$$
### Rewrite using rational exponents

$$\begin{align}
f(x) &= \int^4_1{6\over\sqrt{x}}+{x^2\over\sqrt{x}}\ dx\\
&=\int^4_16x^{-1/2}+x^{2-1/2}\ dx \\
&= \int^4_16x^{-1/2}+x^{3/2}\ dx
\end{align}$$

### Evaluate the integral
$$\begin{align}
\int^4_16x^{-1/2}+x^{3/2} &= F(4) - F(1)\\
\\
&= (12(4)^{1\over2}-12(1)^{1\over2})+({2\over5}(4)^{5\over2}-{2\over5}(1)^{5\over2})\\
&=[12(2)-12]+[{2\over5}(32)-{2\over5}]\\
&={60\over5}+{62\over5}\\
&={122\over5}
\end{align}$$