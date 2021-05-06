package company.amazon.amazon_oa.albert;

import java.util.*;

public class CloudFront {
    private static Map<Integer, List<Integer>> g;
    private static boolean[] visited;

    public static int connectedSum(int n, List<String> edges) {
        return helper(n, transform(edges));
    }

    private static int[][] transform(List<String> edges) {
        int m = edges.size();
        int[][] arr = new int[m][2];

        for (int i = 0; i < edges.size(); i++) {
            String[] tmpArray = edges.get(i).split(" ");
            arr[i][0] = Integer.parseInt(tmpArray[0]);
            arr[i][1] = Integer.parseInt(tmpArray[1]);
        }
        return arr;
    }

    private static int helper(int n, int[][] edges) {
        g = new HashMap<>();
        visited = new boolean[n];
        for (int i = 0; i < edges.length; ++i) {
            int src = edges[i][0] - 1, dest = edges[i][1] - 1;
            if (!g.containsKey(src)) g.put(src, new ArrayList<>());
            if (!g.containsKey(dest)) g.put(dest, new ArrayList<>());
            g.get(src).add(dest);
            g.get(dest).add(src);
        }

        int res = 0;
        for (int i = 0; i < n; ++i) {
            if (!visited[i]) res += doBFS(i);
        }
        return res;
    }

    private static int doBFS(int start) {
        Queue<Integer> q = new LinkedList<>();
        q.offer(start);
        visited[start] = true;
        int cnt = 0;
        while (!q.isEmpty()) {
            int cur = q.poll();
            cnt++;
            if (!g.containsKey(cur)) continue;
            for (int next : g.get(cur)) {
                if (!visited[next]) {
                    q.offer(next);
                    visited[next] = true;
                }
            }
        }
        return (int) (Math.ceil(Math.sqrt(cnt)));
    }


    public static void main(String[] args) {
        CloudFront sol = new CloudFront();

        List<String> edges1 = Arrays.asList("1 2", "1 4");
        System.out.println(sol.connectedSum(4, edges1));
    }
}
