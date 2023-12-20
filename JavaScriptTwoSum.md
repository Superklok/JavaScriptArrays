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

## Explanation:

I've built a function called `twoSum` that takes in an array of numbers (`nums`) and a target number. The purpose of this function is to find a pair of numbers in the array that add up to the target and return their indices in an array. If no such pair is found, it returns `[-1, -1]`.
<br/>

Inside the function, an empty object called `numsObject` is initialized.
<br/>

A `for` loop is used to iterate through each element in the `nums` array. Within the loop, the current element is assigned to a variable `n`, and the difference between the target and `n` is calculated and assigned to a variable `compliment`.
<br/>

An `if` statement checks if the `numsObject` object has a property with the value of `compliment`. If such a property exists, it means that a pair of numbers that add up to the target has been found.
<br/>

In this case, the function returns an array containing the current index ( `i` ) and the index of the compliment in the `numsObject` object.
<br/>

If the compliment property does not exist, it means that the current number has not been encountered before. In that case, the current number (`n`) is added as a property to the `numsObject` object, with the value of the current index (`i`).
<br/>

After the loop finishes, if no pair of numbers that add up to the target is found, the function returns `[-1, -1]`.
<br/>

In summary, this function searches for a pair of numbers in the input array that add up to the target. It uses an object to store previously encountered numbers and their indices. The function iterates through the array, checking if the compliment of each number exists in the object. If a pair is found, their indices are returned. If no pair is found, `[-1, -1]` is returned.
<br/>
<br/>