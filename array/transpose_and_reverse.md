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

