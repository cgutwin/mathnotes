## Formula for Integration By Parts

>[!abstract] Formula A
>$$
>\int f(x)g^\prime(x)\ \mathrm{dx} = f(x)\ g(x) - \int g(x)f^\prime(x)\ \mathrm{dx}
>$$

>[!abstract] Formula B
>Let $u = f(x)$ and $v = g(x)$. Then the differentials are $du=f^\prime(x)\mathrm{dx}$ and $dv=g^\prime(x)\mathrm{dx}$. The formula becomes
>
>$$\int u\ dv = uv - \int v\ du$$

- Aim to ==create a simpler integral than what is started with==.

## Example 1

>[!question] Example 1
>Find $\int x\ \sin{x}\ \mathrm{dx}$.

Let 
$u = x\quad dv=\sin{x}\ \mathrm{dx}\quad du = dx\quad dv = -\cos{x}$.

Then by [[#Formula for Integration By Parts|Formula B]] 
$$\begin{align}
\int x\ \sin{x}\ \mathrm{dx} &= x\cdot\left(-\cos{x}\right) - \int \left(-\cos{x}\right)\ \mathrm{dx}\\
&=-x\cos{x}+\int \cos{x}\ \mathrm{dx}\\
&=-x\cos{x}+\sin{x} + C\\
&&\square
\end{align}$$



## Example 2

>[!question] Example 2
>Find $\int \ln{x}\ \mathrm{dx}$.

Let
$u = \ln{x}\quad dv = dx\quad du={1\over x}\mathrm{dx}\quad v = x$

Then by [[#Formula for Integration By Parts|Formula B]]
$$\begin{align}
\int \ln{x}\ \mathrm{dx} &= x\ln{x} - \int x\cdot {1\over x}dx\\
&=x\ln{x}-\int dx\\
&=x\ln{x}-x+C\\
&&\square
\end{align}$$
## Example 3

>[!question] Example 3
>Find $\int t^2e^t\ dt$.

Let
$u = t^2\quad dv = e^t\ dt\quad du=2t\ dt\quad v = e^t$.

Then by [[#Formula for Integration By Parts|Formula B]]
$$\begin{align}
\int t^2 e^t\ dt &= t^2e^t-\int e^t\cdot 2t\ dt\\
&=t^2e^t-2\int te^t\ dt &&\text(3)\\
\end{align}$$
We can **use integration by parts again**
Let
$u = t\quad dv=e^t\ dt\quad du=dt\quad v = e^t$

Then by [[#Formula for Integration By Parts|Formula B]]
$$\begin{align}
\int te^t\ dt &= te^t-\int e^t\ dt\\
&= te^t-e^t+C&&\text{(4)}
\end{align}$$
Putting (4) into (3)
$$\begin{align}
\int t^2 e^t\ dt &= t^2e^t-2\left(te^t-e^t+C\right)\\
&=t^2e^t-2te^t-2e^t+C_1&&\text{ where }C_1 =-2C\\
&&&&\square
\end{align}$$
## Example 4

>[!question] Example 4
>Find $\int e^x\sin{x}\ dx$.

- $e^x$ nor $\sin{x}$ become easier when differentiating, just start:


Let
$u = e^x\quad dv=\sin{x}\ dx\quad du=e^x\ dx\quad v=-\cos{x}$

Then
$$\begin{align}
\int e^x\sin{x}\ dx &= -e^x\cos{x} +\int e^x\cos{x}\ dx&&\text{(5)}
\end{align}$$


**Integrate by parts again:**

Let
$u = e^x\quad dv = \cos{x}\ dx\quad du=e^x\ dx\quad v=\sin{x}$

Then
$$\begin{align}
\int e^x\cos{x}\ dx&=e^x\sin{x} - \int e^x\sin{x}\ dx&&\text{(6)}
\end{align}$$


==Now we have an expression for $\int e^x\cos{x}\ dx$ to plug into (5)==


$$\begin{align}
\int e^x\sin{x}\ dx &= -e^x\cos{x} + e^x\sin{x} - \int e^x\sin{x}\ dx\\
2\int e^x\sin{x}\ dx &= -e^x\cos{x} + e^x\sin{x}\\
\int e^x\sin{x}\ dx &= {1\over 2}e^x\left(\sin{x}-\cos{x}\right)+C\\
&&\square
\end{align}$$
