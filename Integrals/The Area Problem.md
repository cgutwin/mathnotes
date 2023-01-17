---
tags:
 - MATH152/Lecture2
 - IntegralCalculus/ApproximationWithLimits
 - IntegralCalculus/AreaProblem
---

Areas for fixed shapes are easy. Areas for curved regions are more difficult.

## Method to approximate area of a curved region

>"We first approximate the region by rectangles and then we take the limit of the sum of the areas of the approximating rectangles as we increase the number of rectangles."

![[rectangle_approximation_upper_bound.bmp]]

Each subsection is divided into equal parts, in this case, $n=4$, where $n$ is the number of subdivided regions.

### Upper Bound of the Estimation

Each rectangle subsection has a width of $1\over{4}$ and the rightmost height of it's respective section:
$$\begin{align}

S_1 &= \frac{1}{4}\cdot\left(\frac{1}{4}\right)^2 \\
S_2 &= \frac{1}{4}\cdot\left(\frac{1}{2}\right)^2 \\
S_3 &= \frac{1}{4}\cdot\left(\frac{3}{4}\right)^2 \\
S_4 &= \frac{1}{4}\cdot\left(1\right)^2 \\
\end{align}$$

**The summation of the area of these rectangles is the approximation of the area under $x^2$**


==This is the upper bound: the estimation will be greater as there is extra area considered.==

###
### Lower Bound of the Estimation

The lower bound is calculated by taking the leftmost height of the rectangle:

![[rectangle_approx_lower_bound.bmp]]

$$\begin{align}

S_1 &= {\frac{1}{4}}\cdot0^2 \\
S_2 &= {\frac{1}{4}}\cdot\left({1\over4}\right)^2 \\
S_3 &= {\frac{1}{4}\cdot\left(1\over{2}\right)}^2 \\
S_4 &= {\frac{1}{4}\cdot\left(\frac{3}{4}\right)}^2
\end{align}$$

The summation of these areas is the lower bounds of the estimate.


###
The area of $x^2$ is bound by the upper and lower estimates. In this case:
$$0.21875 < A < 0.46875$$
For a larger number of subdivided rectangles, the estimates will become closer to the real value, up to a limit.

A good estimate is obtained by **averaging** the lower and upper bounds *with a decent size $n$.*

### In Conclusion
* As $y = f(x) = x^2$ is increasing over the interval in the examples, it impies the [[#Lower Bound of the Estimation]] is always less than or equal to the real area.
* The [[#Upper Bound of the Estimation]] will always be greater than or equal to the real value.
* Increasing the number of $n$ subintervals will decrease the [[#Upper Bound of the Estimation]] while increasing the [[#Lower Bound of the Estimation]].


## Approximation with Limits

From *[[#Method to approximate area of a curved region]]*, we can say the approximated sums $R_n$ approach $1\over3$:
$$\begin{align}
\lim\limits_{n \to \infty}{R_n} = \frac{1}{3}
\end{align}$$
==Where $R_n$ is the sum of the $n$ rectangles, *greedy*.==

Each rectangle has a width of $1\over{n}$ and the heights are the values of the function $f(x) = x^2$ at the points $1\over{n}$, $2\over{n}$ ,$3\over{n}$ ,$4\over{n}$, $\dots$  $n\over{n}$. 

**So, the heights would be $\left(\frac{1}{n}\right)^2$,  $\left(\frac{2}{n}\right)^2$, $\left(\frac{3}{n}\right)^2$, $\left(\frac{4}{n}\right)^2$, $\dots$ , $\left(\frac{n}{n}\right)^2$.**




So, $R_n$ would be the sum of $x\cdot f(x)$:
$$\begin{align}
R_n &= \frac{1}{n}\left(\frac{1}{n}\right)^2+\frac{1}{n}\left(\frac{2}{n}\right)^2+\frac{1}{n}\left(\frac{3}{n}\right)^2+\dots+\frac{1}{n}\left(\frac{n}{n}\right)^2 &&\text{The sums of areas of each section.}\\
&= \frac{1}{n}\cdot\frac{1}{n^2}\left(1^2+2^2+3^2+\dots+n^2\right) &&\text{Factor out }\frac{1}{n^2}\\
&= \frac{1}{n^3}\left(1^2+2^2+3^2+\dots+n^2\right)
\end{align}$$

So, with the formula for the sum of first $n$ positive integers:
$$\begin{align}
R_n &= \frac{1}{n^3}\cdot\frac{n\left(n+1\right)\left(2n+1\right)}{6}\\
&= \frac{\left(n+1\right)\left(2n+1\right)}{6n^2}
\end{align}$$
Thus
$$\begin{align}
\lim\limits_{n\to\infty} R_n &= \lim\limits_{n\to\infty} \frac{\left(n+1\right)\left(2n+1\right)}{6n^2}\\\\
&\dots\\\\
&= \frac{1}{6}\cdot1\cdot2\\
&= \frac{1}{3}
\end{align}$$

==The limit of $L_n$, the sum of the lower estimations at $n$, should equal the limit of $R_n$.==$$A = \lim\limits_{n\to\infty}R_n = \lim\limits_{n\to\infty}L_n = \frac{1}{3}$$

## Area in General

Where $n$ is an arbitrary number of subintervals over the global interval $\left[a,b\right]$

* $\Delta{x} = \frac{a-b}{n}$

### Rightbound Estimate

$$\begin{align}
A \approx R_n &= \Delta{x}\cdot\left(x_1\right)^2+\Delta{x}\cdot\left(x_2\right)^2+\Delta{x}\cdot\left(x_3\right)^2+\dots+\Delta{x}\cdot\left(x_n\right)^2 &&\text{The function is } y = f(x) = x^2\\
&= \Delta{x}\cdot\left({x_1}^2 + {x_2}^2 + {x_3}^2 + \dots + {x_i}^2\right)\\
\end{align}$$
### Leftbound Estimate

Same as [[#Rightbound Estimate]] except $x_i$ starts at $0$ and continues to $x_{n-1}$.

## Integral Limit

In computing the area, the following limit arises:

$$
\lim\limits_{n\to\infty}{\sum^{n}_{i=1}f(x^*_i)\cdot\Delta{x}} = \lim\limits_{n\to\infty}{\left[f(x^*_1)\cdot\Delta{x}+f(x^*_2)\cdot\Delta{x}+\dots+f(x^*_n)\cdot\Delta{x}\right]}
$$
Which is the sum areas of subdivided sections up to $i=n$.

This Riemann sum leads into the definition for the [[The Definite Integral#Definition of a Definite Integral|definite integral]].