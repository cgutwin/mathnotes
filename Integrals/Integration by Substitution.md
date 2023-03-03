## $\int\sec^2{\theta}\tan^3{\theta}\ d\theta$

$$\begin{align}
\text{Let u}&=\tan{\theta}\\
du &= \sec^2{\theta}\ d\theta\\
\\
&\Downarrow
\\
\\
\int\sec^2{\theta}\cdot u^3\ d\theta&=\int u^3\ du\\
&={1\over4}u^4 + C\\
&={1\over4}\tan^4{\theta} + C

\end{align}$$

## $\int\frac{\left(\arctan{x}\right)^2}{x^2 + 1}\ dx$

$$\begin{align}
\text{Let u}&=\arctan{x}\\
du &= {1\over1+x^2}dx\\
\\
&\Downarrow
\\
\\
\int\frac{\left(\arctan{x}\right)^2}{x^2 + 1}\ dx &=\int u^2\cdot{1\over x^2+1} dx\\
&=\int u^2\ du\\
&= {1\over3}u^3+C\\
&={\left(\arctan{x}\right)^3\over3}+C
\end{align}$$

## $\int\frac{\sin{2x}}{1+\cos^2x}\ dx$

$$\begin{align}
\text{Let u}&=1+\cos^2x\\
du &= -2\cos{x}\sin{x}\ dx\\
-{1\over2}du&=\cos{x}\sin{x}
\\
\\
&\Downarrow
\\
\\
\int\sin{2x}\cdot{1\over u}\ dx &= \int2\sin{x}\cos{x}\cdot{1\over u}\ dx\\
&=2\int\sin{x}\cos{x}\cdot{1\over u}\ dx\\
&=2\int-{1\over 2}\cdot{1\over u}\ du\\
&=-\ln(1+\cos^2x)+C &&\text{No absolute value as u is always positive.}
\end{align}$$

## $\int\frac{1+x}{1+x^2}\ dx$
$$\begin{align}
\text{Let u}&=1+x^2\\
du &= 2x\ dx\\
{1\over2}du&=x\ dx
\\
\\
&\Downarrow
\\
\\
\int\frac{1+x}{1+x^2}\ dx &=\int{1\over u}+{1\over 1+x^2}\cdot x\ dx\\
&={1\over2}\int{1\over u}+{1\over 1+x^2}\ du\\
&={1\over2}\ln(1+x^2)+\arctan{x}+C\\\\
&\square
\end{align}$$