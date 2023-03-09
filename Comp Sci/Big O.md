## Formal Definition
### Big O
- The *fastest increasing term* for large inputs

## Master Theorem

Given a recurrence relation $T(n) = a*T\left( \frac{n}{b} \right)+f(n)$ for $a,b \in \Bbb{I}$, and some function $f$.

Let $c=\log_{b}(a)$

Then
1. If $f(n) = O(n^d)$ for some $d\lt c$, then $T(n) = \Theta(n^c)$.
2. If $f(n)=\Theta(n^c)$, then $T(n) = \Theta(n^c\log n)$.
3. If $f(n)=\Omega(n^d)$ for some $d\gt c$, then $T(n) = \Theta(f)$.

### Examples
___
#### $T(n)=2T\left( \frac{n}{2} \right)+O(1)$
$f(n)=O(1)\qquad a = 2\qquad b=2\qquad c=\log_{2}2=1$

We compare $f(n)$ to $n^{\log_2 2} = n^1 = n$.

Since $f(n)$ is $O(1) = O(n^0)$, where $d < c$, and $n^{\log_b a}$ is equal to $n$, apply part one of the [[#Master Theorem]].
- $T(n)=\Theta(n)$
- $T(n) = O(n\log n)$


___
#### $T(n)=2T\left( \frac{n}{2} \right)+\Theta(n)$
$f(n)=\Theta(n)\qquad a = 2\qquad b=2\qquad c=\log_{2}2=1$

We compare $f(n)$ to $n^{\log_{2}2}=n^1=n$.

Since $F(n)=\Theta(n) = \Theta(n^1)$, we can apply [[#Master Theorem]] part 2:
- $T(n)=\Theta(n\log n)$.
___
#### $T(n) = 3T\left( \frac{n}{2} \right)+3n^2$
$f(n)=3n^2\qquad a = 3\qquad b=2\qquad c=\log_{2}3$

We compare $f(n) = 3n^2$ to $n^c = n^{\log_{2}3}$

$\log_{b}a = \log_{2}3<d=2$
$f(n) = \Omega(n^2)$, where $d = 2$.

So it follows from the [[#Master Theorem]] part 3:
$T(n) = \Theta(f(n))=\Theta(n^2)$.

___
#### $T(n)= 4T\left( \frac{n}{2} \right)+4n^{3/2}$
$f(n)=4n^{3/2}\qquad a = 4\qquad b=2\qquad c=\log_{2}4$

Compare $f(n) = 4n^{\frac{2}{3}}$ to $c =\log_{2}4$

Since $f(n)$ is $O(n^{2/3})$ where $d \lt c$, we can apply part 1
- $T(n) = \Theta({n^{2}})$.
___
### $T(n) = 3T\left( \frac{n}{3} \right)+5n$
$f(n)=5n\qquad a = 3\qquad b=3\qquad c=\log_{3}3 = 1$

Compare $f(n) = 5n$ to $c = 1$
Since $f(n) = \Theta(n^1), d = 1$, then by part 2
- $f(n)=\Theta(n\log n)$
___

### $T(n) = 4T\left( \frac{n}{3} \right)+5n$
$f(n)=5n\qquad a = 4\qquad b=3\qquad c=\log_{3}4$

We compare $f(n) = 5n$ to $n^{\log_{3}4}$
As $c < d$, we apply part 1:
- $f(n)=\Theta(n^{\log_{3}4})$
---

## Examples
### 1
Suppose $f(n)=2^n$ and $g(n)=3^n$. Is it true that $f=\Theta(g)$?

$$\begin{align}
0\ge\lim_{ N \to \infty }{\frac{f(N)}{g(N)}}&\lt\infty \\
&=\frac{f(\infty)}{g(\infty)} \\
&=\frac{2^\infty}{3^\infty}=0
\end{align}$$

OR

$f(n) = O(g(n))$ and $f(n) = \Omega(g(n))$

We only need to prove one side of the inequality false for the functions to not be true.
$$
\begin{align}
&c_{2}\cdot g(n)\le f(n)\le c_{1}\cdot g(n)\\
&c_{2}3^n\le 2^n\le c_{1}3^n\\
&\text{There are no such constants }c_{1},c_{2}\text{ s.t. }f(n)\text{ is between } c_x g(n). 
\end{align}
$$