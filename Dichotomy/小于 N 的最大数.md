### 题目描述

数组 nums 中给定可以使用的 1 ~ 9 的数，返回由数组 nums 中的元素组成的小于 n 的最大数。元素可以重复使用。

示例 1：nums = {1, 2, 9, 4}，n = 2533，返回 2499。

示例 2：nums = {1, 2, 5, 4}，n = 2543，返回 2542。

示例 3：nums = {1, 2, 5, 4}，n = 2541，返回 2525。

示例 4：nums = {1, 2, 9, 4}，n = 2111，返回 1999。

示例 5：nums = {5, 9}，n = 5555，返回 999。

---

深度搜索优先：时间复杂度 `O n^len(target)`

```go
package main

import (
	"fmt"
)

var res int

func main() {
	nums := []int{2, 4, 6, 8}
	target := 2411
	backtrack(nums, target, 0)
	fmt.Println(res)
}

func backtrack(nums []int, target, sum int) {
	if sum >= target {
		return
	}
	res = max(res, sum)
	for i := range nums {
		backtrack(nums, target, 10*sum+nums[i])
	}
}

func max(i, j int) int {
	if i > j {
		return i
	}
	return j
}

```





贪心 + 二分查找：时间复杂度 `Ologn`

```java
package com.example.demo.test;


// nums = [5, 4, 8, 2], n = 5416,     res = 5288

import java.util.Arrays;


public class Solution {

    public static void main(String[] args) {
        int[] nums = {1,2,5,4};
        int n = 2541;
        Arrays.sort(nums);
        String s = findMin(n, nums[0]);
        StringBuilder sb = new StringBuilder();
        boolean flag = false;
        for(int i = 0; i < s.length(); i++){
            /*
            每位都找小于等于该位最大的数，如果s这个位置的数大于等于nums的最大值，就用最大值，否则去数组找最接近的
            如果当前从数组中找的数字小于s对应这位的数字，此后选择的数字都可以是数组中的最大值
            例如2513和{2,4,6,8}，选到第二位4之后，4比5小，此后就可以都选择8，组成2488
            */
            char c = s.charAt(i);
            if(flag){
                sb.append(nums[nums.length - 1]);
            } else {
                int index = getIndex(nums, i, s);
                sb.append(nums[index]);
                if(nums[index] < c - '0') flag = true;
            }
        }
        System.out.println(sb);
    }

    public static int getIndex(int[] nums, int index, String s){
        int target = s.charAt(index) - '0';
        /*
        此外，选择数字还要受到下一位数字的影响
        假设s为2411，nums为{2,4,6,8}
        第二位数字应该选4，但如果选了4，后面再拼接就一定会大于s了。
         */
        if(index < s.length() - 1){
            int next = s.charAt(index + 1) - '0';
            if(next <= nums[0]){
                target -= 1;
            }
        }
        return dichotomy(nums, target);
    }


    /**
     * 二分查找，查找小于等于target的最大下标。
     * @param nums
     * @param target
     * @return
     */
    public static int dichotomy(int[] nums, int target){
        int left = 0, right = nums.length;
        while(left < right){
            int mid = (left + right) / 2;
            if(nums[mid] <  target){
                left = mid + 1;
            } else if(nums[mid] > target){
                right = mid;
            } else return mid;
        }
        return left - 1;
    }

    /**
     * 判断是否能拼出和 n 长度一样的字符串，通过判断str的第一位与nums[0](minValue)的大小关系，无法判断则迭代判断下一位
     * @param n
     * @param minValue
     * @return
     */
    public static String findMin(int n, int minValue){
        boolean flag = false;
        String numStr = String.valueOf(n);
        for(int i = 0; i < numStr.length(); i++){
            if(minValue < (numStr.charAt(i) - '0')){
                flag = true;
                break;
            }
        }
        int maxValue = flag ? (n - 1) : (int)(Math.pow(10, numStr.length() - 1) - 1);
        return String.valueOf(maxValue);
    }
}

```
