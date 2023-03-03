- Try to write the integrand with powers of sine and cosine in a form that has
	- One sine factor, with the rest in the cosine factor, or
	- One cosine factor, with the rest in the sine factor.

## Example 1


>[!question] Example 1
>Evaluate $\int \cos^3x\ dx$.

- Substituting $u = \cos x$ won't help as $du = -\sin x\ dx$ which isn't a factor in the integral.
- Use the identity ==$\sin^2x + \cos^2x = 1$==

$$\begin{align}
\cos^3{x} &= \cos^2x\cdot\cos x=(1-\sin^2x)\cdot\cos x\\
\\
&\Downarrow\\
\\
\int\cos^3{x}\ dx &= \int\cos^2x\cdot\cos x\ dx\\
&= \int(1-\sin^2x)\cdot\cos x\ dx\\
\\
\text{Let u} &=\sin x\\
du&=\cos x\ dx\\
\\
&=\int(1-u^2)\ du\\
&=u-{1\over3}u^3+C\\
&=\sin x-{1\over3}\sin^3x+C\\
&&\square
\end{align}$$

## Example 2

>[!question] Example 2
> Find $\int\sin^5x\cos^2x\ dx$.

- Converting $\cos^2x$ to a factor of sine yields no remaining cosine factor
- Instead, ==separate a single sine factor==.


$$\begin{align}
\sin^5x\cos^2x &= \left(\sin^2{x}\right)^2\cdot\cos^2x\cdot\sin{x}\\
&=\left(1-\cos^2x\right)^2\cdot\cos^2x\cdot\sin{x}\\
\\
&\Downarrow\\
\\
\text{Let }u&=\cos{x}\\
du&=-\sin{x}\ dx\\
\\
\int\sin^5x\cos^2x\ dx&=\int\left(1-\cos^2x\right)^2\cdot\cos^2x\cdot\sin{x}\ dx\\
&=\int(1-u^2)^2\cdot u^2\cdot(-du)\\
&=-\int\left(u^2-2u^4+u^6\right)\ du\\
&=-\left({1\over3}u^3-{2\over5}u^5+{1\over7}u^7\right)\ + C\\
&=-{1\over3}\cos^3x+{2\over5}\cos^5x-{1\over7}\cos^7x+C\\
&&\square
\end{align}$$

## Example 3

>[!question] Example 3
>Evaluate $\int_0^\pi\sin^2x\ dx$.

- The integrand expressed as $1-\cos^2x$ is no simpler
- Use the half-angle identity for $sin^2x$

$$\begin{align}
\int_0^\pi\sin^2x\ dx&={1\over2}\int_0^\pi\left(1-\cos2x\right)\ dx\\
&=\left[{1\over2}\left(x-{1\over2}\sin2x\right)\right]_0^\pi\\
&={1\over2}\left(\pi-{1\over2}\sin2\pi\right)-{1\over2}\left(0-{1\over2}\sin0\right)\\
&={\pi\over2}
\end{align}$$


## Strategy for Evaluating Trig Integrals

For $\int\sin^mx\cos^nx\ dx$

### Odd power of cosine
- Save one cosine power and use $\cos^2x = 1 - \sin^2x$ to express remaining in terms of sine
$$\begin{align}
\int\sin^mx\cos^{2k+1}x\ dx &= \int\sin^mx\cdot\left(\cos^2x\right)^k\cdot\cos{x}\ dx\\
&=\int\sin^mx\cdot\left(1-\sin^2x\right)^k\cdot\cos{x}\ dx
\end{align}$$
Then substitute $u = \sin x$.
See [[#Example 1]].

### Odd power of sine
- Save one sine power and use $\sin^2x = 1 - \cos^2x$ to express the remaining in therms of sine
$$\begin{align}
\int\sin^{2k+1}x\cos^nx\ dx &=\int\left(\sin^2x\right)^k\cdot\cos^n{x}\sin{x}\ dx\\
&=\int\left(1-\cos^2x\right)^k\cdot\cos^nx\cdot\sin{x}\ dx
\end{align}$$
Then substitute $u = \cos x$.
See [[#Example 2]].

### Both powers are even
- Use the half angle identies
- Sometimes you can use $\sin x\cdot\cos x = {1\over2}\sin2x$.
- See [[#Example 3]].