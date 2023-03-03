- Establishes the connection between differential calculus and integral calculus
	- Differentiation and integration are inverse processes
	- Allows easy computing of integrals without sums of areas.

## Fundamental Theorem of Calculus Part 1

>[!ABSTRACT]+ "Area So Far"
> $$g(x)=\int^x_af(t)\mathrm{\ dt}$$
> where $f$ is a continuous function on $[a,b]$ and $x$ varies between $a$ and $b$.
> - $g$ depends only on $x$, which appears as the variable upper limit
> - $a$ is a fixed point
> 
> ![[area_so_far.bmp | center]]

### Example 1 - *g* from *f(t)*
 
>
 >Where *f* is the function displayed, and $g(x)=\int^x_0f(t)dt$, find the values of $g(0), g(1), g(2), g(3), g(4), g(5)$.
>![[ftc_ex1.png | center]]
---
##### Positive Areas
$g(0) = \int^0_0f(t)dt$ which equals 0.

$g(1)$ is the area of the triangle from 1 to 0
$$\begin{align}
g(1)&=\int^1_0f(t)dt\\
&={1\over2}(1\cdot2)\\
&=1
\end{align}$$

$g(2)$ is the sum of areas $g(1)$ and the area of the rectangle from 2 to 1
$$\begin{align}
g(2)&=\int^2_0f(t)dt=\int^1_0f(t)dt + \int^2_1f(t)dt\\
&=1+(1\cdot2)\\
&=3
\end{align}$$

$g(3)$ can be estimated to 1.3 so
$$g(3)=g(2) + \int^3_2f(t)dt \approx 3+1.3 = 4.3$$


##### Negative Areas
- Subtract the negative areas from the positive areas for the net area.
- For $t > 3, f(t) < 0$

$$g(4) = g(3) + \int^4_3f(t)dt \approx 4.3 + (-1.3) = 3.0$$
$$g(5) = g(4) + \int^5_4f(t)dt \approx 3.0 + (-1.3) = 1.7$$
---
The graph of $g$ looks as follows from the points above

![[ftc_ex1_graphofg.png|center]]

### Definition

> [!ABSTRACT]+ The Fundamental Theorem of Calculus, Part 1
> If $f$ is a continuous function on $[a,b]$, then the function $g$ is defined by
> $$g(x) = \int^x_af(t)dt \quad a \le x \le b$$
> is continuous on $[a,b]$ and differentiable on $(a,b)$, and $g^\prime(x) = f(x)$.
> 
>- The abbreviation for this theorem is FTC1.
>- The derivative of a definite integral with respect to its upper limit is the integrand evaluated at the upper limit.

#### Leibniz Notation for FTC1
$${\mathrm{d}\over\mathrm{dx}}\int^x_af(t)\mathrm{dx} = f(x)$$

### Example 1 - Analysis of Graph of *g* from *f*

Let $g(x) = \int^x_0f(t)\mathrm{dt}$, where *f* is on the graph below

#### Evaluate $g(x)$ where...
$$\begin{align}
g(0)&=\int^0_0f(t)\mathrm{dt} = 0 &&\text{(1) The integral from 0 to 0 equal to 0}\\
\\
g(1) &= g(0) + \int^1_0f(t)\mathrm{dt} &&\text{(2) Add (1) and evaluate integral by areas}\\
&=0+(2\cdot1) = 2\\
\\
g(2)&=g(1) + \int^2_1f(t)\mathrm{dt} = 5\\
\\
g(3)&=g(2) + \int^3_2f(t)\mathrm{dt} = 7\\
\\
g(6)&=g(3) + \left(-{1\over2}\right) + \left(-{3\over2}\right) + (-12)\\
&=7-4\\
&=3
\end{align}$$
####
- $g(x)$ is increasing on the interval $[0,3]$
- $g(x)$ has a maximum value at $x=3$

## Fundamental Theorem of Calculus Part 2

### Definition

>[!ABSTRACT]+ The Fundamental Theorem of Calculus Part 2
>If $f$ is continuous on $[a,b]$, then
>$$
>\int^b_af(x)dx = F(b) - F(a)
>$$
>where $F$ is _any_ antiderivative of $f$, that is, a function $F$ such that $F^\prime = f$.

In essence, if we know an antiderivative $F$ of $f$, we can evaluate $\int^b_af(x)dx$ ==simply by subtracting the values of $F$ at the endpoints of the interval $[a,b]$.==

### Proof

Let $g(x) = \int^x_af(t)\ dt$. By [[The Fundamental Theorem of Calculus#Fundamental Theorem of Calculus Part 1#Definition|FTC1]], we know $g^\prime(x)=f(x)$ - $g$ is an antiderivative of $f$.

Let $F(x)$ be any antiderivative of $f$ on $[a,b]$. ==$F$ and $g$ will differ by a constant==
$$
g(x) = F(x) + C
$$
Let $x=a$ and $x=b$
$$\begin{align}
g(a)&=F(a)+C\\
\\
g(a) &= \int^a_af(t)dt\\
&= 0\\
\\
0 &= F(a) + C\\
C &= -F(a)\\
\\
g(x) &= F(x) + C\\
&= F(x) - F(a)\\
\\
g(b) &= \int^b_af(t)dt=g(b)-g(a)\\
&= F(b) - F(a)\\
\\
&\square
\end{align}$$




### Example
Evaluate the integral
$$
\int^3_1e^xdx
$$

- $e^x$ is continuous everywhere
- The antiderivative $F$ of $f(x) = e^x$ is $e^x$

By [[The Fundamental Theorem of Calculus#Fundamental Theorem of Calculus Part 2#Definition|FTC2]], we get $\int^3_1e^xdx = F(3) - F(1) = e^3 - e^1$.
$\square$

Compared to [[The Definite Integral#Example 1|evaluating the Riemann Sum]], using FTC2 is much more straightforward.

This can also be expressed by
$$
\int^3_1e^xdx=\left.e^x\right|_1^3=e^3-e
$$