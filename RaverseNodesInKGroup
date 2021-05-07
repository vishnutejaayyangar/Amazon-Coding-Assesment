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
public class Q27ReverseNodesInKGroup {

  public ListNode reverseLinkedList(ListNode head, int k) {
    ListNode dummy = null;
    ListNode cur = head;

    while (k > 0) {

      // Keep track of the next node to process in the
      // original list
      ListNode next_node = cur.next;

      // Insert the node pointed to by "ptr"
      // at the beginning of the reversed list
      cur.next = dummy;
      dummy = cur;

      // Move on to the next node
      cur = next_node;

      // Decrement the count of nodes to be reversed by 1
      k--;
    }

    // Return the head of the reversed list
    return dummy;

  }

  public ListNode reverseKGroup(ListNode head, int k) {

    int count = 0;
    ListNode ptr = head;

    // First, see if there are atleast k nodes
    // left in the linked list.
    while (count < k && ptr != null) {
      ptr = ptr.next;
      count++;
    }

    // If we have k nodes, then we reverse them
    if (count == k) {

      // Reverse the first k nodes of the list and
      // get the reversed list's head.
      ListNode reversedHead = this.reverseLinkedList(head, k);

      // Now recurse on the remaining linked list. Since
      // our recursion returns the head of the overall processed
      // list, we use that and the "original" head of the "k" nodes
      // to re-wire the connections.
      head.next = this.reverseKGroup(ptr, k);
      return reversedHead;
    }

    return head;
  }
}
