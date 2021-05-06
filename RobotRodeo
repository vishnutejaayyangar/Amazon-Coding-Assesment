package company.amazon.amazon_oa.albert;

import java.util.ArrayList;
import java.util.List;

public class RobotRodeo {
    public static void main(String[] args) {
        List<String> input = new ArrayList<>();
        input.add("2");
        input.add("G");
        input.add("L");

        System.out.println(doesCircleExist(input));
//        List<String> input1 = new ArrayList<>();
//        input1.add("1");
//        input1.add("GRGL");

//        System.out.println(doesCircleExist(input1));

    }

    public static List<String> doesCircleExist(List<String> commands) {
        List<String> ans = new ArrayList<>();
        for (int k = 1; k < commands.size(); k++) {
            int x = 0, y = 0, i = 0, d[][] = {{0, 1}, {1, 0}, {0, -1}, {-1, 0}};
            for (int j = 0; j < commands.get(k).length(); ++j)
                if (commands.get(k).charAt(j) == 'R')
                    i = (i + 1) % 4;
                else if (commands.get(k).charAt(j) == 'L')
                    i = (i + 3) % 4;
                else {
                    x += d[i][0];
                    y += d[i][1];
                }
            if (x == 0 && y == 0 || i > 0) {
                ans.add("YES");
            } else {
                ans.add("NO");
            }

        }

        return ans;
    }


}
