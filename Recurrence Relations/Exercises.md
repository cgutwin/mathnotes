## Question 4
>[!question] Question 4
>Consider the recurrence $a_{n+1}=3a_n-a_{n-1}$ with $a_1=1, a_2=1$. Calculate $a_0, a_3, a_4$.

This recurrence states the next number in the sequence $a_{n+1}$ is equal to three times the current number, minus the previous value.

For $a_3$, it would be $3\times a_2 - a_1 = 3\times1-1 = 2$
For $a_4$, it would be $3\times a_3 - a_2 = 3\times2-1 = 5$

For $a_0$, we can slide the RR around, by adding 1 to each $a$
$$\begin{align}
a_{n+2} &= 3a_{n+1}-a_n\\
n&=0\\
\\
a_2&=3a_1-a_0 &&\text{Solve for }a_0\\
a_0&=3a_1-a_2\\
&=3(1)-1\\
\\
a_0&=2
\end{align}$$

## Question 7

### Part 1
On the first night, there are three eating choices:
Italian, French, or Brazilian.

On the second night, there are eight eating choices:
One was FF

I-I
I-F
I-B
F-I
F-B
B-I
B-F
B-B

On the third night, there are 22 options
5 were FF

I-I-I
I-I-F
I-I-B
I-F-I
I-F-B
I-B-I
I-B-F
I-B-B

F-I-I
F-I-F
F-I-B
F-B-I
F-B-F
F-B-B

B-I-I
B-I-F
B-I-B
B-F-I
B-F-B
B-B-I
B-B-F
B-B-B

on the fourth night, there are 60 options

I-I-I-I
I-I-F-I
I-I-B-I
I-F-I-I
I-F-B-I
I-B-I-I
I-B-F-I
I-B-B-I
I-I-I-F
I-I-B-F
I-F-I-F
I-F-B-F
I-B-I-F
I-B-B-F
I-I-I-B
I-I-F-B
I-I-B-B
I-F-I-B
I-F-B-B
I-B-I-B
I-B-F-B
I-B-B-B

F-I-I-I
F-I-F-I
F-I-B-I
F-B-I-I
F-B-F-I
F-B-B-I
F-I-I-F
F-I-B-F
F-B-I-F
F-B-B-F
F-I-I-B
F-I-F-B
F-I-B-B
F-B-I-B
F-B-F-B
F-B-B-B

B-I-I-I
B-I-F-I
B-I-B-I
B-F-I-I
B-F-B-I
B-B-I-I
B-B-F-I
B-B-B-I
B-I-I-F
B-I-B-F
B-F-I-F
B-F-B-F
B-B-I-F
B-B-B-F
B-I-I-B
B-I-F-B
B-I-B-B
B-F-I-B
B-F-B-B
B-B-I-B
B-B-F-B
B-B-B-B

### Part 2

A recurrence for $d_n$ would be $d_n = 2(d_{n-1}+d_{n-2})$ where $d_1 = 3, d_2=8, n\ge1$

### Part 3
d3 = 22
d4 = 60
d5 = 164