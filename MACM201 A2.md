## (+) Determine the coefficient of
### $x^2y^3z^2$ in $(x+y+z)^7$

$$\begin{align}
n &= 5\\
x &= k_1 = 2\\
y &= k_2 = 3\\
z &= k_3 = 2\\
\\
{7\choose2, 3, 2} &= \frac{5!}{2!\times3!\times2!}\\
&=\frac{5\times\not4\times3\times\not2}{\not2\times\not3\times\not2\times\not2}\\
&=5\times3\\
&=15
\end{align}$$

### $x^2y^3z^2$ in $(x+2y+z)^7$


## Q2
> In how many ways can we distribute 10 apples to 4 people named Alice, Bob, Cathy, Devon, such that each person gets at least one apple?
## (+) Q3
> How many ways are there to distribute 5 muffins and 4 bagels to Alice, Bob, and Cathy?

|People |Muffins $(x_n)$|Bagels $(y_n)$|
|-|-|-|
|(1) Alice|2|1|
|(2) Bob|2|2
|(3) Cathy|1|1|

Let x = muffins, y = bagels

$x_1 + x_2 + x_3 = 5$ and $y_1+y_2+y_3=4$

Number of solutions ${3+5-1\choose5}\times{3+4-1\choose4}$.

## Q4
> Zara, Jonah, Sarita, and Jack buy a bag of Halloween candy containing 100 chocolate bars. Zara and Jonah together went to the store to buy the bag, so they feel they deserve at least  10 chocolate bars each. How many ways can they divide up the chocolate bars subject to this  condition (assume the chocolate bars are all the same)?


## (+) Q5
For a positive integer n, what is the value of the counter after the following code has been executed?

```c
int i,j,k;  
int counter = 0;  
for(i=1; i<=n; i++)  
	for(j=1; j<=i; j++)  
		for( k=1; k<=j; k++)  
			counter++;
```

```js
let counter = 0

for (let i = 1; i <= n; i++) {
  for (let j = i; j <= n; j++) {
    for (let k = j; k <= n; k++) {
      counter++
    }
  }
}
```

$i \le j \le k \le n$

Which is selections of size 3 that are from 1->n = ${n+3-1\choose3} = {n+2\choose3}$.
## Q6
