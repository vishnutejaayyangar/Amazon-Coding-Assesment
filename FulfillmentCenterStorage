/*
 * Copyright (c) 2020. Yuanchen
 */

package company.amazon;

import java.util.ArrayList;
import java.util.List;

/**
 * @author shiyuanchen
 * @project LeetCode
 * @since 2020/09/20
 */
public class Q21FulfillmentCenterStorage {


  public static void incrStack(List<String> operations) {
    int n = Integer.parseInt(operations.get(0));
    List<Integer> stack = new ArrayList<>();
    for (int i = 1; i <= n; i++) {
      String cur = operations.get(i).trim();
      if (cur.equals("pop")) {
        if (stack.size() == 1) {
          System.out.println("EMPTY");
          stack.remove(stack.size() - 1);
        } else {
          stack.remove(stack.size() - 1);
          System.out.println(stack.get(stack.size() - 1));
        }
      } else if (cur.indexOf("push") != -1) {
        int num = Integer.parseInt(cur.split("\\s+")[1]);
        stack.add(num);
        System.out.println(stack.get(stack.size() - 1));
      } else if (cur.indexOf("inc") != -1) {
        int index = 0;
        List<Integer> tmpStack = new ArrayList<>();
        int k = Integer.parseInt(cur.split("\\s+")[1]);
        int val = Integer.parseInt(cur.split("\\s+")[2]);
        for (int x : stack) {
          if (index >= k) {
            tmpStack.add(x);
          } else {
            tmpStack.add(x + val);
          }
          index++;
        }
        stack = tmpStack;
        System.out.println(stack.get(stack.size() - 1));
      }
    }
  }

  public static void main(String[] args) {
    List<String> operations = new ArrayList<>();
    operations.add("12");
    operations.add("push 4");
    operations.add("pop");
    operations.add("push 3");
    operations.add("push 5");
    operations.add("push 2");
    operations.add("inc 3 1");
    operations.add("pop");
    operations.add("push 1");
    operations.add("inc 2 2");
    operations.add("push 4");
    operations.add("pop");
    operations.add("pop");
    incrStack(operations);
  }
}
