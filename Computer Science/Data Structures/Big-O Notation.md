tags: #DataStructures #CS
# Time Complexity  `ris:Timer`
---
- How much time does my code take to run?
- This is also called ==asymptotic runtime== or Big O time.

## Big - O notation  $O(\log{N})$
- Computer scientists came up with a way to quantitatively measure the efficiency of a particular algorithm, this is called the Big - O Notation.
- It gives us an upper bound for complexity in the worst case, helping quantify performance when as input becomes arbitrarily large

### Different Big - O Values
**Time complexities:**
#### $O(1)$ constant time
- The loop takes the same amount of time to run regardless of the input size `n`

```c++
for( int i = 0; i < 10; i++ ) // This loop does not depend on n at all
```
![[Big-O Notation-1654429335428.jpeg|330]]

---

#### $O(\log{N})$ logarithmic time
- The loops runtime has logarithmic growth

Example: [[Binary Search]]
```c++
//returns the index of the number we want to find
low = 0;
high = n - 1;
while(low <= high)
{
	mid = (low + high) / 2;
	if(array[mid] == value)
		return mid;
	else if(array[mid] < value)
		lo = mid + 1;
	else if(array[mid] > value)
		hi = mid - 1;
	return -1; //value not found
}
```
![[Big-O Notation-1654429420298.jpeg|330]]

---

#### $O(n)$ Linear time
- The time taken by the loop increases linearly with n

```c++
for( int i = 0; i < n; i++ ) //time only depends on size of n
```

![[Big-O Notation-1654429434442.jpeg|330]]

---

#### $O(n\log{n})$