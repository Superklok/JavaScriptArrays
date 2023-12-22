# JavaScript Transpose Matrix
<br/>

## Challenge
Given a 2D integer array `matrix`, return the transpose of `matrix`.

The transpose of a matrix is the matrix flipped over its main diagonal, switching the matrix's row and column indices.
<br/>
<br/>

### 1<sup>st</sup> Example

```JavaScript
Input: matrix = [[1,2,3],[4,5,6],[7,8,9]]
Output: [[1,4,7],[2,5,8],[3,6,9]]
```

### 2<sup>nd</sup> Example

```JavaScript
Input: matrix = [[1,2,3],[4,5,6]]
Output: [[1,4],[2,5],[3,6]]
```

<br/>

### Constraints

```JavaScript
m == matrix.length
n == matrix[i].length
1 <= m, n <= 1000
1 <= m * n <= 10⁵
-10⁹ <= matrix[i][j] <= 10⁹
```

<br/>

## Solution

```JavaScript
const transpose = (A) => {
    let result = [];

    for (let i= 0; i<A[0].length; i++) {
        let currentColumn = [];

        for (let j=0; j<A.length; j++) {
            currentColumn.push(A[j][i]);
        }

        result.push(currentColumn);
    }

    return result;
};
```

<br/>

## Explanation

I've defined a function called `transpose` that takes a matrix, represented by a 2-dimensional array, as input. The purpose of this function is to transpose the matrix, which means to swap the rows and columns, and return the transposed matrix.
<br/>

Inside the function, an empty array called `result` is created to store the transposed matrix.
<br/>

A `for` loop is used to iterate over the columns of the input matrix. This loop runs for the length of the first row of the matrix, assuming all rows have the same length.
<br/>

Inside the loop, a new empty array called `currentColumn` is created to store the current column of the transposed matrix.
<br/>

Another nested `for` loop is used to iterate over the rows of the input matrix. This loop runs for the length of the matrix.
<br/>

Inside the nested loop, the value at the current row and column of the input matrix is pushed into the `currentColumn` array.
<br/>

After the nested loop completes, the `currentColumn` array containing the transposed column is pushed into the `result` array.
<br/>

The outer loop continues until all columns of the input matrix are processed.
<br/>

Finally, the `result` array containing the transposed matrix is returned as the output of the function.
<br/>

In summary, this function transposes a given matrix by swapping the rows and columns. It achieves this by iterating over the columns and rows of the input matrix and constructing a new array representing the transposed matrix. The resulting transposed matrix is then returned as the output of the function.
<br/>
<br/>