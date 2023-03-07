# Data Structures Easy to Advanced Course - Full Tutorial from a Google Engineer

## What is a data structure?

- a way of organizing data that way it can be accessed efficiently/effectively

## What is an abstract data type?

- provides an interface to which the data must adhere to. doesn't care about the language or how it's implemented

### Examples

| Abstraction | Description                                                 |
| ----------- | ----------------------------------------------------------- |
| List        | Dynamic Array/Linked List                                   |
| Queue       | Linked List based Queue/Array based Queue/Stack based Queue |
| Map         | Tree Map/Hash Map/Hash Table                                |

## Complexity Analysis

- how much time does the algo need to finish
- how much space does the algo need for computation
- Big O, we only care about the measurements when the input scales
  - Constant: O(1)
  - ogarithmic: O(log(n))
  - Linear: O(n)
  - Linearithmic: O(nlog(n))
  - Quadric: O(n^2)
  - Cubic: O(n^3)
  - Exponential: O(n^n), b > 1
  - Factorial: O(n!)

### Examples

```
a: = 1
b: = 2
c: = a + 5\*b

i: = 0
While i < n Do
i = i + 3
```

(these are O(n))

```
low: = 0
high: = n - 1
While low <= high Do
  mid: = (low + high) / 2
  If array[mid] == value: return mid
  Else If array[mid] < value: lo = mid + 1
  Else If array[mid] < value: hi = mid - 1

return -1 // Value not found
// O(log2(n)) the 2 is a subscript
```

```
i: = 0
While i < n Do
  j = 0
  While j < 3 * n Do
  j = 0
  While j < 2 * n Do
    j = j + 2
  i = i + 1

// we multiply loops at different levels and add loops that are at the same level
// so here we have f(n) = n * (3n + 2n) = 5n^2
// O(f(n)) = O(n^2)
```

```
i: = 0
While i < 3 * n Do
  j: = 10
  While j <= 50 Do
    j = j + 1
  j = 0
  While j < n*n*n Do
    j = j + 2
  i = i + 1
// f(n) = 3n * (40 + n^3/2) = 3n/40 + 3n^4/2
// O(f(n)) = O(n^4)
// idk where the division by 2 comes from, seems to be from j + 2 since this accelerates the calculation
```
