/*
 * Copyright (c) 2020. Yuanchen
 */

package company.amazon;

import java.util.ArrayDeque;
import java.util.Deque;

/**
 * @author shiyuanchen
 * @project LeetCode
 * @since 2020/09/10
 */
public class Q8BasicCalculatorII {

  public static int calculate(String s) {
    if (s == null || s.length() == 0) {
      return 0;
    }
    s = s.replaceAll("\\s+", "");
    char[] array = s.toCharArray();
    StringBuilder buffer = new StringBuilder();
    Deque<Integer> stack = new ArrayDeque<>();
    char sign = '+';
    for (int i = 0; i < array.length; i++) {
      if (Character.isDigit(array[i])) {
        buffer.append(array[i]);
      }
      if (!Character.isDigit(array[i]) || i == array.length - 1) {
        int num = Integer.parseInt(buffer.toString());
        if (sign == '+') {
          stack.offerFirst(num);
        } else if (sign == '-') {
          stack.offerFirst(-num);
        } else if (sign == '*') {
          stack.offerFirst(stack.pollFirst() * num);
        } else if (sign == '/') {
          stack.offerFirst(stack.pollFirst() / num);
        }
        buffer = new StringBuilder();
        sign = array[i];
      }
    }

    int res = 0;
    for (int i : stack) {
      res += i;
    }

    return res;
  }

  public static void main(String[] args) {
    System.out.println(calculate("3+ 5 /2"));
  }
}
