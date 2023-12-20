# JavaScript Sort Array By Parity

## Challenge:

Given an integer array `nums`, move all the even integers at the beginning of the array followed by all the odd integers.

Return any array that satisfies this condition.

### 1<sup>st</sup> Example:

`Input: nums = [3,1,2,4]`
<br/>
`Output: [2,4,3,1]`
<br/>
`Explanation: The outputs [4,2,3,1], [2,4,1,3], and [4,2,1,3] would also be accepted.`

### 2<sup>nd</sup> Example:

`Input: nums = [0]`
<br/>
`Output: [0]`

### Constraints:

`1 <= nums.length <= 5000`
<br/>
`0 <= nums[i] <= 5000`

## Solution:

`const sortArrayByParity = (nums) => {`
<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`let oddIndex = 0;`
<br/>
<br/>  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`for (let i = 0; i < nums.length; i++) {`
<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`if (nums[i] % 2 === 0) {`
<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`[nums[i], nums[oddIndex]] = [nums[oddIndex], nums[i]];`
<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`oddIndex++;`
<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}
<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`}`
<br/>
<br/>  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`return nums;`
<br/>
`};`
<br/>
<br/>

## Explanation:

I've coded a function called `sortArrayByParity` that takes an array of numbers, `nums`, as input. The purpose of this function is to rearrange the elements of the input array such that all even numbers appear before odd numbers, while maintaining the relative order of even and odd numbers within their respective groups.
<br/>

The function begins by initializing a variable called `oddIndex` with a value of `0`. This variable will keep track of the index where the next odd number should be placed in the array.
<br/>

Next, a `for` loop is used to iterate through each element of the input array. Within the loop, an `if` statement checks if the current number `(nums[i])` is even by checking if the remainder of dividing it by `2` is `0`.
<br/>

If the number is even, a destructuring assignment is used to swap the current number with the number at the `oddIndex`. This effectively moves the even number to its correct position in the array, ensuring that all even numbers appear before odd numbers.
<br/>

After the swap, the `oddIndex` is incremented by `1` to prepare for the next odd number that will be encountered.
<br/>

Once the loop finishes, the modified array is returned as the output of the function.
<br/>

In summary, this function rearranges the elements of the input array such that all even numbers come before odd numbers, while preserving the relative order of even and odd numbers within their respective groups.
<br/>
<br/>