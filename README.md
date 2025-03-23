QN 1

1. Constant Time – O(1):

An algorithm runs in constant time if its execution time does not depend on the size of the input.

Example: Accessing an element in an array by its index.


int arr[] = {1, 2, 3, 4};
int x = arr[2]; // O(1)
Logarithmic Time – O(log n):

2.  An algorithm runs in logarithmic time when the number of operations needed increases logarithmically with the size of the input.

Example: Binary search in a sorted array.

int binarySearch(int[] arr, int target) {
    int low = 0, high = arr.length - 1;
    while (low <= high) {
        int mid = (low + high) / 2;
        if (arr[mid] == target) return mid;
        else if (arr[mid] < target) low = mid + 1;
        else high = mid - 1;
    }
    return -1; // O(log n)
}
3.   Linear Time – O(n):

An algorithm runs in linear time if the number of operations grows directly in proportion to the input size.

Example: Traversing an array.

for (int i = 0; i < arr.length; i++) {
    System.out.println(arr[i]); // O(n)
}
Quadratic Time – O(n²):

4.   An algorithm runs in quadratic time when the number of operations grows quadratically as the input size increases.

Example: Nested loops over an array.

for (int i = 0; i < arr.length; i++) {
    for (int j = 0; j < arr.length; j++) {
        System.out.println(arr[i] + arr[j]); // O(n²)
    }
}
5.  Exponential Time – O(2^n):

An algorithm runs in exponential time when the time required grows exponentially with the input size.

Example: Solving the traveling salesman problem using brute force.


// Imagine a function that explores every possible permutation of cities



QN 2

  Aspect	                                 Arrays	                                                                                      Linked Lists
Memory Allocation	-      Arrays allocate memory in contiguous blocks.	-                                              Linked lists allocate memory non-contiguously, one block at a time for each node.
Performance	-            Access time is fast due to direct indexing (O(1)).	-                                        Access time is slower as it requires traversal (O(n)).
Insertion/Deletion	-    Insertion and deletion are slow as elements may need to be shifted (O(n) in worst case).	-  Insertion and deletion are efficient (O(1) for beginning/end) as only pointers need to be adjusted.
