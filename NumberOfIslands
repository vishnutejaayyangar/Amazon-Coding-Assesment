/*
 * Copyright (c) 2020. Yuanchen
 */

package company.amazon;

/**
 * @author shiyuanchen
 * @project LeetCode
 * @since 2020/09/07
 *
 * Given a 2d grid map of '1's (land) and '0's (water), count the number of
 * islands. An island is surrounded by water and is formed by connecting
 * adjacent lands horizontally or vertically. You may assume all four edges of
 * the grid are all surrounded by water.
 */
public class Q2NumberOfIslands {

  public int numIsLands(char[][] grid) {
    if (grid == null || grid[0].length == 0) {
      return 0;
    }
    int res = 0;
    int m = grid.length;
    int n = grid[0].length;
    for (int i = 0; i < m; i++) {
      for (int j = 0; j < n; j++) {
        if (grid[i][j] == '1') {
          res++;
          dfs(grid, i, j, m, n, res);
        }
      }
    }
    return res;
  }

  private void dfs(char[][] grid, int i, int j, int m, int n, int res) {
    if (i < 0 || j < 0 || i >= m || j >= n || grid[i][j] == '0') {
      return;
    }
    grid[i][j] = '0';
    dfs(grid, i + 1, j, m, n, res);
    dfs(grid, i - 1, j, m, n, res);
    dfs(grid, i, j + 1, m, n, res);
    dfs(grid, i, j - 1, m, n, res);
  }

}
