/*
 * Copyright (c) 2020. Yuanchen
 */

package company.amazon;

import java.util.HashMap;
import java.util.Map;

/**
 * @author shiyuanchen
 * @project LeetCode
 * @since 2020/09/07
 *
 * an data_structures.array of integers nums and an integer target, return indices of the two
 * numbers such that they add up to target.
 *
 * You may assume that each input would have exactly one solution, and you may
 * not use the same element twice.
 *
 * You can return the answer in any order.
 */
public class Q1TwoSum {

  public int[] twoSum(int[] nums, int target) {
    Map<Integer, Integer> map = new HashMap<>(nums.length);
    for (int i = 0; i < nums.length; i++) {
      if (map.containsKey(target - nums[i])) {
        return new int[]{i, map.get(target - nums[i])};
      } else {
        map.put(nums[i], i);
      }
    }
    return null;
  }
}
