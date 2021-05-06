/*
 * Copyright (c) 2020. Yuanchen
 */

package company.amazon;

/**
 * @author shiyuanchen
 * @project LeetCode
 * @since 2020/09/20
 */
public class Q15MissingNumber {

  public static int missingNumber(int[] nums) {
    int n = nums.length;
    int sum = (0 + n) * (n + 1) / 2;
    for (int num : nums) {
      sum -= num;
    }
    return sum;
  }

  public static void main(String[] args) {
    int[] input = {3, 0, 1};
    int[] input1 = {9, 6, 4, 2, 3, 5, 7, 0, 1};
    System.out.println(missingNumber(input));
    System.out.println(missingNumber(input1));
  }
}
