package company.amazon.amazon_oa.ella;

import java.util.Arrays;

public class SearchChallenge {
    final static int MAX_CHARS = 26;

    public static boolean isValid(int[] count, int k) {
        int val = 0;
        for (int i = 0; i < MAX_CHARS; i++) {
            if (count[i] > 0) {
                val++;
            }
        }
        return k >= val;
    }

    public static String SearchingChallenge(String str) {
        int k = str.charAt(0) - '0';
        return helper(str.substring(1), k);
    }

    public static String helper(String s, int k) {
        int n = s.length();
        int[] count = new int[MAX_CHARS];
        Arrays.fill(count, 0);
        for (int i = 0; i < n; i++) {
            count[s.charAt(i) - 'a']++;
        }
        int curr_start = 0;
        int curr_end = 0;
        int max_size = 1;
        int max_start = 0;
        Arrays.fill(count, 0);
        count[s.charAt(0) - 'a']++;
        for (int i = 1; i < n; i++) {
            count[s.charAt(i) - 'a']++;
            curr_end++;
            while (!isValid(count, k)) {
                count[s.charAt(curr_start) - 'a']--;
                curr_start++;
            }
            if (curr_end - curr_start + 1 > max_size) {
                max_size = curr_end - curr_start + 1;
                max_start = curr_start;
            }
        }
        return s.substring(max_start, max_start + max_size);
    }

    // Driver Code
    static public void main(String[] args) {
        System.out.println(SearchingChallenge("3aabacbebebe"));
        System.out.println(SearchingChallenge("2aabbcbbbadef"));
    }
}
