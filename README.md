
Unit I: Sorting and Complexity Analysis
1. Bubble Sort Implementation (C)
Bubble Sort is a simple sorting algorithm that repeatedly steps through the list, compares adjacent elements, and swaps them if they are in the wrong order.
void bubbleSort(int arr[], int n) {
    int i, j, temp;
    for (i = 0; i < n - 1; i++) {
        for (j = 0; j < n - i - 1; j++) {
            if (arr[j] > arr[j + 1]) {
                // Swap elements
                temp = arr[j];
                arr[j] = arr[j + 1];
                arr[j + 1] = temp;
            }
        }
    }
}

2. Comparison of Sorting Algorithms
| Feature | Bubble Sort | Insertion Sort | Selection Sort |
|---|---|---|---|
| Worst Case Complexity | O(n^2) | O(n^2) | O(n^2) |
| Stability | Stable | Stable | Unstable |
| Adaptivity | Adaptive | Highly Adaptive | Non-Adaptive |
3. Binary Search vs. Linear Search
 * Linear Search: Checks every element sequentially. Time complexity: O(n).
 * Binary Search: Works on sorted arrays by repeatedly dividing the search interval in half. Time complexity: O(\log n).
 * Why faster? Because it eliminates half of the remaining elements in every step, making it significantly more efficient for large datasets.
4. Asymptotic Notations
 * Big-O (O): Represents the upper bound (Worst case).
 * Omega (\Omega): Represents the lower bound (Best case).
 * Theta (\Theta): Represents the tight bound (Average case).
Unit II: Stacks and Queues
1. Postfix Expression Evaluation
Postfix expressions are evaluated using a stack. Operands are pushed onto the stack, and when an operator is encountered, operands are popped to perform the calculation.
Example: 2 3 1 * + 9 -
 * Push 2, 3, 1.
 * Operator *: Pop 1 and 3. 3 \times 1 = 3. Push 3.
 * Operator +: Pop 3 and 2. 2 + 3 = 5. Push 5.
 * Push 9.
 * Operator -: Pop 9 and 5. 5 - 9 = -4.
   Result: -4
2. Stack as an ADT (Abstract Data Type)
A Stack is a LIFO (Last-In-First-Out) structure. The basic C structure for an array implementation is:
struct Stack {
    int items[MAX];
    int top;
};

Core Operations:
 * Push: Insert element at the top.
 * Pop: Remove element from the top.
 * Peek: View the top element without removing it.
3. Infix to Postfix Conversion
Expression: (A + B * C) / (D - E / F ^ G)
| Step | Token | Stack | Postfix Output |
|---|---|---|---|
| 1 | ( | ( |  |
| 2 | A | ( | A |
| 3 | + | (+ | A |
| 4 | B | (+ | AB |
| 5 | * | (+* | AB |
| 6 | C | (+* | ABC |
| 7 | ) |  | ABC*+ |
| 8 | / | / | ABC*+ |
| ... | ... | ... | ... |
Final Postfix: ABC*+DEFG^/- /
4. Types of Queues
 * Linear Queue: Follows FIFO. suffers from memory wastage (empty spaces at the front cannot be reused).
 * Circular Queue: The last position is connected back to the first position to make a circle, resolving memory wastage.
 * Priority Queue: Elements are removed based on their priority rather than just their order in the queue.
