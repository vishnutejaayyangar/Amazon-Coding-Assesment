/*
 * Copyright (c) 2020. Yuanchen
 */

package company.amazon;

import java.util.Arrays;
import java.util.LinkedList;
import java.util.Queue;

/**
 * @author shiyuanchen
 * @project LeetCode
 * @since 2020/09/18
 */
public class Q10RotateImage {

  public static void rotate(int[][] matrix) {
    int m = matrix.length, n = matrix[0].length;
    int[][] result = new int[m][n];
    Queue<Integer> queue = new LinkedList<>();
    for (int i = 0; i < m; i++) {
      for (int j = 0; j < n; j++) {
        queue.offer(matrix[i][j]);
      }
    }
    for (int j = n - 1; j >= 0; j--) {
      for (int i = 0; i < m; i++) {
        result[i][j] = queue.poll();
      }
    }
    for (int i = 0; i < m; i++) {
      for (int j = 0; j < n; j++) {
        matrix[i][j] = result[i][j];
      }
    }
  }

  public static void main(String[] args) {
    int[][] matrix = {{1, 2, 3}, {4, 5, 6}, {7, 8, 9}};
    rotate(matrix);
    for (int i = 0; i < matrix.length; i++) {
      System.out.println(Arrays.toString(matrix[i]));
    }
  }
}
