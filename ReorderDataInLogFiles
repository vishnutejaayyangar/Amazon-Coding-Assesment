/*
 * Copyright (c) 2020. Yuanchen
 */

package company.amazon;

import java.util.Arrays;
import java.util.Comparator;

/**
 * @author shiyuanchen
 * @project LeetCode
 * @since 2020/09/20
 */
public class Q20ReorderDataInLogFiles {

  public static String[] reorderLogFiles(String[] logs) {
    Comparator<String> myComparator = new Comparator<String>() {
      @Override
      public int compare(String o1, String o2) {
        String[] s1 = o1.split(" ", 2);
        String[] s2 = o2.split(" ", 2);

        boolean isDigit1 = Character.isDigit(s1[1].charAt(0));
        boolean isDigit2 = Character.isDigit(s2[1].charAt(0));

        if (!isDigit1 && !isDigit2) {
          int comp = s1[1].compareTo(s2[1]);
          return comp == 0 ? s1[0].compareTo(s2[0]) : comp;
        } else if (!isDigit1) {
          return -1;
        } else if (!isDigit2) {
          return 1;
        } else {
          return 0;
        }
      }
    };

    Arrays.sort(logs, myComparator);
    return logs;

  }

  public static void main(String[] args) {
    String[] logs = {"dig1 8 1 5 1", "let1 art can", "dig2 3 6",
      "let2 own kit dig", "let3 art zero"};
    System.out.println(Arrays.toString(reorderLogFiles(logs)));

  }
}
