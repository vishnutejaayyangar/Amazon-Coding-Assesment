/*
 * Copyright (c) 2020. Yuanchen
 */

package company.amazon;

import java.util.HashMap;
import java.util.Map;

/**
 * @author shiyuanchen
 * @project LeetCode
 * @since 2020/09/20
 */
public class Q16IntegerToEnglishWords {

  public static String numberToWords(int num) {
    Map<Integer, String> map = new HashMap<>();
    map.put(0, "Zero");
    map.put(1, "One");
    map.put(2, "Two");
    map.put(3, "Three");
    map.put(4, "Four");
    map.put(5, "Five");
    map.put(6, "Six");
    map.put(7, "Seven");
    map.put(8, "Eight");
    map.put(9, "Nine");
    map.put(10, "Ten");
    map.put(11, "Eleven");
    map.put(12, "Twelve");
    map.put(13, "Thirteen");
    map.put(14, "Fourteen");
    map.put(15, "Fifteen");
    map.put(16, "Sixteen");
    map.put(17, "Seventeen");
    map.put(18, "Eighteen");
    map.put(19, "Nineteen");
    map.put(20, "Twenty");
    map.put(30, "Thirty");
    map.put(40, "Forty");
    map.put(50, "Fifty");
    map.put(60, "Sixty");
    map.put(70, "Seventy");
    map.put(80, "Eighty");
    map.put(90, "Ninety");

    StringBuilder sb = new StringBuilder();
    if (num == 0) {
      return "Zero";
    }
    int billion = num / 1_000_000_000;
    int million = num % 1_000_000_000 / 1_000_000;
    int thousand = num % 1_000_000 / 1_000;
    int ones = num % 1_000;
    if (billion != 0) {
      sb.append(helper(billion, map));
      sb.append("Billion ");
    }
    if (million != 0) {
      sb.append(helper(million, map));
      sb.append("Million ");
    }
    if (thousand != 0) {
      sb.append(helper(thousand, map));
      sb.append("Thousand ");
    }
    if (ones != 0) {
      sb.append(helper(ones, map));
    }
    return sb.toString().trim();
  }

  private static String helper(int num, Map<Integer, String> map) {
    StringBuilder sb = new StringBuilder();
    int hundred = num / 100;
    int tens = num % 100 / 10;
    int ones = num % 10;
    if (hundred != 0) {
      sb.append(map.get(hundred)).append(" Hundred ");
    }
    if (tens != 0) {
      if (num % 100 <= 20) {
        sb.append(map.get(num % 100)).append(" ");
      } else {
        sb.append(map.get(tens * 10)).append(" ");
        if (ones != 0) {
          sb.append(map.get(ones)).append(" ");
        }
      }
    }
    if (tens == 0 && ones != 0) {
      sb.append(map.get(ones)).append(" ");
    }
    return sb.toString();
  }

  public static void main(String[] args) {
    System.out.println(numberToWords(123));
    System.out.println(numberToWords(12345));
    System.out.println(numberToWords(1234567));
    System.out.println(numberToWords(1234567891));
  }
}
