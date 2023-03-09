>[!Formula] Area bounded by Polar Curves
>Let $f$ be a continuous function of the angle $\theta$ for $\theta\in[a,b]$.
>The polar region $R$ bounded by the curve $r=f(\theta)$, for $\theta\in[a,b]$ has area given by
>$$A=\int_{a}^{b} \frac{1}{2}r^2 \, d\theta = \int_{a}^{b} \frac{1}{2}[f(\theta)]^2 \, d\theta $$

The area bounded by polar curves is similar to the formula for the [[Area of a Surface of Revolution#Area of a Sector of a Circle|area of a sector of a circle.]]

* In applying the formula for the area bounded by polar curves, its helpful to thing of the area as being swept out by a rotating ray through $O$ that starts with angle $a$ and ends with angle $b$.
	
	![[ddde_0001_0001_0_img2374-t2.png|center]]

## Example
Find the area enclosed by the cardioid $r=1+\cos \theta$

$$\begin{align}
A &= \int_{0}^{2\pi} \frac{1}{2}r^2 \, d\theta\\
&= \frac{1}{2} \int_{0}^{2\pi} (1+\cos \theta) \, d\theta\\
&= \frac{1}{2}\int_{0}^{2\pi} 1+2\cos \theta+\cos^2\theta \, d\theta\\
&=\frac{1}{2}\left[ \theta-2\sin \theta\right]\\
\dots
\end{align}$$
