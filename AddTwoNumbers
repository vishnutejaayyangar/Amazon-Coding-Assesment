/*
 * Copyright (c) 2020. Yuanchen
 */

package company.amazon;

import utility.ListNode;

/**
 * @author shiyuanchen
 * @project LeetCode
 * @since 2020/09/21
 */
public class Q22AddTwoNumbers {

  public static ListNode addTwoNumbers(ListNode l1, ListNode l2) {
    ListNode dummy = new ListNode(0);
    ListNode cur = dummy;
    int val = 0;
    while (l1 != null || l2 != null || val != 0) {
      if (l1 != null) {
        val += l1.val;
        l1 = l1.next;
      }
      if (l2 != null) {
        val += l2.val;
        l2 = l2.next;
      }
      cur.next = new ListNode(val % 10);
      val /= 10;
      cur = cur.next;
    }
    if (l1 != null) {
      cur.next = l1;
    }
    if (l2 != null) {
      cur.next = l2;
    }
    return dummy.next;
  }

  public static void main(String[] args) {
    ListNode l1 = new ListNode(2);
    ListNode l2 = new ListNode(4);
    ListNode l3 = new ListNode(3);
    l1.next = l2;
    l2.next = l3;
    ListNode l4 = new ListNode(5);
    ListNode l5 = new ListNode(6);
    ListNode l6 = new ListNode(4);
    l4.next = l5;
    l5.next = l6;
    ListNode res = addTwoNumbers(l1, l4);
    while (res != null) {
      System.out.println(res.val);
      res = res.next;
    }
  }
}
