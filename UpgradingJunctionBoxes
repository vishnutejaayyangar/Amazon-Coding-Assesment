package company.amazon.amazon_oa.ella;

import java.util.Arrays;
import java.util.Comparator;
import java.util.List;

public class UpgradingJunctionBoxes {
    public static List<String> reorderLogFiles(List<String> boxList) {
        Comparator<String> myComparator = (o1, o2) -> {
            String[] s1 = o1.split(" ", 2);
            String[] s2 = o2.split(" ", 2);

            boolean isNewVersion1 = Character.isDigit(s1[1].charAt(0));
            boolean isNewVersion2 = Character.isDigit(s2[1].charAt(0));

            if (!isNewVersion1 && !isNewVersion2) {
                int comp = s1[1].compareTo(s2[1]);
                return comp == 0 ? s1[0].compareTo(s2[0]) : comp;
            } else if (!isNewVersion1) {
                return -1;
            } else if (!isNewVersion2) {
                return 1;
            } else {
                return 0;
            }
        };
        boxList.sort(myComparator);
        return boxList;
    }

    public static void main(String[] args) {
        List<String> boxList = Arrays.asList("ykc 82 01", "eo first qpx", "09z cat hamster", "06f 12 25 6",
                "ax0 first qpx", "236 cat dog rabbit snake");
        System.out.println(reorderLogFiles(boxList));
    }
}
