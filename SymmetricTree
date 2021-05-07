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
public class Q29SymmetricTree {

  public static boolean isSymmetric(TreeNode root) {
    if (root == null) {
      return true;
    }
    return helper(root.left, root.right);
  }

  private static boolean helper(TreeNode left, TreeNode right) {
    if (left == null && right == null) {
      return true;
    }
    if (left == null || right == null) {
      return false;
    }
    return left.val == right.val && helper(left.left, right.right) && helper(
      left.right, right.left);
  }

  public static void main(String[] args) {
    TreeNode node1 = new TreeNode(1);
    TreeNode node2 = new TreeNode(2);
    TreeNode node3 = new TreeNode(2);
    TreeNode node4 = new TreeNode(3);
    TreeNode node5 = new TreeNode(3);
    TreeNode node6 = new TreeNode(3);
    TreeNode node7 = new TreeNode(3);
    node1.left = node2;
    node1.right = node3;
    node2.left = node4;
    node2.right = node5;
    node3.left = node6;
    node3.right = node7;
    System.out.println(isSymmetric(node1));
  }
}
