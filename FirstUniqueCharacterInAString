/*
 * Copyright (c) 2020. Yuanchen
 */

package company.amazon;

/**
 * @author shiyuanchen
 * @project LeetCode
 * @since 2020/09/20
 */
public class Q17FirstUniqueCharacterInAString {

  public static int firstUniqChar(String s) {
    int[] array = new int[256];
    char[] charArray = s.toCharArray();
    for (Character c : charArray) {
      array[c]++;
    }
    for (int i = 0; i < charArray.length; i++) {
      if (array[charArray[i]] == 1) {
        return i;
      }
    }
    return -1;
  }

  public static void main(String[] args) {
    System.out.println(firstUniqChar("leetcode"));
    System.out.println(firstUniqChar("loveleetcode"));
  }
}
