/*
 * Copyright (c) 2020. Yuanchen
 */

package company.amazon;

/**
 * @author shiyuanchen
 * @project LeetCode
 * @since 2020/09/22
 */
public class Q35NumberOfIslands {

  public static int numIslands(char[][] grid) {
    int res = 0;
    for (int i = 0; i < grid.length; i++) {
      for (int j = 0; j < grid[0].length; j++) {
        if (grid[i][j] == '1') {
          res++;
          dfs(grid, i, j);
        }
      }
    }
    return res;
  }

  private static void dfs(char[][] grid, int i, int j) {
    int m = grid.length;
    int n = grid[0].length;
    if (i < 0 || i >= m || j < 0 || j >= n || grid[i][j] == '0') {
      return;
    }
    grid[i][j] = '0';

    dfs(grid, i + 1, j);
    dfs(grid, i - 1, j);
    dfs(grid, i, j + 1);
    dfs(grid, i, j - 1);
  }

  public static void main(String[] args) {
    char[][] grid = {{'1', '1', '1', '1', '0'}, {'1', '1', '0', '1', '0'},
      {'1', '1', '0', '0', '0'}, {'0', '0', '0', '0', '0'}};
    System.out.println(numIslands(grid));
  }

}
