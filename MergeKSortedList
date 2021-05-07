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
public class Q26MergeKSortedLists {

  public ListNode mergeKLists(ListNode[] lists) {
    if (lists == null || lists.length == 0) {
      return null;
    }
    ListNode dummy = new ListNode(0);
    ListNode cur = lists[0];
    dummy.next = cur;
    int i = 1;
    while (i < lists.length) {
      dummy.next = mergeTwo(cur, lists[i]);
      cur = dummy.next;
      i++;
    }
    return dummy.next;
  }

  private ListNode mergeTwo(ListNode one, ListNode two) {
    ListNode dummy = new ListNode(0);
    ListNode cur = dummy;
    while (one != null && two != null) {
      if (one.val < two.val) {
        cur.next = one;
        one = one.next;
      } else {
        cur.next = two;
        two = two.next;
      }
      cur = cur.next;
    }
    if (one == null) {
      cur.next = two;
    }
    if (two == null) {
      cur.next = one;
    }
    return dummy.next;
  }
}
