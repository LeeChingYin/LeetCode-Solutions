Given an array of integers, return indices of the two numbers such that they add up to a specific target.

You may assume that each input would have exactly one solution, and you may not use the same element twice.


Example

Given nums = [2, 7, 11, 15], target = 9,

Because nums[0] + nums[1] = 2 + 7 = 9,
return [0, 1].


思路：
从数组的第一个元素开始遍历，target - nums[i] 的值不能与 num[i] 相同

因此需要两个循环遍历


for(let i = 0; i < nums.length; i++){
   	for(let j = i + 1; j < nums.length; j++){
		//...
   }
}

然后判断 target - nums[i] 是否就是 nums[j], 若相同则返回

if(target - nums[i] == nums[j]){
	return [i,j]
}