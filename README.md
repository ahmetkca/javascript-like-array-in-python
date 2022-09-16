## Unpythonic way to work with Arrays, ... like JavaScript

the `Array` object resembles JavaScript Array. It support most of the function JavaScript provides for Arrays.

```python

from javascript_like_array import Array

arr: Array[int] = Array([1, 2, 3, 4, 5])

arr.forEach(lambda x: print(x, end=" ")) # Output: 1 2 3 4 5
arr # [1, 2, 3, 4, 5]

arr.map(lambda x: x**2).forEach(lambda x: print(x, end=" ")) # Output: 1 4 9 16 25
arr # [1, 2, 3, 4, 5]

arr.map(lambda x: 'a' * x).filter(lambda x: len(x) >= 3) # Resulting array: ['aaa', 'aaaa', 'aaaaa']
arr # [1, 2, 3, 4, 5]

arr.reduce(lambda acc, curr: acc + curr) # Output: 15
arr # [1, 2, 3, 4, 5]

arr.reduce(lambda acc, curr: acc + curr, 100) # Output: 115
arr # [1, 2, 3, 4, 5]

arr.reduceRight(lambda acc, curr: acc - curr) # Output: -5
arr # [1, 2, 3, 4, 5]

arr.length # Output: 5

arr.fill(99, 2) # Output: [1, 2, 99, 99, 99] Original array is mutated.
arr # [1, 2, 99, 99, 99]

arr.find(lambda x: x > 10) # Output: 99
arr # [1, 2, 99, 99, 99]

arr.find(lambda x: x > 100) # Output: None
arr # [1, 2, 99, 99, 99]

arr.indexOf(99) # Output: 2
arr # [1, 2, 99, 99, 99]

arr.indexOf(2, 2) # Output: -1
arr # [1, 2, 99, 99, 99]

arr.lastIndexOf(99) # Output: 4
arr # [1, 2, 99, 99, 99]

arr.lastIndexOf(99, 2) # Output: 2
arr # [1, 2, 99, 99, 99]

arr.push(100, 98) # Output: 7
arr # [1, 2, 99, 99, 99, 100, 98]

arr.findIndex(lambda x: x > 99) # Output: 5
arr # [1, 2, 99, 99, 99, 100, 98]

arr.pop() # Output: 98
arr # [1, 2, 99, 99, 99, 100]

arr.shift() # Output: 1
arr # [2, 99, 99, 99, 100]

arr.unshift(11, 12, 13) # Output: 8
arr # [11, 12, 13, 2, 99, 99, 99, 100]


```# javascript-like-array-in-python
