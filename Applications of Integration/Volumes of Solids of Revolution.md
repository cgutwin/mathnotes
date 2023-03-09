- A **solid of revolution** is obtained by revolving a region about a line.
- Solid, cross-sections perpendicular to the axis of rotation are circular.

## Procedure in General

The volume of a solid of revolution is calculated by
$$V = \int_a^bA(x)\ dx$$or $$V = \int_c^dA(y)\ dy$$
and we find the cross-sectional area $A(x)$ or $A(y)$ in one of:

### Cross-section as a disk
As in [[#Example 1]] [[#Example 2]] and [[#Example 3]], we find the area using $$A=\pi r^2$$
### Cross-section as a washer
As in [[#Example 4]], we find the area by subtracting the inner area from the outer area using $$A=\pi\left(r_{outer}\right)^2-\pi\left(r_{inner}\right)^2$$

## Example 1

>[!question] Example 1
>Find the volume of the solid obtained by rotating about the x-axis the region under the curve $y=\sqrt{x}$ from 0 to 1.

(a) is an example of a $\Delta x$ region under the curve from 0 to 1.
(b) is the rotation of $\Delta x$ around the x-axis.

The slice in (b) has a radius of $\sqrt{x}$.
![[ogfyozon.bmp|center]]

The area of this cross-section (red) is
$$A(x) = \pi(\sqrt{x})^2 = \pi x$$
The volume, from [[Volumes#Volume of a Right Cylinder|the volume of a right cylinder]] is
$$A(x)\Delta x = \pi x\ \Delta x$$

As the solid lies between 0 and 1, from the [[Volumes#Definition of Volume|definition of volume]]
$$\begin{align}
V=\int_0^1A(x)\ dx &=\int_0^1\pi x\ dx\\
&=\pi\left[{1\over2}x^2\right]_0^1\\
&={\pi\over2}\\
&&\square
\end{align}$$
## Example 2

>[!question] Example 2
>Find the volume of the solid obtained by rotating the region bounded by $y=x^3$, $y=8$, and $x=0$ about the y-axis.


![[c4loi38r.bmp|center]]

As the region is rotated around the y-axis, it's easier to ==slice perpendicular to the y-axis== and therefore ==integrate w.r.t. y==.

A slice at height y will get a disk with radius x, where $x=\sqrt[3]{y}$.

So the area of the cross section is 
$$A(y)=\pi x^2 = \pi\left(\sqrt[3]{y}\right)^2=\pi y^{2\over3}$$
So the volume of the approximated cylinder is
$$
A(y)\Delta y=\pi y^{2\over3}\Delta y
$$

As the cylinder lies between $y=0$ and $y=8$, the volume is
$$\begin{align}
V = \int_0^8A(y)\ dy&=\int_0^8\pi y^{2\over3}\Delta y\\
&=\pi[{3\over5}y^{5\over3}]_0^8\\
&={96\pi\over5}\\
&&\square
\end{align}$$

## Example 3

>[!question] Example 3
> The region $\mathscr{R}$ enclosed by curves $y=x$ and $y=x^2$ is rotated about the x-axis. Find the volume of the resulting solid.

![[0gbzae6y.bmp|center]]

- Find the points of intersection of the curves
  
  The curves intersect at (0,0) and (1,1). The region between them is the solid of rotation $\mathscr{R}$ in (a).

The cross-section of the plane (c) forms a washer, with the inner radius $x^2$ and the outer radius $x$.

We find the cross-sectional area by ==subtracting the area of the inner circle from the area of the outer circle.==
$$
A(x)=\pi\left(x\right)^2-\pi\left(x^2\right)^2=\pi\left(x^2-x^4\right)
$$

So the volume of the washer from 0 to 1 is
$$\begin{align}
V=\int_0^1A(x)\ dx &=\int_0^1\pi\left(x^2-x^4\right)\ dx\\
&=\pi\left[{1\over3}x^3-{1\over5}x^5\right]_0^1\\
&={2\pi\over15}\\
&&\square
\end{align}$$

## Example 4

>[!question] Example 4
>Find the volume of the solid obtained by rotating the region in [[#Example 3|example 3]] about the line $y=2$.

The inner radius is $y=2-x$ and the outer radius is $y=2-x^2$.
![[tlffnbue.bmp|center]]

The area of the cross-section is
$$
A(x) = \pi\left(2-x^2\right)^2-\pi\left(2-x\right)^2
$$
So the volume of S is
$$\begin{align}
V=\int_0^1A(x)\ dx &=\int_0^1\left[\pi\left(2-x^2\right)^2-\pi\left(2-x\right)^2\right]\ dx\\
&=\pi\int_0^1\left(x^4-5x^2+4x\right)dx\\
&=\pi\left[{x^5\over5}-5{x^3\over3}+4{x^2\over2}\right]_0^1\\
&={8\pi\over15}\\
&&\square
\end{align}$$