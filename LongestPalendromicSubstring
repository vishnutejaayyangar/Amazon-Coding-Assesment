/*
 * Copyright (c) 2020. Yuanchen
 */

package company.amazon;

/**
 * @author shiyuanchen
 * @project LeetCode
 * @since 2020/09/07
 *
 * Given a string s, find the longest palindromic substring in s. You may assume
 * that the maximum length of s is 1000.
 */
public class Q7LongestPalindromicSubstring {

  public String longestPalindrome(String s) {
    int l = 0, start = 0;
    for (int i = 0; i < s.length(); i++) {
      int l1 = expand(s, i, i);
      int l2 = expand(s, i, i + 1);
      int cur = Math.max(l1, l2);
      if (cur > l) {
        l = cur;
        start = i - (cur - 1) / 2;
      }
    }
    return s.substring(start, start + l);
  }

  private int expand(String s, int left, int right) {
    while (left >= 0 && right < s.length() && s.charAt(left) == s
      .charAt(right)) {
      left--;
      right++;
    }
    return right - left - 1;
  }
}
