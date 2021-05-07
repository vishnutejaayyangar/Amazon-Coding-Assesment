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
public class Q23MergeTwoSortedLists {

  public static ListNode mergeTwoLists(ListNode l1, ListNode l2) {
    ListNode dummy = new ListNode(0);
    ListNode cur = dummy;
    while (l1 != null && l2 != null) {
      if (l1.val < l2.val) {
        cur.next = l1;
        l1 = l1.next;
      } else {
        cur.next = l2;
        l2 = l2.next;
      }
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
    ListNode l1 = new ListNode(1);
    ListNode l2 = new ListNode(2);
    ListNode l3 = new ListNode(4);
    l1.next = l2;
    l2.next = l3;
    ListNode l4 = new ListNode(1);
    ListNode l5 = new ListNode(3);
    ListNode l6 = new ListNode(4);
    l4.next = l5;
    l5.next = l6;
    ListNode res = mergeTwoLists(l1, l4);
    while (res != null) {
      System.out.println(res.val);
      res = res.next;
    }
  }
}
