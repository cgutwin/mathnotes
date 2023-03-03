An extension to [[The Midpoint Rule]]

The trapezoidal rule is the **average of the left hand approximation and right hand approximation**

$$\begin{align}
\int_a^bf(x)\ dx &\approx {1\over2}\left[\sum^n_{i=1}f(x_{i-1})\Delta{x} + \sum^n_{i=1}f(x_{i})\Delta{x} \right] ={\Delta x\over2}\left[\sum^n_{i=1}(f(x_{i-1})+f(x_i))\right]\\
&={\Delta x\over2}\left[(f(x_0)+f(x_1))+(f(x_1)+f(x_2))+\dots+(f(x_{n-1})+f(x_n))\right]\\
&={\Delta x\over2}\left[(f(x_0)+2f(x_1))+2f(x_2)+\dots+2f(x_{n-1})+f(x_n)\right]
\end{align}$$

>[!definition] Trapezoidal Rule
> $\int_a^bf(x)\ dx \approx = {\Delta x\over2}\left[f(x_0)+2f(x_1)+2f(x_2)+\dots+2f(x_{n-1})+f(x_n)\right]$ where $\Delta x = {(b-a)\over n}$ and $x_i = a + i\ \Delta x$.

## Example 01
Approximate the integral $\int_1^2({1\over x})\ dx$ with $n = 5$. 

### Trapezoidal Rule

$$\begin{align}
n=5\\
a=1\\
b=2\\
\\
\Delta x = {(2-1)\over5} = 0.2\\
\\
&\text{From the trapezoidal rule:}\\
\\
\int_2^1({1\over x})\ dx \approx T_5 &= {0.2\over2}\left[f(1)+2f(1.2)+2f(1.4)+2f(1.6)+2f(1.8)+f(2)\right]\\
&=0.1\left({1\over1}+{2\over1.2}+{2\over1.4}+{2\over1.6}+{2\over1.8}+{1\over2}\right)\\
&\approx0.695635
\end{align}$$
![[xu9juk4l.bmp|center]]
### Midpoint Rule
The midpoints of the five subintervals are 1.1, 1.3, 1.5, 1.7, and 1.9. By the [[The Midpoint Rule]]:

$$\begin{align}
\int_2^1{1\over x}\ dx &\approx \Delta x\left[f(1.1)+f(1.3)+f(1.5)+f(1.7)+f(1.9)\right]\\
&={1\over5}\left({1\over1.1}+{1\over1.3}+{1\over151}+{1\over1.7}+{1\over1.9}\right)\\
&\approx 0.691908
\end{align}$$
![[x2oyhe5m.bmp|center]]
###
In this example, the trapezoidal estimate is larger than the midpoint estimate. We know $\int_1^2{1\over x}dx = \ln 2 \approx 0.693147$. The trapezoidal rule is an overestimate and the midpoint rule is an underestimate.