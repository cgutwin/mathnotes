

1 Find the most general antiderivative of the function
---
$$
f(x) = x^2 - 9x + 4
$$
$$\begin{align}
F(x) &= \frac{x^3}{3}+\frac{9x^2}{2}+4x+C &&\text{(1) Add 1 to each power, set denominator to the power}\\
&&&\text{and add the constant C}\\
\\
&= \frac{1}{3}x^3+\frac{9}{2}x^2+4x+C &&\text{(2) Rewrite of (1) to bring coefficient out}\\
\\
\\
&\text{(1) is an acceptable answer}
\end{align}$$


12 Use the Midpoint Rule with $n = 4$ to approximate the integral
---
14 Express the Integral as a Limit of Riemann Sums using Right Endpoints
---

$$
\int^4_2\sqrt{5+x^2}\ \mathrm{dx}
$$

#### Find the width of each subinterval in terms of $n$.

The width of each subinterval is $\Delta{x} = \frac{b-a}{n}$ where $b = 4$ is the number on top and $a = 2$ is the number on the bottom. 
$$
\Delta{x} = \frac{4 - 2}{n} = \frac{2}{n}
$$

#### Find the *i*th endpoint in terms of $n$.

In general, the endpoint is

$$\begin{align}
x_i &= a + i\Delta{x} \\
&= 2 + \frac{2i}{n} \\
\end{align}$$
#### Evaluate $f(x) = \sqrt{5+x^2}$ at the *i*th endpoint.
Substitute the general form for $x_i$ from above into $f(x)$

$$f(x_i) = \sqrt{5+\left(2+\frac{2i}{n}\right)^2}$$

#### Express the integral as the limit of Riemann sums using right endpoints.

Using right endpoints means that $i=1$.
Use the equation for limit of Riemann sums from [[The Area Problem#Integral Limit]].

$$ \lim\limits_{n\to\infty}\sum^n_{i=1}\left[\sqrt{5+\left(2+\frac{2i}{n}\right)^2}\cdot\frac{2}{n}\right]$$

21 If m ≤ f(x) ≤ M for a ≤ x ≤ b, where _m_ is the absolute minimum and _M_ is the absolute maximum of _f_.
---
$$
\int^2_0\frac{5}{x+4}\mathrm{dx}
$$
As over the interval $[0,2]$, $f(x)$ is a decreasing function. So $f(0)$ will be the maximum $M$ and $f(2)$ will be the minimum $m$.

$$\begin{align}
f(0) = \frac{5}{0+4} = \frac{5}{4} = M\\
f(2) = \frac{5}{2+4} = \frac{5}{6} = m\\
\end{align}$$
By Property 8

$$\begin{align}
\frac{5}{6}\left(2-0\right)\le&\int^2_0\frac{5}{x+4}\mathrm{dx}\le\frac{5}{4}(2-0)\\
\\
\frac{10}{6}\le&\int^2_0\frac{5}{x+4}\mathrm{dx}\le\frac{10}{4}
\end{align}$$

Therefore, $\int^2_0\frac{5}{x+4}\mathrm{dx}$ lies between $\frac{10}{6}$ and $\frac{10}{4}$.