### DS LAB-1
**Take input from user and create an array using pointers with `malloc` and `calloc`**
- `malloc` allocates memory without initialization.
- `calloc` allocates memory and initializes all elements to 0.

```c
#include <stdio.h>
#include <stdlib.h>
int main() {
    int *arr1, *arr2, n, i;
    printf("Enter number of elements: ");
    scanf("%d", &n);
    // Using malloc
    arr1 = (int*) malloc(n * sizeof(int));
    if (arr1 == NULL) {
        printf("Memory allocation failed using malloc.\n");
        return 1;
    }
    printf("Enter elements for malloc array:\n");
    for (i = 0; i < n; i++) {
        scanf("%d", &arr1[i]);
    }
    // Using calloc
    arr2 = (int*) calloc(n, sizeof(int));
    if (arr2 == NULL) {
        printf("Memory allocation failed using calloc.\n");
        return 1;
    }
    printf("Enter elements for calloc array:\n");
    for (i = 0; i < n; i++) {
        scanf("%d", &arr2[i]);
    }
    // Display arrays
    printf("Array using malloc:\n");
    for (i = 0; i < n; i++) {
        printf("%d ", arr1[i]);
    }
    printf("\nArray using calloc:\n");
    for (i = 0; i < n; i++) {
        printf("%d ", arr2[i]);
    }
    // Free the memory
    free(arr1);
    free(arr2);
    return 0;
}

```

___
### DS lecture
### **Definitions**:

- **Best Case**: The input scenario that requires the **minimum** number of operations.
- **Average Case**: Expected performance for **random input**. Calculated using probability.
- **Worst Case**: The input scenario that causes the **maximum** number of operations.

___
### MKLO converted to IDT
discussed the problems and their possible solutions 


___
### DS lab-2 

**Extend Lab-1 by reallocating memory and freeing it using `realloc()` and `free()`.**

```c
#include <stdio.h>
#include <stdlib.h>

int main() {
    int *arr, n, newSize, i;
    printf("Enter initial number of elements: ");
    scanf("%d", &n);
    arr = (int*) malloc(n * sizeof(int));
    if (arr == NULL) {
        printf("Memory allocation failed.\n");
        return 1;
    }
    printf("Enter %d elements:\n", n);
    for (i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }
    // Resize array using realloc
    printf("Enter new size of the array: ");
    scanf("%d", &newSize);
    arr = (int*) realloc(arr, newSize * sizeof(int));
    if (arr == NULL) {
        printf("Memory reallocation failed.\n");
        return 1;
    }
    if (newSize > n) {
        printf("Enter %d new elements:\n", newSize - n);
        for (i = n; i < newSize; i++) {
            scanf("%d", &arr[i]);
        }
    }
    printf("Final array:\n");
    for (i = 0; i < newSize; i++) {
        printf("%d ", arr[i]);
    }
    // Free memory
    free(arr);
    return 0;
}

```

| Concept   | Function                 | Purpose                          | Syantax                                     |
| --------- | ------------------------ | -------------------------------- | ------------------------------------------- |
| `malloc`  | `malloc(size)`           | Allocates memory (uninitialized) | (int*) malloc(n * sizeof(int));             |
| `calloc`  | `calloc(n, size)`        | Allocates and initializes to 0   | (int*) calloc(n * sizeof(int));             |
| `realloc` | `realloc(ptr, new_size)` | Changes memory size              | (int*) realloc(arr, newSize * sizeof(int)); |
| `free`    | `free(ptr)`              | Deallocates memory               | free(arr);                                  |
