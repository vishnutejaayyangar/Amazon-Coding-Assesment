package company.amazon.amazon_oa.ella;

import java.util.ArrayList;
import java.util.Arrays;
import java.util.Comparator;
import java.util.List;

public class PrimeAirRoute {
    public static List<List<Integer>> primeAirTime(List<List<Integer>> forwardRouteList, List<List<Integer>> returnRouteList, int maxTravelDist) {
        List<List<Integer>> res = new ArrayList<>();
        List<List<Integer>> org_forward = new ArrayList<>(forwardRouteList);
        List<List<Integer>> org_return = new ArrayList<>(returnRouteList);
        forwardRouteList.sort(Comparator.comparingInt(a -> a.get(1)));
        returnRouteList.sort(Comparator.comparingInt(a -> a.get(1)));

        int minDiff = Integer.MAX_VALUE;
        int i = 0, j = returnRouteList.size() - 1;
        while (i < forwardRouteList.size() && j >= 0) {
            if (minDiff >= Math.abs(maxTravelDist - forwardRouteList.get(i).get(1) - returnRouteList.get(j).get(1))) {
                minDiff = Math.abs(maxTravelDist - forwardRouteList.get(i).get(1) - returnRouteList.get(j).get(1));
                List<Integer> tmp = new ArrayList<>();

                tmp.add(forwardRouteList.get(i).get(0));
                tmp.add(returnRouteList.get(j).get(0));
                res.add(tmp);
            }

            if (maxTravelDist >= forwardRouteList.get(i).get(1) + returnRouteList.get(j).get(1))
                i++;
            else
                j--;
        }

        int max = Integer.MIN_VALUE;
        List<List<Integer>> final_res = new ArrayList<>();
        for (List<Integer> cur : res) {
            int curVal = org_forward.get(cur.get(0) - 1).get(1) + org_return.get(cur.get(1) - 1).get(1);
            if (curVal > max && curVal <= maxTravelDist) {
                final_res.clear();
                max = curVal;
                final_res.add(cur);
            } else if (curVal == max) {
                final_res.add(cur);
            }
        }
        return final_res;
    }

    public static void main(String[] args) {
        List<List<Integer>> forward = new ArrayList<>();
        forward.add(Arrays.asList(1, 8));
        forward.add(Arrays.asList(2, 15));
        forward.add(Arrays.asList(3, 9));
        List<List<Integer>> returnList = new ArrayList<>();
        returnList.add(Arrays.asList(1, 8));
        returnList.add(Arrays.asList(2, 11));
        returnList.add(Arrays.asList(3, 12));
        System.out.println(primeAirTime(forward, returnList, 20));
    }
}
