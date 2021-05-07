/*
 * Copyright (c) 2020. Yuanchen
 */

package company.amazon;

/**
 * @author shiyuanchen
 * @project LeetCode
 * @since 2020/09/07
 *
 * Given an integer data_structures.array nums, find the contiguous subarray (containing at
 * least one number) which has the largest sum and return its sum.
 *
 * Follow up: If you have figured out the O(n) solution, try coding another
 * solution using the divide and conquer approach, which is more subtle.
 */
public class Q6MaximumSubarray {

  public int maxSubArray(int[] nums) {
    if (nums == null || nums.length == 0) {
      return 0;
    }

    int[] dp = new int[nums.length];
    dp[0] = nums[0];
    int globalMax = nums[0];
    for (int i = 1; i < nums.length; i++) {
      if (dp[i - 1] < 0) {
        dp[i] = nums[i];
      } else {
        dp[i] = nums[i] + dp[i - 1];
      }
      globalMax = Math.max(globalMax, dp[i]);
    }
    return globalMax;
  }

}
