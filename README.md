# Diagonal-Star-Pattern

This program will produce the desired diagonal star pattern, shifting down and then back up, forming a mirrored pattern. Here’s the corrected code to achieve this:

### C Program for Diagonal Star Pattern

```c
#include <stdio.h>

int main() {
    int i, j, n;
    printf("Enter the number of rows: ");
    scanf("%d", &n);

    // Upper part of the pattern (including the middle row)
    for (i = 0; i < n; i++) {
        for (j = 0; j < i; j++) {
            printf(" ");
        }
        printf("*\n");
    }

    // Lower part of the pattern (excluding the middle row)
    for (i = n - 2; i >= 0; i--) {
        for (j = 0; j < i; j++) {
            printf(" ");
        }
        printf("*\n");
    }

    return 0;
}
```

### Explanation:

1. **Input Handling:**
   - The user inputs the value `n`, which represents the number of rows for the upper part of the pattern (including the middle row).

2. **Upper Part of the Pattern:**
   - The outer loop `for (i = 0; i < n; i++)` iterates from `0` to `n-1`.
   - The inner loop `for (j = 0; j < i; j++)` prints leading spaces, increasing with each row.
   - After printing the leading spaces, the program prints a single star (`*`) followed by a newline.

3. **Lower Part of the Pattern:**
   - The outer loop `for (i = n - 2; i >= 0; i--)` iterates from `n-2` down to `0`.
   - The inner loop `for (j = 0; j < i; j++)` prints leading spaces, decreasing with each row.
   - After printing the leading spaces, the program prints a single star (`*`) followed by a newline.

### Result:

If the user inputs `10`, the program will generate the following pattern:

```
*
 *
  *
   *
    *
     *
      *
       *
        *
         *
        *
       *
      *
     *
    *
   *
  *
 *
*
```
