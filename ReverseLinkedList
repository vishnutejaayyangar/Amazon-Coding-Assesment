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
public class Q25ReverseLinkedList {

  public static ListNode reverseList(ListNode head) {
    ListNode prev = null;
    while (head != null) {
      ListNode newNode = head.next;
      head.next = prev;
      prev = head;
      head = newNode;
    }
    return prev;
  }

  public static void main(String[] args) {
    ListNode l1 = new ListNode(1);
    ListNode l2 = new ListNode(2);
    ListNode l3 = new ListNode(3);
    ListNode l4 = new ListNode(4);
    ListNode l5 = new ListNode(5);
    l1.next = l2;
    l2.next = l3;
    l3.next = l4;
    l4.next = l5;
    ListNode res = reverseList(l1);
    while (res != null) {
      System.out.println(res.val);
      res = res.next;
    }
  }

}
