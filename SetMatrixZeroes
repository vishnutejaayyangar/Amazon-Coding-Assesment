/*
 * Copyright (c) 2020. Yuanchen
 */

package company.amazon;

import java.util.Arrays;

/**
 * @author shiyuanchen
 * @project LeetCode
 * @since 2020/09/18
 */
public class Q11SetMatrixZeroes {

  public static void setZeroes(int[][] matrix) {
    if (matrix == null || matrix.length == 0) {
      return;
    }
    int m = matrix.length, n = matrix[0].length;
    boolean[][] bm = new boolean[m][n];
    for (int i = 0; i < m; i++) {
      for (int j = 0; j < n; j++) {
        if (matrix[i][j] == 0 && !bm[i][j]) {
          helper(matrix, bm, i, j);
        }
      }
    }
  }

  private static void helper(int[][] matrix, boolean[][] bm, int a, int b) {
    for (int i = 0; i < matrix.length; i++) {
      for (int j = 0; j < matrix[0].length; j++) {
        if (i == a || j == b) {
          if (matrix[i][j] != 0) {
            matrix[i][j] = 0;
            bm[i][j] = true;
          }
        }
      }
    }
  }

  public static void main(String[] args) {
    int[][] matrix = {{1, 1, 1}, {1, 0, 1}, {1, 1, 1}};
    int[][] matrix1 = {{0, 1, 2, 0}, {3, 4, 5, 2}, {1, 3, 1, 5}};
    setZeroes(matrix);
    setZeroes(matrix1);
    for (int i = 0; i < matrix.length; i++) {
      System.out.println(Arrays.toString(matrix[i]));
    }
    for (int i = 0; i < matrix1.length; i++) {
      System.out.println(Arrays.toString(matrix1[i]));
    }
  }
}
