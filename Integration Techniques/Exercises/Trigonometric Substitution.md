## 1
Find the area inside the ellipse defined by $9x^2+4y^2=36, 0\le x\le 1$

1. Rewrite $y$ in terms of $x$
	$$\begin{align}
	4y^2&=36-9x^2=9(4-x^2)\\
	y^2&=\frac{9}{4}(4-x^2)\\
	y&=\frac{3}{2}\sqrt{4-x^2}
	\end{align}$$
	This yields the formula for the upper half of the ellipse. By symmetry, we can just multiply the final integral by 2.

2. Form the integral
	$$A=2\int_{0}^{1} \frac{3}{2}\sqrt{4-x^2} \, dx $$
	Can further pull the $3\over2$ outside the integrand.

3. Recognize that the integrand is a trigonometric substitution
	$\sqrt{ 4-x^2 }$ is in the form $\sqrt{ a^2-x^2 }$ where $a=2$
	$$\begin{align}
	\text{Let }x&=a\sin \theta = 2\sin \theta\\
	dx&= 2\cos \theta\  d\theta
	\end{align}$$
	==Change the limits of integration==
	$$\begin{align}
	\text{When }x&=0,\theta=0\\
	\text{When }x&=1\\
	1&=2\sin \theta\\
	\frac{1}{2}&=\sin \theta\\
	\theta&=\arcsin{1\over2}\\
	\theta&=\frac{\pi}{6}
	\end{align}$$

	So:
	$$\begin{align}
	\sqrt{ 4-x^2 }&=\sqrt{ 4-(2\sin \theta)^2 }\\
	&=\sqrt{ 4-4\sin^2\theta }\\
	&=\sqrt{ 4-4(1-\cos^2\theta)}\\
	&=\sqrt{4\cos^2\theta}\\
	&=2|\cos \theta|\\
	&=2\cos \theta &&\text{Remove absolute value since using top half (+).}
	\end{align}$$
	
	It follows:
	$$\begin{align}
	A=3\int_{0}^{\pi/6} \sqrt{4-x^2 } \, dx &=  3\int_{0}^{\pi/6} 2\cos \theta\cdot2\cos \theta  \, d\theta\\
	&=12\int_{0}^{\pi/6} \cos^2\theta \, d\theta\\
	&\text{Perfect for double-angle identity}\\
	&=12\int_{0}^{\pi/6} \frac{1}{2}(1+\cos{2\theta}) \, d\theta\\
	&=6\int_{0}^{\pi/6} 1+\cos2\theta \, d\theta\\
	&=6\left[\theta+\frac{2\sin2\theta}{2}\right]_{0}^{\pi/6}\\
	&=6\left[\frac{\pi}{6}+\frac{\sin \frac{\pi}{3}}{2}\right]\\
	&=\pi+3\sin \frac{\pi}{3}\\
	&=\pi+\frac{3\sqrt{ 3 }}{2}\\
	&&\square.
	\end{align}$$


So, the area of the ellipse from $0\le x\le 1$ is $\pi+\frac{3\sqrt{ 3 }}{2}$.

