/*
 * Copyright (c) 2020. Yuanchen
 */

package company.amazon;

import java.util.Arrays;

/**
 * @author shiyuanchen
 * @project LeetCode
 * @since 2020/09/20
 */
public class Q14ProductOfArrayExceptSelf {

    public static int[] productExceptSelf(int[] nums) {
        int n = nums.length;
        int[] res = new int[n];
        int[] left = new int[n];
        left[0] = 1;
        int[] right = new int[n];
        right[n - 1] = 1;
        for (int i = 1; i <= n - 1; i++) {
            left[i] = left[i - 1] * nums[i - 1];
        }
        for (int i = n - 2; i >= 0; i--) {
            right[i] = right[i + 1] * nums[i + 1];
        }
        for (int i = 0; i < n; i++) {
            res[i] = left[i] * right[i];
        }
        return res;
    }

    public static void main(String[] args) {
        int[] arr = {1, 2, 3, 4};
        int[] arr1 = {0, 0};
        System.out.println(Arrays.toString(productExceptSelf(arr)));
        System.out.println(Arrays.toString(productExceptSelf(arr1)));
    }
}
