/*
 * Copyright (c) 2020. Yuanchen
 */

package company.amazon;

import java.util.HashMap;
import java.util.Map;
import java.util.Map.Entry;

/**
 * @author shiyuanchen
 * @project LeetCode
 * @since 2020/09/20
 */
public class Q19MostCommonWord {

  public static String mostCommonWord(String paragraph, String[] banned) {
    paragraph = paragraph.replaceAll("[^0-9a-zA-Z]", " ").toLowerCase();
    String[] words = paragraph.split("\\s+");
    Map<String, Integer> map = new HashMap<>();
    for (String word : words) {
      map.put(word, map.getOrDefault(word, 0) + 1);
    }
    for (String s : banned) {
      map.remove(s);
    }
    int max = Integer.MIN_VALUE;
    String res = "";
    for (Entry<String, Integer> entry : map.entrySet()) {
      if (entry.getValue() > max) {
        res = entry.getKey();
        max = entry.getValue();
      }
    }
    return res;
  }

  public static void main(String[] args) {
    String[] banned = {"hit", "bob"};
    System.out.println(
      mostCommonWord("Bob. hIt, baLl",
        banned));
  }
}
