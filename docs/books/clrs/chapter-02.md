# Chapter 2 - Getting Started

## 2.1 - Insertion-Sort

### 2.1-1

> Example using Java (maybe I prefer it more than pseudocode).

```
import java.util.Arrays;

public class Main {
    
	public static void main(String[] args) {
		
		int[] stack = {31, 41, 59, 26, 41, 58};
		
		for (int j = 1; j < stack.length; j++) {
		    
		    int key = stack[j];
		    int i = j - 1;
		    
		    while(i > -1 && stack[i] > key) {
		        stack[i + 1] = stack[i];
		        i = i - 1;
		    }
		    
		    stack[i + 1] = key;
		}
		
		System.out.println(Arrays.toString(stack));
	}
}
```

### 2.1-2

> Example using Java.

```
import java.util.Arrays;

public class Main {
    
	public static void main(String[] args) {
		
		int[] stack = {31, 41, 59, 26, 41, 58};
		
		for (int j = 1; j < stack.length; j++) {
		    
		    int key = stack[j];
		    int i = j - 1;
		    
		    while(i > -1 && stack[i] < key) {
		        stack[i + 1] = stack[i];
		        i = i - 1;
		    }
		    
		    stack[i + 1] = key;
		}
		
		System.out.println(Arrays.toString(stack));
	}
}
```

### 2.1-3

Using pseudocode.

```
LINEAR-SEARCH(A, v)
    for i = 1 to A.length
        if A[i] == v
            return i 
    return NIL
```

**Initialization:** before the first iteration, the invariant is true because we have not examined any elements.

**Maintenance:** if the invariant is true at the beginning of an iteration, it remains true after the iteration (or the algorithm returns).

**Termination:** when the loop ends, the invariant guarantees that v is not in `A[1..A.length]`, so returning NIL is correct.

### 2.1-4

> Pending...

## 2.2 - Algorithms Analysis

### Notes

Analysis from Insertion-Sort

- The time depends on input.

- Sort 1000 items != Sort 3 items.

- Is tradctional explain the execution time in function of the size input.

- **Size Input:** depends on the problem. The measurement is the number of items on input, as *n* of the Insertion-Sort. Also is possible to be the total number of bits. There are other cases.

- **Execution Time:** number of primitive operations or "steps" executed. Each step must be the more independent possible. In RAM model, we consider each line with a constant execution time.

- The execution time of the algorithm is the sum of the execution time for each instruction executed.

Order of Growth

- The focus is as the execution time grows; your rate grows.

- Remove the lowest order terms and constant coefficient of the initial term: an^2 => Θ(n^2), tetha notation of the execution time for worst case.

- An algorithm is more efficient than another if its order of growth is smaller.

### 2.2-1

> Pending...

### 2.2-2

> Pending...

### 2.2-3

> Pending...

### 2.2-4

> Pending...

## 2.3 - Algorithms Project

### Notes

The Divider to Conquer Approach

- There are many recursive algorithms. In general, they follow the "Divider to Conquer" approach: break the problem down into smaller problems and then combine the solutions to create a solution to the original problem.

- Three steps: **division, conquer and combination**.

- Here we use the Merge-Sorting.