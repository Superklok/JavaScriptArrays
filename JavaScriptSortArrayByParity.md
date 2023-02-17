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