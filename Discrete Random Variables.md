> Let $S$ be a sample space.
> 
- A random variable just takes elements from S and assigns a real number to them.

## Example 3.10
If S is the set of all binary sequences of size 4. The function that counts the number of 1's is a random variable.

X(0110) = 2 -> the number of 1's
X(1011) = 3

The range of X will be {1, 2, 3, 4}, as it can return up to 4 ones in the binary sequence.

## Example 3.11
If S is the set of all rolls of two dice.
The function that adds the values of the dice is a random variable.

Ex. Roll 1 = 1
Roll 2 = 3

X(Roll 1, Roll 2) = 1 + 3 = 4

The discrete random variable returns the sum of the two dice.

r(X) = {2, 3, 4, ..., 12} -> 2 is two ones, 12 is two sixes.

## Example 3.12
Suppose we throw m (distinguishable) balls into n (distinguishable) bins randomly. Let X be the number of empty bins.

X counts the number of empty bins in the sample space, so X is a random variable.

Let m = 5 (5 balls)
o o o o o

Let n = 4

Bin 1 gets balls 3 and 5, Bin 2 and 3 get none, but bin 4 gets balls 1, 2 and 4.

The random variables returns the number of empty bins, so X returns 2.

The smallest number of empty bins can be 0, all bins have a ball. The maximum can have 3 empty bins as all balls are in one bin (n-1) bins if m >= n.

r(x) = \[0, n-1] or r(x) \[n-m, n-1] if m < n.
##
- The range r(X) of X is the set of all values it can take.
- We can use random variables to describe events.