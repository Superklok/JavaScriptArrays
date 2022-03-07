# JavaScript Two Sum

## Challenge:

Given an array of integers `nums` and an integer `target`, return indices of the two numbers such that they add up to `target`.

You may assume that each input would have exactly one solution, and you may not use the same element twice.

You can return the answer in any order.

### 1<sup>st</sup> Example:

`Input: nums = [2,7,11,15], target = 9`
<br/>
`Output: [0,1]`
<br/>
`Explanation: Because nums[0] + nums[1] == 9, we return [0, 1].`

### 2<sup>nd</sup> Example:

`Input: nums = [3,2,4], target = 6`
<br/>
`Output: [1,2]`

### 3<sup>rd</sup> Example:

`Input: nums = [3,3], target = 6`
<br/>
`Output: [0,1]`

### Constraints:

`2 <= nums.length <= 10⁴`
<br/>
`-10⁹ <= nums[i] <= 10⁹`
<br/>
`-10⁹ <= target <= 10⁹`
<br/>
Only one valid answer exists.

## Solution:

`const twoSum = (nums, target) => {`
<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`let numsObject = {};`
<br/>
<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`for(let i = 0; i < nums.length; i++) {`
<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`let n = nums[i],`
<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`compliment = target-n;`
<br/>
<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`if (numsObject.hasOwnProperty(compliment)) {`
<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`return [i,numsObject[compliment]];`
<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`}`
<br/>
<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`numsObject[n] = i;`
<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`}`
<br/>
<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`return [-1,-1];`
<br/>
`};`
<br/>
<br/>