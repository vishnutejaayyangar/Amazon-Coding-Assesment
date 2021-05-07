/*
 * Copyright (c) 2020. Yuanchen
 */

package company.amazon;

import utility.TreeNode;

/**
 * @author shiyuanchen
 * @project LeetCode
 * @since 2020/09/22
 */
public class Q32BinaryTreeMaximumPathSum {

  static int max = Integer.MIN_VALUE;

  public static int maxPathSum(TreeNode root) {
    helper(root);
    return max;
  }

  private static int helper(TreeNode root) {
    if (root == null) {
      return 0;
    }
    int left = Math.max(helper(root.left), 0);
    int right = Math.max(helper(root.right), 0);
    max = Math.max(max, left + right + root.val);
    return Math.max(left, right) + root.val;
  }

  public static void main(String[] args) {

  }
}
