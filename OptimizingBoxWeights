package company.amazon.amazon_oa.albert;

import java.util.*;

public class OptimizingBoxWeights {
    public List<Integer> minimalHeaviestSetA(List<Integer> arr) {
        Map<Integer, Integer> map = new HashMap<>();
        int totalSum = 0;
        for (int i : arr) {
            totalSum += i;
            map.put(i, map.getOrDefault(i, 0) + 1);
        }
        List<Map.Entry<Integer, Integer>> list = new ArrayList<>();
        for (Map.Entry<Integer, Integer> entry : map.entrySet()) {
            list.add(entry);
        }
        helper(list, 0, 0, totalSum, new ArrayList<>());
        return res;
    }
    int minElements = Integer.MAX_VALUE;
    int maxSum = 0;
    List<Integer> res = null;
    private void helper(List<Map.Entry<Integer, Integer>> list, int index, int currSum, int totalSum, List<Integer> curr) {
        if (currSum > totalSum - currSum) {
            if (minElements > curr.size()) {
                minElements = curr.size();
                res = new ArrayList<>(curr);
                maxSum = currSum;
            } else if (minElements == curr.size()) {
                if (currSum > maxSum) {
                    minElements = curr.size();
                    res = new ArrayList<>(curr);
                    maxSum = currSum;
                }
            }
            return;
        }
        if (index > list.size() - 1)
            return;
        Map.Entry<Integer, Integer> entry = list.get(index);
        List<Integer> temp = new ArrayList<>(curr);
        for (int i = 0; i < entry.getValue(); i++) {
            temp.add(entry.getKey());
        }
        helper(list, index + 1, currSum + (entry.getValue() * entry.getKey()), totalSum, temp);
        helper(list, index + 1, currSum, totalSum, curr);
    }


    public static void main(String[] args) {
        //int[] arr = {15, 20, 20, 20, 50};
        //int[] arr = {6, 6, 6, 7};
        //int[] arr = {3, 4,7, 5, 6, 2};
        List<Integer> arr = Arrays.asList(5, 3, 2, 4, 1, 2);
        OptimizingBoxWeights o = new OptimizingBoxWeights();
        List<Integer> res = o.minimalHeaviestSetA(arr);
        System.out.println(res);
    }
}
