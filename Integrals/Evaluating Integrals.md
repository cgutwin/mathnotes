## Example 1

Evaluate $\int^4_2(12-6x)\mathrm{dx}$

$f(x) = 12-6x, a = 2, b = 4$ and
$$
\Delta{x} = \frac{b-a}{n} = \frac{4 - 2}{n} = \frac{2}{n}
$$

The general form of the subinterval endpoints are
$$
x_i=2+i\cdot\frac{2}{n} = 2+\frac{2i}{n}
$$
Now we evaluate the Integral Limit

$$\begin{align}
\int^4_2(12-6x)\mathrm{dx}&=\lim\limits_{n\to\infty}\sum^n_{i=1}f(x_i)\Delta{x} &&\text{(1) From the definition of an integral limit}\\
\\
&=\lim\limits_{n\to\infty}\sum^n_{i=1}\left[12-6\left(2+\frac{2i}{n}\right)\right]\left(\frac{2}{n}\right)&&\text{(2) Substituting into xi into f(x)} \\
\\
&= \lim\limits_{n\to\infty}\left(\frac{2}{n}\right)\sum^n_{i=1}\left[12-6\left(2+\frac{2i}{n}\right)\right] &&\text{(3) n is constant so we can move 2/n infront of the sigma}\\
\\
&= \lim\limits_{n\to\infty}\left(\frac{2}{n}\right)\sum^n_{i=1}\left(12-12-\frac{12i}{n}\right) &&\text{(4) Expand}\\
\\
&= \lim\limits_{n\to\infty}\left(\frac{2}{n}\right)\sum^n_{i=1}\left(-\frac{12}{n}i\right) \\
\\
&= \lim\limits_{n\to\infty}\left(\frac{2}{n}\right)\cdot\left(-\frac{12}{n}\right)\sum^n_{i=1}i &&\text{(5) -12/n is constant so move infront of sigma} \\
\\
&= \lim\limits_{n\to\infty}\left(\frac{-24}{n^2}\right)\left[\frac{n(n+1)}{2}\right] &&\text{(6) Replace sum with equation for sum of digits up to n}\\
\\
&= \lim\limits_{n\to\infty}\left[-12\left(1+\frac{1}{n}\right)\right] \\
\\
\int^4_2(12-6x)\mathrm{dx}&= -12
\end{align}$$

