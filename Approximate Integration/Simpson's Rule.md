- Simpsons rule is the use of parabolas instead of straight line segments to approximate a curve.

>[!Definition] Simpson's Rule
>$$\begin{align}
\int_a^bf(x)\ dx &\approx S_n = {\Delta x\over3}[f(x_0) + 4f(x_1)+2f(x_2)+4f(x_3)+\dots\\
&+f(x_{n-2})+4f(x_{n-1})+f(x_n)]
\end{align}$$
> where $n$ is even and $\Delta x = {(b-a)\over n}$


## Example 1
Use Simpson's Rule with $n=10$ to approximate $\int_1^2({1\over x})\ dx$.

$$\begin{align}
f(x) &= {1\over x} \qquad n=10 \qquad\Delta x={2-1\over10}={1\over10}\\
\\
\int_1^2({1\over x})\ dx &\approx S_{10}\\
&={\Delta x\over3}[f(1) + 4f(1.1)+2f(1.2)+4f(1.3)+\dots+2f(1.8)+4f(1.9)+f(2)]\\
&={0.1\over3}\left({1\over1}+{4\over1.1}+{2\over1.2}+{4\over1.3}+\dots+{4\over1.9}+{1\over2}\right)\\
&\approx0.693150
\end{align}$$

## Example 2
The graph of the acceleration $a(t)$ of a car, measured in $\text{ft/s}^2$ is shown. Use Simpson’s Rule to estimate the increase in the velocity of the car during the six-second time interval.
![[ddde_0001_0001_0_img1627-t2.png|center]]
- Make sure the units are consistent
	- Let $d$ be measured in feet

Acceleration is the rate of change of velocity: $A(t) = V^\prime(t)$
By the net change theorem ([[The Fundamental Theorem of Calculus#Fundamental Theorem of Calculus Part 2|FTC 2]]):
$$
\int_0^{6}A(t)\ dt=\int_0^{6}V^\prime(t)\ dt = V(6)-V(0)
$$
Which is the total increase in the velocity of the car.

$$\begin{align}
&\text{Let }n=6\qquad\Delta t={6-0\over6}=1\\
\\
\int_0^6V(t)\ dt &\approx {\Delta t\over3}\left[A(0)+4A(1)+2A(2)+4A(3)+2A(4)+4A(5)+A(6)\right]\\
&\approx{1\over3}\times[0+4(1)+2(4)+4(10)+2(13)+4(9)+0]\\
&=38\text{ ft/s}^2
\end{align}$$

The increase of velocity of the car over the six-second interval is approximately 38$\text{ft/s}$.

- The answer given was 37.7ft/s. This is down to a more accurate approximation of each subinterval's $f(x_i^*)$.