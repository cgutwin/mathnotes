# Type 1 - Infinte Intervals

- a and/or b is unbounded:
	- $\int_b^{-\infty}f(x)\ dx$

- Determining convergence or divergence finds wether the integral is finite.

>[!Definition] Improper Integral of Type 1
>1. If $\int_a^t f(x)\ dx$ exists for all $t \ge a$, then
>$$\int_a^\infty f(x)\ dx = \lim\limits_{t\to\infty}\int_a^tf(x)\ dx$$
>provided that this limit exists as a finite number.
>
>2. If $\int_t^b f(x)\ dx$ exists for all $t \le b$, then
>   $$\int_{-\infty}^b f(x)\ dx = \lim\limits_{t\to-\infty}\int_b^tf(x)\ dx$$
>   provided that this limit exists as a finite number.

The improper integrals $\int_a^\infty f(x)\ dx$ and $\int_{-\infty}^b f(x)\ dx$ are **convergent** if the corresponding limit exists, and **divergent** if the limit does not exist or is infinite.

If both  $\int_{-\infty}^a f(x)\ dx$ and $\int_a^\infty f(x)\ dx$ are convergent for any $a\in R$ then we define
$$
\int_{-\infty}^\infty f(x)\ dx = 
\int_{-\infty}^a f(x)\ dx + \int_a^\infty f(x)\ dx = \lim\limits_{s\to\infty}\int_s^a f(x)\ dx + \lim\limits_{t\to\infty}\int_a^t f(x)\ dx
$$

$\int_{-\infty}^{\infty} \frac{x^3}{x^4 + 1} dx$

Since the integrand is an odd function, we can simplify our calculations by just evaluating the integral from $0$ to $\infty$ and then multiplying by $2$:

$\int_{0}^{\infty} \frac{x^3}{x^4 + 1} dx$

To solve this integral, we can use the substitution $u = x^4 + 1$. Then, $du = 4x^3 dx$, so $x^3 dx = \frac{1}{4} du$:

$\int_{0}^{\infty} \frac{x^3}{x^4 + 1} dx = \frac{1}{4} \int_{1}^{\infty} \frac{1}{u} du = \frac{1}{4} \ln |u| |_1^\infty = \frac{1}{4} \ln (\infty) - \frac{1}{4} \ln (1) = 0$

Therefore, the integral is equal to $0$.