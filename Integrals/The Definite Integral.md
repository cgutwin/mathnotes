---
tags:
 - MATH152/Lecture3
 - IntegralCalculus/Definitions
---

The [[The Area Problem#Integral Limit|Integral Limit]] is given a special name and notation:

## Definition of a Definite Integral

If $f$ is a function defined for $a\le x \le  b$, we divide the interval $\left[a,b\right]$ into $n$ subintervals of equal width $\Delta{x}=\frac{(b-a)}{n}$ ([[The Area Problem#Area Under Parabola in General]]), we let $x_0=a,x_1,\dots,x_n=b$ be the endpoints of the subintervals and let $x_1^*,x_2^*,\dots,x_n^*$ be any **sample endpoints** in these subintervals so $x_i^*$ lies in the *i*th subinterval $\left[x_{i-1},x_i\right]$. Then the
**==definite integral of *f* from *a* to *b*==** is:

$$
\int^b_af(x)\mathrm{dx} = \lim\limits_{n\to\infty}\sum^{n}_{i=1}f(x^*_i)\Delta{x}
$$
- $f(x)$ is the **integrand**
- *a* and *b* are the **limits of integration**, where *a* is the **lower limit** and *b* is the **upper limit**.

- Taking the limit as n goes to infinity subsequently reduces $\Delta{x}$ to zero.
- This is provided:
	- **The limit exists of the sum**
	- the same limit exists **independently of which $x^*_i$ is chosen.**
		- ie. The limit is the same no matter which sample point on which interval you choose.

## Theorem

If $f$ is integrable on $\left[a,b\right]$, then
$$\int^b_af(x)\mathrm{dx} = \lim\limits_{n\to\infty}\sum^{n}_{i=1}f(x^*_i)\Delta{x}
$$
where
$$
\Delta{x}=\frac{(b-a)}{n}
$$
and
$$x_i = a + i\Delta{x}$$

## Common Choices for $x^*_i$
### Right Hand Endpoint
### Left Hand Endpoint
### Midpoint
See [[The Midpoint Rule]].

### Minimizer
### Maximizer
Let $x^*_i$ be a point where *f* obtains its *maximum* value on the interval
$$
f(x^*_i) \ge f(x) \text{ for all } x \in [x_{i-1},x_i]
$$
This gives the **upper sum**


## Example 1

**Evaluate the Riemann** sum for $f(x) = x^3 - 6x, 0\le x_0 \le3$ with $n = 6$ subintervals and taking the sample endpoints to be the right endpoints.

Each interval width is
$$\begin{align}
\Delta{x} &= \frac{\left(b-a\right)}{n}\\
&= \frac{\left(3-0\right)}{6}\\
&= \frac{1}{2}
\end{align}$$
so for 6 intervals:
$$
x_1 = 0.5 \quad x_2 = 1.0 \quad x_3 = 1.5 \quad x_4 = 2.0 \quad x_5=2.5 \quad x_6=3.0
$$

The Riemman sum would be evaluated as

$$\begin{align}
R_6 &= \sum^{6}_{i=1}f(x_i)\Delta{x}\\
&= f(0.5)\ \Delta{x} + f(1.0)\ \Delta{x} +f(1.5)\ \Delta{x} +f(2.0)\ \Delta{x} +f(2.5)\ \Delta{x} +f(3.0)\ \Delta{x}\\
&= \frac{1}{2}(-2.875 - 5 - 5.625 -4 + 0.625 + 9)\\
&= -3.9375
\end{align}$$

As the sum is negative, its the **net amount of positive rectangles and negative rectangles.**
![[net_rectangles_sum.bmp]]
## Example 2

Express
$$
\lim\limits_{n\to\infty}\sum^{n}_{i=1}\left(x^3_i+x\sin{x_i}\right)\Delta{x}
$$
as an integral on the interval $\left[0,\pi\right]$.

---

* The upper limit is $\pi$.
* The lower limit is 0.

So, the limit can be expressed in an integral as

$$
\int^{\pi}_{0}\left(x^3+x\sin{x}\right)
$$
