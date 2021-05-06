/*
 * Copyright (c) 2020. Yuanchen
 */

package company.amazon;

/**
 * @author shiyuanchen
 * @project LeetCode
 * @since 2020/09/20
 */
public class Q13CompareVersionNumbers {

  public static int compareVersion(String version1, String version2) {
    String[] array1 = version1.split("\\.");
    String[] array2 = version2.split("\\.");
    for (int i = 0; i < array1.length; i++) {
      array1[i] = removeLeadingZero(array1[i]);
    }
    for (int i = 0; i < array2.length; i++) {
      array2[i] = removeLeadingZero(array2[i]);
    }
    int i = 0;
    while (i < array1.length && i < array2.length) {
      if (Integer.parseInt(array1[i]) < Integer.parseInt(array2[i])) {
        return -1;
      } else if (Integer.parseInt(array1[i]) > Integer.parseInt(array2[i])) {
        return 1;
      }
      i++;
    }
    while (i < array1.length) {
      if (array1[i].equals("0")) {
        i++;
        continue;
      } else {
        return 1;
      }
    }
    while (i < array2.length) {
      if (array2[i].equals("0")) {
        i++;
        continue;
      } else {
        return -1;
      }
    }
    return 0;
  }


  private static String removeLeadingZero(String s) {
    if (s.length() == 1 && s.equals("0")) {
      return s;
    }
    char[] arr = s.toCharArray();
    int i = 0;
    for (; i < arr.length; i++) {
      if (arr[i] == '0') {
        continue;
      } else {
        break;
      }
    }
    if (i == arr.length) {
      s = "0";
      return "0";
    } else {
      return s.substring(i);
    }
  }

  public static void main(String[] args) {
    System.out.println(compareVersion("1.2", "1.10"));
    System.out.println(compareVersion("1.01", "1.001"));
    System.out.println(compareVersion("1.0", "1.0.0"));
    System.out.println(compareVersion("0.1", "1.1"));
    System.out.println(compareVersion("1.0.1", "1"));
    System.out.println(compareVersion("7.5.2.4", "7.5.3"));
  }
}
