### Big O Notation

- Big O is a notation used to describe the computational complexity of a given algorithm.
- An algorithms computational complexity is comprised of two aspects: time complexity and space complexity.
- Time complexity is the amount of time an algorithm takes to finish running with respect to the size of its given input.
- Space complexity is the amount of memory allocated by an algorithm when it is run with respect to the size of its input.
- Time complexity is typically the aspect of an algorithms complexity that concerns programmers the most.
- Time complexity: as the size of input increases, how much longer does the algorithm take to run.
- Space complexity: as the the size of input increases, how much more memory does the algorithm use.

### How Complexity Works
- An algorithms complexity is described as a mathematical function.
- The arguments to the function are variabes defined by the programmer.
- Common arguments includes 'n', which denotes the length of an input array/string.
- Given the fact that n denotes the length of something variable in size, n itself will affect the complexity properties of the algorithm.
- When written, the mathematical function used to describe the algorithm exists in the following forms: 
  - O(n)
  - O(n^2)
  - O(2^n)
  - O(log n)
  - O(n * m)
- These functions represent the complexity of an algorithm.
- Each of the unique function forms can be used to describe time or space complexity.

### Calculating Complexity
- Roughly speaking, the function describing an algorithm calculates the number of operations or amount of memory it consumes relative to its input size.
- Time complexity is not meant to be an exact representation of number of operations.
- The primary aim of time complexity is to describe how the number of operations changes as the input changes.
- Rule one: ignore constants - thus O(999n) = O(8n) = O(n) = O(n/500).
- Constants are ignored because they are not relevant for determining how an algorithm scales (they are always O(n)).
- O(n) is: algorithm A determines and returns the largest n in an array, and is O(n) because for each additional item in the array, the algorithm will run 'additional item' amount of times more. More specifically, for each n increase in elements in the array, the algorithm will run n more times.
- The point of complexity is to analyze the algorithm as the input changes.
- What matters is the nature of how the number of operations needed to run changes with respect to input.
- Rule two: complexity is considered as variables tend to infinity.
- With an algorithm that requires n + 500 operations, it has a time complexity of O(n), and when n is small, the +500 is significant, but as n approaches infinity, the +500 becomes insignificant, thus complexity analysis is to be performed as if n is tending toward infinity.
- The best complexity possible is O(1), called constant time/space. In this case, the algorithm always uses the same amount of resources regardless of the input.
- An algorithm of O(1) does not necessarily mean that the algorithm is fast, it simply means that its runtime is independent on the size of its input.
- In the context of complexity, there are three types of cases: best case, average case, worst case.
- Most of the time, algorithms complexity will be the same across all cases, but sometimes they are different.
- Worst case complexity is the standard typically used when assessing algorithms.

### Analyzing Time Complexity
'''  
  let x: [i32; 5] = [1, 2, 3, 4, 5]; 

  for i in x.iter() {
    println!(i);
  }
'''
- Time complexity: O(n).
- Print costs O(1).
- Printing is an O(1) operation as it will always only run once regardless of what the algorithms input is.
- The for loop interates n times.
- With each increase in size for x, the for loop will then run 'n increase in size' amount of times.
- If x is size 6, the for loop will run 6 times.
- Thus the for loop is dependant on the size of the input.
- The for loop scales in amount of operations with/as x increases in size.
- The amount of times the for loop will run is equivalent to 1 * n.
- This is because the for loop runs once for each n in x.
- Thus the time complexity of the for loop is O(1*n), which simplifies to O(n).
- The algorithms time complexity is O(n).


