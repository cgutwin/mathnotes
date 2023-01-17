The Midpoint Rule implements a [[The Definite Integral#Common Choices for $x *_i$|midpoint]] of common choices of $x_i$.

## Theorem

>$$\int^b_af(x)\mathrm{dx}\approx\sum^n_{i=1}f(\bar{x}_i)\Delta{x}=\Delta{x}\left[f(\bar{x}_1)+\dots+f(\bar{x}_n)\right]$$
Where
$$\Delta{x}=\frac{b-a}{n}$$
and
$$\bar{x}=\frac{1}{2}(x_{i-1}+x_i)=\text{midpoint of }[x_{i-1},x_i]$$
* The midpoint is just a [[The Definite Integral#Theorem|sample point]] chosen within the interval $[x_{i-1},x_i]$.

## Example 1
Use the midpoint rule with $n = 5$ to approximate $\int^2_1\frac{1}{x}\mathrm{dx}$.

$$\Delta{x} = \frac{2 - 1}{5} = \frac{1}{5}$$
The endpoints of the 5 intervals are 1.0, 1.2, 1.4, 1.6, 1.8, and 2.0. So, the midpoints are

$$x_1 = 1.1 \quad x_2=1.3 \quad x_3=1.5 \quad x_4=1.7 \quad x_5=1.9$$

From the Midpoint Rule:

$$\begin{align}
\int^2_1\frac{1}{x}\mathrm{dx} &\approx \Delta{x}\left[f(1.1)+f(1.3)+f(1.5)+f(1.7)+f(1.9)\right]\\
&= \frac{1}{5}\left[\frac{1}{1.1}+\frac{1}{1.3}+\frac{1}{1.5}+\frac{1}{1.7}+\frac{1}{1.9}\right] \\
&\approx 0.691908
\end{align}$$
