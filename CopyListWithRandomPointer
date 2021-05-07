/*
 * Copyright (c) 2020. Yuanchen
 */

package company.amazon;


import utility.RNode;

import java.util.HashMap;
import java.util.Map;

/**
 * @author shiyuanchen
 * @project LeetCode
 * @since 2020/09/21
 */
public class Q24CopyListWithRandomPointer {

  public RNode copyRandomList(RNode head) {
    Map<RNode, RNode> map = new HashMap<>();
    RNode node = head;
    while (node != null) {
      map.put(node, new RNode(node.val));
      node = node.next;
    }
    node = head;
    while (node != null) {
      map.get(node).next = map.get(node.next);
      map.get(node).random = map.get(node.random);
      node = node.next;
    }
    return map.get(head);

  }
}
