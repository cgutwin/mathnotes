	## Solving in General

1. Look for an expression in the integral from the table of substitutions
2. Let x be the substitution, and factor out the a value
3. Replace the trig function with the corresponding identity and square root it
4. In the original integral, replace variables with definitions from steps 2 and 4.
5. Simplify and find antiderivative.
6. If the limits of integration didnt change, return the original x by using the trianle associated with the substitution above.

## Table of Substitutions

|Expression|Substitution|Identity|
|-|-|-|
|$\sqrt{a^2-x^2}$|$x=a\sin\theta,\qquad -{\pi\over2}\le\theta\le{\pi\over2}$|$1-\sin^2\theta=\cos^2\theta$|
|$\sqrt{a^2+x^2}$|$x=a\tan\theta,\qquad -{\pi\over2}\lt\theta\lt{\pi\over2}$|$1+\tan^2\theta=\sec^2\theta$|
|$\sqrt{x^2-a^2}$|$x=a\sec\theta,\qquad 0\le\theta\lt{\pi\over2}\text{ or }\pi\le\theta\lt{3\pi\over2}$|$\sec^2\theta-1=\tan^2\theta$|

## Example 1

>[!question] Example 1
>Evaluate $$\int\frac{\sqrt{9-x^2}}{x^2}dx$$

Let $x = 3\sin\theta$, then $dx = 3\cos\theta\ d\theta$.

$$\begin{align}
\sqrt{9-x^2}&=\sqrt{9-9\sin^2\theta} &&\text{Sub for x and square}\\
&=\sqrt{9-9\left(1-\cos^2\theta\right)} &&\text{Replace with identity}\\
&=\sqrt{9\cos^2\theta} &&\text{Expand and simplify}\\
&=3|\cos\theta|&&\text{Square root everything}\\
&= 3\cos\theta&&\text{No need for abs as between pos values}
\end{align}$$
So
$$\begin{align}
\int\frac{\sqrt{9-x^2}}{x^2}dx &= \int\frac{3\cos\theta}{9\sin^2\theta}\cdot3\cos\theta\ d\theta\\
&=\int\frac{9\cos^2\theta}{9\sin^2\theta}\ d\theta\\
&=\int\frac{\cos^2\theta}{\sin^2\theta}\ d\theta\\
&=\int\cot^2\theta\ d\theta\\
&=\int\left(\csc^2\theta-1\right)\ d\theta\\
&=-\cot\theta-\theta+C
\end{align}$$

Since this was an indefinite integral, ==we return to the original variable x==.

Draw a picture. From above, $\sin\theta = {x\over3}$:
![[8swcm24r.bmp|center]]
So $cot\theta = \frac{\sqrt{9-x^2}}{x}$, and since $sin\theta = {x\over3}, \theta=\arcsin{x\over3}$.

Returning the variables:
$$\begin{align}
-\cot\theta-\theta+C &= -\frac{\sqrt{9-x^2}}{x}-\arcsin{x\over3}+C\\
&&\square
\end{align}$$

## Example 2

>[!question] Example 2
>Find the area enclosed by the ellipse $${x^2\over a^2}-{y^2\over b^2}=1$$

Solve for y, which yields
$$\begin{align}
{y^2\over b^2}&=1-{x^2\over a^2}\\
\\
&=\frac{a^2-x^2}{a^2}\\
\\
&\text{or}\\
\\
y&=\pm{b\over a}\sqrt{a^2-x^2}
\end{align}$$

As the ellipse is symettric with respect to both axes, the total area is four times the area in the first quadrant:
![[ld96gy85.bmp|center]]
So the ellipse in the first quadrant is expressed as $y={b\over a}\sqrt{a^2-x^2} \quad 0\le x\le a$

So ${1\over4}A = \int_0^a {b\over a}\sqrt{a^2-x^2}\ dx$.

To evaluate, we substitute $x = a\sin\theta, dx = a\cos\theta\ d\theta$.
==The limits of integration change:==
$$\begin{align}
\text{When } x = 0\\
\\
0&=a\sin\theta\\
\sin\theta&=0\\
\\
\text{so }\theta=0\\
\\
\text{When }x=a\\
\\
a&=a\sin\theta\\
1&=\sin\theta\\
\\
\text{so }\theta={\pi\over2}
\end{align}$$

As in [[#Example 1]] it follows
$$\begin{align}
\sqrt{a^2-x^2}&=\sqrt{a^2-a^2\sin\theta}\\
&=\sqrt{a^2-a^2(1-cos^2\theta)}\\
&=\sqrt{a^2\cos^2\theta}\\
&=a|\cos\theta|\\
&=a\cos\theta
\end{align}$$

Therefore
$$\begin{align}
A&=4{b\over a}\int_0^a\sqrt{a^2-x^2}\ dx\\
&=4{b\over a}\int_0^{\pi\over2}a\cos\theta\cdot a\cos\theta\ d\theta\\
&=4ab\int_0^{\pi\over2}\cos^2\theta\ d\theta\\
&=4ab\int_0^{\pi\over2}{1\over2}(1+\cos2\theta)\ d\theta\\
&=2ab\left[\theta+{1\over2}\sin2\theta\right]_0^{\pi\over2}\\
&=2ab\left({\pi\over2}+0-0\right)\\
&=\pi ab
\end{align}$$

As we changed the limits of integration above, we don't need to return the original variable.
## Example 3

>[!question] Example 3
>Find $$\int\frac{1}{x^2\sqrt{x^2+4}}dx$$

Let $x=2\tan\theta$ then $dx = 2\sec^2\theta\ d\theta$.
So
$$\begin{align}
\sqrt{x^2+4}&=\sqrt{\left(2\tan\theta\right)^2+4}=\sqrt{4\tan^2\theta+4}\\
&=\sqrt{4(\tan^2\theta+1)}\\
&=\sqrt{4\sec^2\theta}\\
&=2|\sec\theta|\\
&=2\sec\theta
\end{align}$$
So
$$\begin{align}
\int\frac{1}{x^2\sqrt{x^2+4}}dx &=\int\frac{1}{4\tan^2\theta\cdot2\sec\theta}\cdot2\sec^2\theta\ d\theta\\
&={1\over4}\int\frac{\sec\theta}{\tan^2\theta}\ d\theta\\
&={1\over4}\int{1\over\cos\theta}\times{\cos^2\theta\over\sin^2\theta}\ d\theta\\
&={1\over4}\int{\cos\theta\over\sin^2\theta}\ d\theta\\
\\
\text{Let }u&=\sin\theta\\
du&=cos\theta\ d\theta\\
\\
&={1\over4}\int u^{-2}\ du\\
&={1\over4}\left(-{1\over u}\right)+C\\
&=-{1\over4\sin\theta}+C\\
&=-{1\over4}\cdot{1\over\sin\theta}+C\\
&=-{\csc\theta\over4}+C
\end{align}$$
From above, $\tan\theta = {x\over2}$
![[kvw87ce9.bmp|center]]
So $\csc\theta = {\sqrt{x^2+4}\over x}$

So
$$
\int\frac{1}{x^2\sqrt{x^2+4}}dx = -{\sqrt{x^2+4}\over4x}+C
$$
