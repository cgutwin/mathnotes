## 1
$$
\int e^{-\theta}\cos{8\theta}\ d\theta
$$
This is an [[Indefinite Integrals By Parts]] question.

$$\begin{align}
\text{Let }u&=e^{-\theta}\\
dv&=\cos{8\theta}\ d\theta\\
du&=-e^{-\theta}\ d\theta\\
v &={1\over8}\sin{8\theta}\\
\\
\int e^{-\theta}\cos{8\theta}\ d\theta&=vu-\int v\ du\\
&={1\over8}e^{-\theta}\sin{8\theta}+{1\over8}\int\sin{8\theta}e^{-\theta}d\theta&&\text{(1)}\\
\end{align}$$

Integrate by parts again.
$$\begin{align}
\text{Let }u&=e^{-\theta}\\
dv&=\sin{8\theta}\ d\theta\\
du&=-e^{-\theta}\ d\theta\\
v &=-{1\over8}\cos{8\theta}\\
\\
\int\sin{8\theta}e^{-\theta}d\theta&=-{1\over8}e^{-\theta}\cos{8\theta}-{1\over8}\int e^{-\theta}\cos{8\theta}\ d\theta &&\text{(2)}
\end{align}$$

Substitute (2) into (1) and solve for the integral.

$$\begin{align}
\int e^{-\theta}\cos{8\theta}\ d\theta&={1\over8}e^{-\theta}\sin{8\theta}+{1\over8}\left[-{1\over8}e^{-\theta}\cos{8\theta}-{1\over8}\int e^{-\theta}\cos{8\theta}\ d\theta\right]\\
&={1\over8}e^{-\theta}\sin{8\theta}+{1\over8}\cdot-{1\over8}\left[e^{-\theta}\cos{8\theta}+\int e^{-\theta}\cos{8\theta}\ d\theta\right]\\
&={1\over8}e^{-\theta}\sin{8\theta}-{1\over64}e^{-\theta}\cos{8\theta}-{1\over64}\int e^{-\theta}\cos{8\theta}\ d\theta\\
{64\over64}\int e^{-\theta}\cos{8\theta}\ d\theta+{1\over64}\int e^{-\theta}\cos{8\theta}\ d\theta &={1\over8}e^{-\theta}\sin{8\theta}-{1\over64}e^{-\theta}\cos{8\theta}+C\\
{65\over64}\int e^{-\theta}\cos{8\theta}\ d\theta&={1\over8}e^{-\theta}\sin{8\theta}-{1\over64}e^{-\theta}\cos{8\theta}+C\\
\int e^{-\theta}\cos{8\theta}\ d\theta&={8\over65}e^{-\theta}\sin{8\theta}-{1\over65}e^{-\theta}\cos{8\theta}+C\\
&&\square
\end{align}$$
