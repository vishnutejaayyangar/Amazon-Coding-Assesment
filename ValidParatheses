/*
 * Copyright (c) 2020. Yuanchen
 */

package company.amazon;

import java.util.ArrayDeque;
import java.util.Deque;
import java.util.HashMap;
import java.util.Map;

/**
 * @author shiyuanchen
 * @project LeetCode
 * @since 2020/09/20
 */
public class Q18ValidParentheses {

  public static boolean isValid(String s) {
    char[] array = s.toCharArray();
    Map<Character, Character> map = new HashMap<>();
    map.put(')', '(');
    map.put('}', '{');
    map.put(']', '[');
    Deque<Character> stack = new ArrayDeque<>();
    for (char c : array) {
      if (!map.containsKey(c)) {
        stack.offerFirst(c);
      } else if (map.get(c) != stack.peekFirst()) {
        stack.offerFirst(c);
      } else if (map.get(c) == stack.peekFirst()) {
        stack.pollFirst();
      }
    }
    return stack.size() == 0;
  }

  public static void main(String[] args) {
    System.out.println(isValid("()"));
    System.out.println(isValid("()[]{}"));
    System.out.println(isValid("(]"));
    System.out.println(isValid("([)]"));
    System.out.println(isValid("{[]}"));
  }

}
