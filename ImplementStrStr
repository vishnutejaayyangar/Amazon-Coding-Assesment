/*
 * Copyright (c) 2020. Yuanchen
 */

package company.amazon;

/**
 * @author shiyuanchen
 * @project LeetCode
 * @since 2020/09/18
 */
public class Q9ImplementStrStr {

  public static int strStr(String haystack, String needle) {
    if (haystack == null) {
      return -1;
    }
    if (haystack.length() == 0 && needle.length() == 0) {
      return 0;
    }
    if (needle.length() == 0) {
      return 0;
    }
    int i = 0, j = 0;
    char[] arr1 = haystack.toCharArray();
    char[] arr2 = needle.toCharArray();
    while (i <= arr1.length - arr2.length) {
      if (arr1[i] == arr2[j]) {
        int tmp = i;
        while (j < arr2.length) {
          if (arr1[tmp] != arr2[j]) {
            j = 0;
            break;
          }
          j++;
          tmp++;
        }
        if (j == arr2.length) {
          return i;
        }
      }
      i++;
    }
    return -1;
  }

  public static void main(String[] args) {
    System.out.println(strStr("mississippi", "issip"));
    System.out.println(strStr("mississippi", "mississippi"));
    System.out.println(strStr("aaaaa", "bba"));
    System.out.println(strStr("a", "a"));
  }
}
