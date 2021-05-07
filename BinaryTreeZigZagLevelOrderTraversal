/*
 * Copyright (c) 2020. Yuanchen
 */

package company.amazon;

import utility.TreeNode;

import java.util.*;

/**
 * @author shiyuanchen
 * @project LeetCode
 * @since 2020/09/22
 */
public class Q31BinaryTreeZigZagLevelOrderTraversal {

  public Q31BinaryTreeZigZagLevelOrderTraversal() {
  }

  public static List<List<Integer>> zigzagLevelOrder(TreeNode root) {
    List<List<Integer>> res = new ArrayList<>();
    if (root == null) {
      return res;
    }
    Queue<TreeNode> queue = new LinkedList<>();
    queue.offer(root);
    boolean goRight = true;
    while (!queue.isEmpty()) {
      List<Integer> curList = new ArrayList<>();
      int size = queue.size();
      for (int i = 0; i < size; i++) {
        TreeNode cur = queue.poll();
        curList.add(cur.val);
        if (cur.left != null) {
          queue.offer(cur.left);
        }
        if (cur.right != null) {
          queue.offer(cur.right);
        }
      }
      if (!goRight) {
        Collections.reverse(curList);
      }
      res.add(curList);
      goRight = !goRight;
    }
    return res;
  }

  public static void main(String[] args) {
    TreeNode t1 = new TreeNode(3);
    TreeNode t2 = new TreeNode(9);
    TreeNode t3 = new TreeNode(20);
    TreeNode t4 = new TreeNode(15);
    TreeNode t5 = new TreeNode(7);
    t1.left = t2;
    t1.right = t3;
    t3.left = t4;
    t3.right = t5;
    System.out.println(zigzagLevelOrder(t1));
  }
}
