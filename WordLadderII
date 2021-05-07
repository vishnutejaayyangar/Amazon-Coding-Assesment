/*
 * Copyright (c) 2020. Yuanchen
 */

package company.amazon;

import java.util.*;

/**
 * @author shiyuanchen
 * @project LeetCode
 * @since 2020/09/22
 */
public class Q33WordLadderII {

  Map<String, Set<String>> graph;
  Map<String, Integer> levels;

  private boolean isEdge(String a, String b) {
    int count = 0;
    for (int i = 0; i < a.length(); i++) {
      if (a.charAt(i) != b.charAt(i)) {
        ++count;
      }
    }
    return count == 1;
  }

  private void createGraph(List<String> wordList) {
    graph = new HashMap<>();

    for (String w : wordList) {
      graph.put(w, new HashSet<String>());
    }

    for (int i = 0; i < wordList.size(); i++) {
      for (int j = i + 1; j < wordList.size(); j++) {
        if (isEdge(wordList.get(i), wordList.get(j))) {
          graph.get(wordList.get(i)).add(wordList.get(j));
          graph.get(wordList.get(j)).add(wordList.get(i));
        }
      }
    }
  }

  void dfs(String word, String endWord, List<String> cur,
    List<List<String>> res, Set<String> seen) {
    cur.add(word);
    seen.add(word);
    if (word.equals(endWord)) {
      res.add(new ArrayList<>(cur));
    } else {
      for (String s : graph.get(word)) {
        if (!seen.contains(s) && levels.get(s) > levels.get(word)) {
          dfs(s, endWord, cur, res, seen);
        }
      }
    }
    cur.remove(cur.size() - 1);
    seen.remove(word);
  }

  public List<List<String>> findLadders(String beginWord, String endWord,
    List<String> wordList) {
    wordList.add(0, beginWord);
    createGraph(wordList);

    levels = new HashMap<>();
    Queue<String> q = new LinkedList<>();
    levels.put(beginWord, 0);
    q.add(beginWord);

    while (!q.isEmpty()) {
      int size = q.size();
      for (int i = 0; i < size; i++) {
        String cur = q.poll();
        for (String nei : graph.get(cur)) {
          if (!levels.containsKey(nei)) {
            levels.put(nei, levels.get(cur) + 1);
            q.add(nei);
          }
        }
      }
    }

    List<List<String>> res = new ArrayList<>();
    List<String> cur = new ArrayList<>();
    Set<String> seen = new HashSet<>();
    dfs(beginWord, endWord, cur, res, seen);

    return res;
  }
}
