## Example
$$
\int \frac{\cos x}{\sin^2x-\sin x} \, dx
$$
$$\begin{align}
&=\int \cos x \frac{1}{\sin x(\sin x-1)} \, dx &&\text{(1.1) Factor the denominator}\\
\\
&\text{Let }u=\sin x\\
&du=\cos x\ dx\\
&\vdots\\
&=\int  \frac{1}{u(u-1)}\, du
&&\text{(1.2) Use partial fractions}\\\\
&\int\frac{A}{u}+\frac{B}{u-1}\, du\\
1&=A(u-1)+B(u)&&\text{(1.3) By cross multiplying}\\
1&=B&&\text{(1.4) Let u = 1 to remove the A}\\
1&=A+2B\text{ where }B=1\\
1-2&=A=-1\\\\
&\therefore A=-1, B=1
\\
\\
\int \frac{A}{u}+\frac{B}{u-1} \, du &=\int -\frac{1}{u}+\frac{1}{u-1} \, du\\
&=-\ln|u|+\ln|u-1|+C\\
&=\ln|\sin x-1|-\ln|\sin x|+C\\
&=\ln|\frac{\sin x-1}{\sin x}|+C
\end{align}$$
