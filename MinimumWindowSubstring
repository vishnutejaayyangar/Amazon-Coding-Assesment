/*
 * Copyright (c) 2020. Yuanchen
 */

package company.amazon;

/**
 * @author shiyuanchen
 * @project LeetCode
 * @since 2020/09/19
 */
public class Q12MinimumWindowSubstring {

  public static String minWindow(String s, String t) {
    if (s == null || t == null) {
      return "";
    }
    int[] required = new int[256];
    int start = 0, len = Integer.MAX_VALUE, requiredCnt = t.length();
    int left = 0, right = 0;
    for (int i = 0; i < t.length(); ++i) {
      ++required[t.charAt(i)];
    }

    for (; right < s.length(); ++right) {
      char r = s.charAt(right);
      if (required[r] > 0) {
        --requiredCnt;
      }
      --required[r];

      while (requiredCnt == 0) {
        if (right - left + 1 < len) {
          start = left;
          len = right - left + 1;
        }
        char l = s.charAt(left);
        ++required[l];
        if (required[l] > 0) {
          ++requiredCnt;
        }
        ++left;
      }
    }
    return len == Integer.MAX_VALUE ? "" : s.substring(start, start + len);
  }

  public static void main(String[] args) {
    System.out.println(minWindow("ADOBECODEBANC", "ABC"));
  }
}
