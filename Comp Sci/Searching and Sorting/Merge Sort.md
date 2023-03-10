Given an array of length $n$
1.  `let mid = n/2`
2. `mergeSort(array[0,mid])`
3. `mergeSort(array[mid+1,n]`
4. `merge(arrayleft, right)`

## Running Time
The function makes 2 recursive calls, on work divided into 2:
$T(n)=2T\left( \frac{n}{2} \right)+O(n)$


$$\begin{align}
&f(n) = O(n)\qquad a=2\qquad b=2\qquad c=\log_{2}2=1
\\
\\
&\text{Comparing }f(n)\text{ to }n^{\log_{2}2}=n^1=n\\
&\text{Since }f(n)=O(n)=O(n^1),\ T(n)=O(n\log n)
\end{align}$$


## The Merge Function

The function is $\Theta(n)$. We end up only touching $n$ elements where $n$ is the length of the array.

```java
public static void merge2(int[] array, int start, int mid, int end) {  
    // Get the left and right array pointers.  
    int leftLength = mid - start + 1;  
    int rightLength = end - mid;  
    // A temp array to put the merged elements in.  
    int[] temp = new int[end - start + 1];  
  
    int i = start, j = mid + 1;  
    int k = start;  
  
    // While one of the arrays still needs to be traversed  
    while (i < leftLength && j < rightLength) {  
        // If the element in the left is smaller than the right,
        // insert it...  
        if (array[i] <= array[j]) {  
            // ...then increment the left pointer. This is so
            // the next value on the left side of the array can
            //be compared to the first value in the right one.            
            temp[k++] = array[i++];  
        } else {  
            ///... else increment the right pointer, so the next 
            //on the right can be compared with the first in  
            // the left.
            temp[k++] = array[j++];
        }  
    }  
    // If there are remaining elements in either of the sides of
    // the array, push them back to the merged array.  
    // At least one of these statements will get skipped. The 
    // one that doesn't will contain values larger than    // 
    // the rest, so we can just copy them directly into the 
    // merged array.  
    while (i < leftLength) {  
        temp[k++] = array[i++];  
    }  
  
    while (j < rightLength) {  
        temp[k++] = array[j++];  
    }  
  
    // Move the temp array to the one we want to change.  
    System.arraycopy(temp, 0, array, start, k);  
}
```