/*
 * Copyright (c) 2020. Yuanchen
 */

package company.amazon;

import utility.TreeNode;

/**
 * @author shiyuanchen
 * @project LeetCode
 * @since 2020/09/21
 */
public class Q28ValidateBinarySearchTree {

  public static boolean isValidBST(TreeNode root) {
    if (root == null) {
      return true;
    }
    return helper(root, Long.MIN_VALUE, Long.MAX_VALUE);
  }

  private static boolean helper(TreeNode root, long min, long max) {
    if (root == null) {
      return true;
    }
    if (root.val < min || root.val > max) {
      return false;
    }
    return helper(root.left, min, root.val) && helper(root.right, root.val,
      max);
  }

  public static void main(String[] args) {
    TreeNode node1 = new TreeNode(2);
    TreeNode node2 = new TreeNode(1);
    TreeNode node3 = new TreeNode(3);
    node1.left = node2;
    node1.right = node3;
    System.out.println(isValidBST(node1));
  }
}
