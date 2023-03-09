- A *surface of revolution* is obtained when a planar curve $C$ is rotated about a line, the axis of rotation; it forms a boundary of a solid of revolution.

## Surface of a Cylinder

![[ddde_0001_0001_0_img1730-t2.png|center]]

The lateral surface area of a cylinder is $A=2\pi rh$. Take the circumference of a cylinder, and multiply it by the height.

## Surface of a Cone

![[ddde_0001_0001_0_img1731-t2.png|center]]

Can flatten the cone to form a sector of a circle with radius $l$, central angle $\theta = \frac{2\pi r}{l}$

### Area of a Sector of a Circle
The ==area of a sector of a circle== with radius $l$ and angle $\theta$ is ${1\over2}l^2\theta$. 

### Lateral Surface Area
Therefore the lateral surface area, using the area of a sector of a circle, and the definition of the central angle, is $$A={1\over2}l^{2}\theta={1\over2}l^{2}{2\pi r\over l}=\pi rl$$
## Complex Surfaces with Bands

### Equation

>[!Definition] Surface Area of a Band
>Let $\ell$ be the slant height, $r_{1}, r_{2}$ be the upper and lower radii	
>$$S = \pi(r_{1}+r_{2})\ell=2\pi\cdot{1\over2}(r_{1}+r_{2})\ell=2\pi \bar{r}\ell$$
>where $\bar{r}={1\over2}(r_{1}+r_{2})$ .

### Proof

The approximating surface is composed of bands formed by rotating a line segment about an axis.

To find surface area, each band can be considered a portion of a circular cone.

The area of the band (frustum of a cone) with slant height $l$ and upper/lower radii $r_{1},r_{2}$ is found by ==subtracting the areas of the cones==:


$$A = \pi r_{2}\left(l_{1}+l\right)-\pi r_{1}l_{1}=\pi\left[(r_{2}-r_{1})\cdot l_{1}+r_{2}l\right]$$
^9cefd5

![[ddde_0001_0001_0_img1732-t2.png|center]]

Using similar triangles:
$$\begin{align*}
{l_{1}\over r_{1}}&={l_{1}+l\over r_2}\\\\
r_{2}l_1&=r_{1}l_{1}+r_{1}l\\\\
(r_{2}-r_{1})l_{1}&=r_{1}l
\end{align*}$$

Substituting this into [[#^9cefd5|Equation 1]]:
$$\begin{align*}
A&=\pi\left[\left({r_{1}l\over l_{1}}\right)\cdot l_1+r_{2}l\right]\\\\
&=\pi\left(r_{1}l+r_{2}l\right)\\\\
&=2\pi rl\\
&&\square
\end{align*}$$
where $r$ is the average radius represented by $r={(r_{1}+r_{2})\over2}$.

### Properties of the Approximating Band
#### Slant Height
$$|\mathrm{P}_{i-1}\mathrm{P}_i|=\sqrt{1+\left[f^{\prime}(x_{i}^*)\right]^{2}}\Delta{x}$$
#### Average Radius
$\bar{y}_i=\frac{y_{i-1}+y_{i}}{2}\approx f(x_{i}^*)$ when $\Delta x$ is small.



### Approximation to the Area of a Complete Surface of Revolution
When $\Delta x$ is small, $y_{i}=f(x_i)\approx f(x_{i}^{*})$ and $y_{i-1}=f(x_{i-1})\approx f(x_{i}^{*})$ since $f$ is continuous.

Therefore
$$2\pi\frac{y_{i-1}+y_{i}}{2}|\mathrm{P}_{i-1}\mathrm{P}_i|\approx 2\pi f(x_{i}^{*})\sqrt{1+\left[f^{\prime}(x_{i}^{*}\right]^{2}}\Delta x$$

So the approximation for the area of complete surface of revolution is
$$\sum\limits_{i=1}^{n}2\pi f(x_{i}^*)\sqrt{1+\left[f^{\prime}(x_{i}^{*})\right]^2}\Delta x$$
The approximation gets better as $n\to\infty$. The formula above is a [[The Definite Integral|Riemann sum]] for the function $g(x) = 2\pi f(x_{i}^*)\sqrt{1+\left[f^{\prime}(x_{i}^{*})\right]^2}$ which makes
$$
\lim\limits_{n\to\infty}\sum\limits_{i=1}^{n}2\pi f(x_{i}^*)\sqrt{1+\left[f^{\prime}(x_{i}^{*})\right]^2}\Delta x=\int_{a}^{b}2\pi f(x_{i}^*)\sqrt{1+\left[f^{\prime}(x_{i}^{*})\right]^2}\ dx
$$

## Example 1
$y=\sqrt{4-x^{2}},-1\le x\le1$ is an arc of the circle $x^{2}+y^{2}=4$. Find the area of the surface obtained by rotating this arc about the x-axis.

![[ddde_0001_0001_0_img1735-t2.png|center]]

$\frac{dy}{dx}=\frac{1}{2}(4-x^{2})^{-\frac{1}{2}}(-2x)=\frac{-x}{\sqrt{4-x^{2}}}$

Making $ds = \sqrt{1+\left(\frac{-x}{\sqrt{4-x^{2}}}\right)^{2}}dx = \sqrt{1+\frac{x^{2}}{4-x^{2}}} dx$:

$$\begin{align*}
S&=\int_{-1}^{1}2\pi y\sqrt{1+\frac{x^{2}}{4-x^{2}}}\ dx\\\\
&=2\pi\int_{-1}^{1} \sqrt{4-x^{2}}\sqrt{1+\frac{x^{2}}{4-x^{2}}}\ dx\\\\
&=2\pi\int_{-1}^{1}\sqrt{4-x^{2}}\sqrt{\frac{4-x^{2}+x^2}{4-x^2}}\ dx\\\\\\
&=2\pi\int_{-1}^{1}\sqrt{4-x^{2}}\frac{2}{\sqrt{4-x^2}}\ dx\\\\
&=4\pi\int_{-1}^{1}1\ dx\\\\
&=4\pi(2)\\\\
&=8\pi\\
&&\square
\end{align*}$$
## Example 2
$x^\left( \frac{2}{3} \right)+y^\left( \frac{2}{3} \right)=4$ for $0\le y \le 8$, rotated around y-axis.

$$\begin{align}
x&=\left( 4-y^{2\over 3}\right)^{3\over2} &&\text{(2.1) Rewrite as function of }y\\\\
\frac{dx}{dy}&=\frac{d}{dy}(4-y^{2\over 3})^{3\over 2} &&\text{(2.2) Differentiate w.r.t. }y\\\\
&=\frac{3}{2}(4-y^{2\over 3})^{1\over 2}\cdot\frac{d}{dy}(4-y^{2\over 3})\\\\
&=\frac{3}{2}(4-y^{2\over 3})^{1\over 2}\cdot\left(-{2\over 3}y^{-{1\over 3}}\right)\\\\
\frac{dx}{dy}&=\frac{\sqrt{ 4-y^{2\over3}}}{y^{1\over3}} &&\text{(2.3) The derivative of (2.1)}\\\\
\\\\
S_{y}&=\int_{0}^{8} 2\pi y\sqrt{1+\left(\frac{\sqrt{ 4-y^{2\over3}}}{y^{1\over3}}\right)^2} \, dy &&\text{(2.4) Integral setup for surface area of revolution.}\\\\ 
\sqrt{1+\left(\frac{\sqrt{ 4-y^{2\over3}}}{y^{1\over3}}\right)^2}&=\sqrt{1+\frac{4-y^{2\over3}}{y^{2\over3}}} &&\text{(2.5) Squaring removes the upper root.}\\\\
&=\sqrt{\frac{4-y^{2\over3}+y^{2\over3}}{y^{2\over3}}} &&\text{(2.6) Adding 1 is adding }\frac{y^{2\over3}}{y^{2\over3}}\\\\
&=\sqrt{4\over y^{2\over3}}=\frac{2}{\sqrt{y^{2\over3}}}=\frac{2}{y^{1\over3}}\\\\\\
S_{y}&=2\pi\int_{0}^{8} \frac{2y}{y^{1\over3}} \, dy =4\pi\int_{0}^{8} y\cdot y^{-{1\over3}} \, dy\\\\
&=4\pi\int_{0}^{8} y^{2\over3} \, dy\\\\
&=4\pi\left[{3\over5}y^{5\over3}\right]_{0}^8\\\\
&=4\pi\left[\frac{3}{5}(8)^{5\over3}-0\right]\\\\
&=\frac{384\pi}{5}\\\\
&&&\square
\end{align}$$
