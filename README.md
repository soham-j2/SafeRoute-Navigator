# Data Structures & Algorithms (DSA) - Course Work

This repository contains detailed solutions and explanations for core Data Structure concepts, focusing on **Unit I (Sorting & Complexity)** and **Unit II (Stacks & Queues)**.

---

## 🟢 Unit I: Sorting and Complexity Analysis

### 1. Bubble Sort Implementation (C)
Bubble Sort is a comparison-based algorithm that repeatedly swaps adjacent elements if they are in the wrong order.

```c
void bubbleSort(int arr[], int n) {
    for (int i = 0; i < n - 1; i++) {
        for (int j = 0; j < n - i - 1; j++) {
            if (arr[j] > arr[j + 1]) {
                int temp = arr[j];
                arr[j] = arr[j + 1];
                arr[j + 1] = temp;
            }
        }
    }
}
.
📂 Unit I: Sorting and Complexity Analysis
1. Bubble Sort Implementation (C)
Bubble Sort is a comparison-based algorithm where each pair of adjacent elements is compared and swapped if they are not in order.
#include <stdio.h>

void bubbleSort(int arr[], int n) {
    for (int i = 0; i < n - 1; i++) {
        // Last i elements are already in place
        for (int j = 0; j < n - i - 1; j++) {
            if (arr[j] > arr[j + 1]) {
                int temp = arr[j];
                arr[j] = arr[j + 1];
                arr[j + 1] = temp;
            }
        }
    }
}

2. Comparison Table
| Feature | Bubble Sort | Insertion Sort | Selection Sort |
|---|---|---|---|
| Worst Case | O(n^2) | O(n^2) | O(n^2) |
| Best Case | O(n) (Optimized) | O(n) | O(n^2) |
| Stability | Stable | Stable | Unstable |
| Adaptivity | Yes | Yes | No |
3. Binary Search vs. Linear Search
 * Linear Search: O(n) complexity. Scans every element.
 * Binary Search: O(log n) complexity. Requires a sorted array. It is faster because it follows the Divide and Conquer strategy, halving the search space in every step.
4. Asymptotic Notations
 * Big-O (O): Upper bound (Worst case).
 * Omega (\Omega): Lower bound (Best case).
 * Theta (\Theta): Tight bound (Average case).
📂 Unit II: Stacks and Queues
1. Stack: Definition and ADT
A Stack is an Abstract Data Type (ADT) that follows the LIFO (Last-In, First-Out) principle.
C Structure for Array Implementation:
struct Stack {
    int top; 
    unsigned capacity;
    int* array;
};

Key Operations:
 * Push: Adds an item to the top.
 * Pop: Removes an item from the top.
 * Peek: Returns the top item without removing it.
2. Postfix Evaluation
To evaluate a postfix expression like 2 3 1 * + 9 -:
 * Scan operands (2, 3, 1) and push to stack.
 * When * is hit: Pop 1 and 3, multiply (3 \times 1 = 3), push 3.
 * When + is hit: Pop 3 and 2, add (2 + 3 = 5), push 5.
 * Scan 9, push to stack.
 * When - is hit: Pop 9 and 5, subtract (5 - 9 = -4).
   Result: -4
3. Infix to Postfix Conversion
Expression: (A + B * C) / (D - E / F ^ G)
Result: ABC*+DEFG^/- /
4. Queue Variations
 * Linear Queue: Standard FIFO. Problem: "False Overflow" (space at front cannot be reused).
 * Circular Queue: Connects the last position back to the first. It solves the space wastage problem of linear queues.
 * Priority Queue: Each element has a priority. Elements with higher priority are served before lower priority ones, regardless of their position.
🚀 Usage
To run the C implementations:
 * Clone the repo: git clone https://github.com/yourusername/dsa-prep.git
 * Compile: gcc bubble_sort.c -o sort
 * Run: ./sort
Next Step: Would you like me to generate the similar Markdown content for Unit III (Linked Lists) and Unit IV (Trees)?
