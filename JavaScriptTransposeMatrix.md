# JavaScript Transpose Matrix

## Challenge:

Given a 2D integer array `matrix`, return the transpose of `matrix`.

The transpose of a matrix is the matrix flipped over its main diagonal, switching the matrix's row and column indices.

### 1<sup>st</sup> Example:

`Input: matrix = [[1,2,3],[4,5,6],[7,8,9]]`
<br/>
`Output: [[1,4,7],[2,5,8],[3,6,9]]`

### 2<sup>nd</sup> Example:

`Input: matrix = [[1,2,3],[4,5,6]]`
<br/>
`Output: [[1,4],[2,5],[3,6]]`

### Constraints:

`m == matrix.length`
<br/>
`n == matrix[i].length`
<br/>
`1 <= m, n <= 1000`
<br/>
`1 <= m * n <= 10⁵`
<br/>
`-10⁹ <= matrix[i][j] <= 10⁹`

## Solution:

`const transpose = (A) => {`
<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`let result = [];`
<br/>
<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`for(let i= 0; i<A[0].length; i++){`
<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`let currentColumn = [];`
<br/>
<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`for(let j=0; j<A.length; j++){`
<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`currentColumn.push(A[j][i]);`
<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`}`
<br/>
<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`result.push(currentColumn);`
<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`}`
<br/>
<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`return result;`
<br/>
`};`
<br/>
<br/>

## Explanation:

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