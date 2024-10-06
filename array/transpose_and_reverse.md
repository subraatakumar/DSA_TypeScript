## Problem Statement: Transpose and Reverse Columns of a Matrix

#### Objective: Write a function that takes a 2-dimensional square matrix as input and modifies it in place to achieve the following:

- Transpose the Matrix: Convert rows to columns, such that the element at position (i, j) in the original matrix becomes the element at position (j, i) in the transposed matrix.
- Reverse Each Column: After transposing, reverse the elements in each column of the transposed matrix.

#### Requirements:

- The function should not use any additional data structures (no third array).
- The operation should be performed directly on the input matrix.

#### Input:

- A 2D array of numbers (square matrix), where matrix[i][j] represents the element in the i-th row and j-th column.

#### Output:

- The function modifies the input matrix in place to reflect the transposed and column-reversed matrix.

#### Example:

- Input:

```typescript
const matrix = [
    [8, 2, 3],
    [2, 9, 1],
    [9, 0, 6]
];
```

- Output:

```typescript
matrix = [
    [3, 1, 6],
    [2, 9, 0],
    [8, 2, 9]
];
```

#### Constraints:

- The matrix will always be square (number of rows equals number of columns).

#### Function Signature:

```typescript
function transposeAndReverseColumnsInPlace(matrix: number[][]): void {
    // Implementation
}
```

# Solution

```ts
function transposeAndReverseColumnsInPlace(matrix: number[][]): void {
    const rows = matrix.length;
    const cols = matrix[0].length;

    // Step 1: Transpose the matrix in place
    for (let i = 0; i < rows; i++) {
        for (let j = i + 1; j < cols; j++) {
            // Swap matrix[i][j] with matrix[j][i]
            [matrix[i][j], matrix[j][i]] = [matrix[j][i], matrix[i][j]];
        }
    }

    console.log("transposed:", matrix)

    // Step 2: Reverse each column in place
    for (let col = 0; col < cols; col++) {
        for (let row = 0; row < Math.floor(rows / 2); row++) {
            // Swap the top and bottom elements within the same column
            [matrix[row][col], matrix[rows - row - 1][col]] = 
                [matrix[rows - row - 1][col], matrix[row][col]];
        }
    }
}

// Example usage
const matrix = [
    [8, 2, 3],
    [2, 9, 1],
    [9, 0, 6]
];

transposeAndReverseColumnsInPlace(matrix);

console.log(matrix);
```
