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

