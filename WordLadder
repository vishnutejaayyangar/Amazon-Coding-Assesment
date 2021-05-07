/*
 * Copyright (c) 2020. Yuanchen
 */

package company.amazon;

import java.util.HashSet;
import java.util.List;
import java.util.Set;

/**
 * @author shiyuanchen
 * @project LeetCode
 * @since 2020/09/22
 */
public class Q34WordLadder {

  public int ladderLength(String beginWord, String endWord,
    List<String> wordList) {
    Set<String> begin = new HashSet<>();
    Set<String> end = new HashSet<>();
    Set<String> dict = new HashSet<>(wordList);

    if (!dict.contains(endWord)) {
      return 0;
    }
    begin.add(beginWord);
    end.add(endWord);

    return helper(begin, end, dict, 1);
  }

  private int helper(Set<String> begin, Set<String> end, Set<String> dict,
    int level) {
    if (begin.isEmpty() || end.isEmpty()) {
      return 0;
    }
    dict.removeAll(begin);
    Set<String> next = new HashSet<>();
    for (String word : begin) {
      char[] arr = word.toCharArray();
      for (int j = 0; j < arr.length; j++) {
        char tmp = arr[j];
        for (char ch = 'a'; ch <= 'z'; ch++) {
          arr[j] = ch;
          String oneDistanceWord = new String(arr);
          if (end.contains(oneDistanceWord)) {
            return level + 1;
          }
          if (dict.contains(oneDistanceWord)) {
            next.add(oneDistanceWord);
          }
        }
        arr[j] = tmp;
      }
    }

    if (next.size() > end.size()) {
      return helper(end, next, dict, level + 1);
    } else {
      return helper(next, end, dict, level + 1);
    }
  }
}
