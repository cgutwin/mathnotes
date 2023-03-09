## Example

Find the arc length of one arch of the cycloid
$$
x=r(\theta-\sin \theta) \qquad y=r(1-\cos \theta), \qquad 0 \le \theta\le 2\pi
$$

One arch is described by the parameter interval $0\le\theta\le 2\pi$

$$\begin{align}
dx &= r(1-\cos \theta)d\theta\\
\frac{dx}{dy} &= r(1-\cos \theta)\\
\\
dy &= r\sin \theta d\theta\\
\frac{dy}{d\theta} &= r\sin \theta
\end{align}$$

Using the formula for arc length $L =\int_{0}^{2\pi} \sqrt{ \left( \frac{dx}{d\theta} \right)^2 + \left( \frac{dy}{d\theta} \right)^2 }^ \, d\theta$:
$$\begin{align}
L&=\int_{0}^{2\pi} \sqrt{ r^2(1-\cos \theta)^2 + r^2\sin^2\theta} \, d\theta\\
&=\int_{0}^{2\pi} r^2(1-2\cos \theta+\cos^2\theta+\sin^2\theta) \, d\theta\\
&=\int_{0}^{2\pi} \sqrt{2(1-\cos \theta)} \, d\theta
\end{align}$$

Use the identity $\sin^2x=\frac{1}{2}(1-\cos2x)$ with $\theta=2x$, which gives $1-\cos \theta =2\sin^2\left( \frac{\theta}{2} \right)$.

$$
\sqrt{ 2(1-\cos \theta)}=4\sin^2\left( \frac{\theta}{2} \right)=2\ |\sin\left( \frac{\theta}{2} \right)| = 2\sin\left( \frac{\theta}{2} \right)
$$

So
$$\begin{align}
L &= 2r \int_{0}^{2\pi} \sin\left( \frac{\theta}{2} \right) \, d\theta \\
&= 2r\left[ -2\cos\left( \frac{\theta}{2} \right) \right]_{0}^{2\pi}\\
&= 2r[2 + 2]\\
&= 8r
\end{align}
$$
