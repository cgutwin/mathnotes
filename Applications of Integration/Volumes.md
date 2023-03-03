## Volume of a Right Cylinder

>[!definition] Volume of a Right Cylinder
>$$V = Ah$$ 
>where $A$ is the area of the base, and $h$ is the height.
>
>If the base is a circle with radius $r$, the volume is expressed as
>$$V = \pi r^2h$$

## Definition of Volume

Let $S$ be a solid that lies between $x=a$ and $x=b$. If the cross-sectional area of $S$ in the plane $P_x$, through $x$ and perpendicular to the x-axis, is $A(x)$, where $A$ is a continuous function, then the volume of $S$ is
$$
V = \lim\limits_{n\to\infty}\sum_{i=1}^n
A(x_i^*)\Delta x=\int_a^bA(x)\ dx$$

## Example
Show that the volume of a sphere of radius $r$ is $V = {4\over3}\pi r^3$.

Placing the sphere with the center on the origin, a plane (red) intersects the circle with a radius of $y=\sqrt{r^2-x^2}$. This is from the inner triangle formed, with the radius meeting at the coordinate (x,y).
![[jf894kl3.bmp|center]]

The area of the cross-section (red) is $A(x) = \pi y^2 = \pi\left(r^2-x^2\right)$.

From the [[#Definition of Volume]]
:
$$\begin{align}
a &= -r\\
b &= r\\
\\
V=\int_a^bA(x)\ dx &= \int_{-r}^r\pi\left(r^2-x^2\right)\ dx\\
&=2\pi\int_0^r(r^2-x^2)\ dx\quad\text{The integrand is even, double it over half the interval.}\\
&=2\pi\left[r^2x-{1\over3}x^3\right]_0^r\\
&=2\pi\left[r^3-{1\over3}r^3\right]\\
&={4\over3}\pi r^3
\end{align}$$
