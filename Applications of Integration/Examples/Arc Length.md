## Find the exact length of

### $f(x)=\ln(sec(x))$ from $0\le x \le \frac{\pi}{4}$

$$\begin{align}
L &=\int_{0}^{\pi/4}\sqrt{ 1+\left( \frac{dy}{dx} \right)^2 }dx \\\\
\frac{dy}{dx} &= \frac{1}{\sec(x)}\cdot\frac{d}{dx}\sec x \\
&=\frac{1}{\sec x}\cdot\sec x\tan x \\
&=\tan x\\ \\

L&=\sqrt{ 1+(\tan^2x) }dx \\
&=\int_{0}^{\pi/4} \sqrt{ \sec^2 x } \, dx \\
&= \int_{0}^{\pi/4} |\sec x| \, dx  \\
&= \ln|\sec x + \tan x| \Bigr]_{0}^{\pi/4} \\
&=\ln|\sqrt{ 2 }+1|-\ln|1-0| \\
&=\ln \sqrt{ 2 }+1 \\
&&\square
\end{align}$$
### $x^\left( \frac{2}{3} \right)+y^\left( \frac{2}{3} \right)=1$

As the function represents an asteroid, we can find the arc length between 0 and 1 in the first quadrant, and multiply it by 4. All results will not need absolute value as all will be positive anyways.

![[b92db4f1b9ec9e8ef9d170219e6e93.gif| center]]

$$\begin{align}
f(x)&=\left( 1-x^\left( \frac{2}{3} \right) \right)^\left( \frac{3}{2} \right) \\
L&=4*\int_{0}^{1} \sqrt{ 1+\left( \frac{dy}{dx} \right)^2 } \, dx  \\ \\ \\
\frac{dy}{dx}&=\frac{3}{2}\left( 1-x^\left( \frac{2}{3} \right) \right)^\left( \frac{1}{3} \right)\cdot \frac{2}{3}x^\left( -\frac{1}{3} \right) \\
&=\frac{\sqrt{1-x^\left( \frac{2}{3} \right)}}{\sqrt[3]{x}} \\ \\
L&=4\cdot \int_{0}^{1} \sqrt{ 1+ \left(\frac{\sqrt{1-x^\left( \frac{2}{3} \right)}}{\sqrt[3]{x}}\right)^2}\, dx  \\
&=4\int_{0}^{1} \sqrt{1+\frac{1-x^\left( \frac{2}{3} \right)}{x^\left( \frac{2}{3} \right)} }  \, dx  \\
&=4\int_{0}^{1} 1\ dx+\int_{0}^{1} \frac{1}{x^\left( \frac{2}{3} \right)}\ dx-\int_{0}^{1} 1\ dx \\
&=4\cdot \frac{3}{2}x^{2/3}\Bigg]_{0}^1 \\
&=6

\end{align}$$