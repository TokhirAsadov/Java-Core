# Savollar
```txt
1. Hech qanday sikl ishlatmasdan stringni teskari qiluvchi rekursiv funksiya yozing.
2. Katta-kichik harflarni va bo‘shliqlarni e’tiborsiz qoldirib, string palindrom ekanligini tekshiruvchi rekursiv funksiya yarating.
3. Stringdagi unli harflar sonini hisoblaydigan rekursiv funksiya yozing.
4. Stringdagi bir belgini boshqa belgi bilan almashtiruvchi rekursiv funksiya tuzing.
5. len() yoki sikllardan foydalanmasdan string uzunligini topuvchi rekursiv funksiya yozing.
6. Ikkita string bir-birining anagrammasi ekanligini tekshiruvchi rekursiv funksiya yarating.
7. Berilgan stringning barcha mumkin bo‘lgan pastki qatorlarini generatsiya qiluvchi rekursiv funksiya tuzing.
8. Stringdagi so‘zlar sonini (bo‘shliq bilan ajratilgan) hisoblaydigan rekursiv funksiya yozing.
9. Stringdagi har bir so‘zning birinchi harfini katta qiluvchi rekursiv funksiya tuzing.
10. Stringdagi takrorlanuvchi belgilarni olib tashlaydigan va tartibni saqlovchi rekursiv funksiya yarating.
11. Stringdagi birinchi takrorlanmaydigan belgini topuvchi rekursiv funksiya yozing.
12. Berilgan stringning barcha mumkin bo‘lgan almashtirilmalarni generatsiya qiluvchi rekursiv funksiya tuzing.
13. String faqat raqamlardan iborat ekanligini tekshiruvchi rekursiv funksiya yarating.
14. Stringdagi har bir belgi chastotasini hisoblaydigan rekursiv funksiya yozing.
15. Stringni belgilarga bo‘lib, ro‘yxat sifatida qaytaruvchi rekursiv funksiya tuzing.
16. Stringdagi eng uzun palindromik pastki qatorni topuvchi rekursiv funksiya yarating.
17. String to‘g‘ri qavslar ketma-ketligi ekanligini tekshiruvchi rekursiv funksiya yozing (masalan, "((()))").
18. Stringni uning ikkilik ko‘rinishiga aylantiruvchi rekursiv funksiya yarating.
19. Stringdagi barcha bo‘shliqlarni olib tashlaydigan rekursiv funksiya tuzing.
20. Stringda pastki qatorning birinchi paydo bo‘lish indeksini topuvchi rekursiv funksiya yozing.
21. Stringdagi belgilarni barcha mumkin bo‘lgan kombinatsiyalarini generatsiya qiluvchi rekursiv funksiya yarating.
22. Bir string ikkinchi stringning pastki ketma-ketligi ekanligini tekshiruvchi rekursiv funksiya tuzing.
23. Stringdagi katta va kichik harflar sonini hisoblaydigan rekursiv funksiya yozing.
24. Ikkita stringni bir-biriga aralashtiruvchi rekursiv funksiya tuzing (masalan, "abc" va "def" → "adbecf").
25. String takrorlanuvchi pastki qator orqali shakllantirilishi mumkinligini tekshiruvchi rekursiv funksiya yarating.
26. Stringdagi bir pastki qatorni boshqa pastki qator bilan almashtiruvchi rekursiv funksiya yozing.
27. Stringni palindromlarga bo‘lish uchun zarur bo‘lgan minimal kesishlar sonini topuvchi rekursiv funksiya tuzing.
28. Raqamlar qatoridan barcha mumkin bo‘lgan to‘g‘ri IP manzillarni generatsiya qiluvchi rekursiv funksiya yarating.
29. Qavslar bilan kodlangan stringni dekod qiluvchi rekursiv funksiya yarating (masalan, "3[a]2[bc]" → "aaabcbc").
```
---
# Javoblar

## 1. Stringni teskari qilish (reverse)

```java
public static String reverse(String str) {
    if (str.isEmpty()) return "";
    return reverse(str.substring(1)) + str.charAt(0);
}
```

## 2. Palindromni tekshirish (ignoring case and spaces)

```java
public static boolean isPalindrome(String str) {
    str = str.replaceAll("\s+", "").toLowerCase();
    return checkPalindrome(str, 0, str.length() - 1);
}

private static boolean checkPalindrome(String str, int left, int right) {
    if (left >= right) return true;
    return str.charAt(left) == str.charAt(right) && checkPalindrome(str, left + 1, right - 1);
}
```

## 3. Unli harflar soni

```java
public static int countVowels(String str) {
    if (str.isEmpty()) return 0;
    char c = Character.toLowerCase(str.charAt(0));
    int count = "aeiou".indexOf(c) >= 0 ? 1 : 0;
    return count + countVowels(str.substring(1));
}
```

## 4. Belgini boshqa belgi bilan almashtirish

```java
public static String replaceChar(String str, char oldChar, char newChar) {
    if (str.isEmpty()) return "";
    char first = str.charAt(0) == oldChar ? newChar : str.charAt(0);
    return first + replaceChar(str.substring(1), oldChar, newChar);
}
```

## 5. String uzunligini topish (len()siz)

```java
public static int length(String str) {
    if (str.equals("")) return 0;
    return 1 + length(str.substring(1));
}
```

## 6. Anagramma tekshirish

```java
public static boolean isAnagram(String s1, String s2) {
    if (s1.length() != s2.length()) return false;
    if (s1.isEmpty()) return true;
    char c = s1.charAt(0);
    int index = s2.indexOf(c);
    if (index == -1) return false;
    return isAnagram(s1.substring(1), s2.substring(0, index) + s2.substring(index + 1));
}
```

## 7. Barcha pastki qatorlarni generatsiya qilish

```java
public static void generateSubstrings(String str, int start, String curr) {
    if (start == str.length()) {
        if (!curr.isEmpty()) System.out.println(curr);
        return;
    }
    generateSubstrings(str, start + 1, curr + str.charAt(start));
    generateSubstrings(str, start + 1, curr);
}
```

## 8. So‘zlar sonini hisoblash

```java
public static int countWords(String str) {
    str = str.trim();
    if (str.isEmpty()) return 0;
    int space = str.indexOf(' ');
    if (space == -1) return 1;
    return 1 + countWords(str.substring(space + 1));
}
```

## 9. Har bir so‘zning birinchi harfini katta qilish

```java
public static String capitalizeWords(String str) {
    if (str.isEmpty()) return "";
    int space = str.indexOf(' ');
    if (space == -1) return Character.toUpperCase(str.charAt(0)) + str.substring(1);
    String word = str.substring(0, space);
    return Character.toUpperCase(word.charAt(0)) + word.substring(1) + " " + capitalizeWords(str.substring(space + 1));
}
```

## 10. Takrorlanuvchi belgilarni olib tashlash (tartib saqlanadi)

```java
public static String removeDuplicates(String str) {
    return removeDuplicatesHelper(str, "", "");
}

private static String removeDuplicatesHelper(String str, String seen, String result) {
    if (str.isEmpty()) return result;
    char c = str.charAt(0);
    if (seen.indexOf(c) == -1) {
        return removeDuplicatesHelper(str.substring(1), seen + c, result + c);
    }
    return removeDuplicatesHelper(str.substring(1), seen, result);
}
```

## 11. Birinchi takrorlanmaydigan belgi

```java
public static char firstUnique(String str) {
    return firstUniqueHelper(str, 0);
}

private static char firstUniqueHelper(String str, int index) {
    if (index >= str.length()) return 0;
    char c = str.charAt(index);
    if (str.indexOf(c) == str.lastIndexOf(c)) return c;
    return firstUniqueHelper(str, index + 1);
}
```

## 12. Permutatsiyalarni generatsiya qilish

```java
public static void permute(String str, String prefix) {
    if (str.isEmpty()) {
        System.out.println(prefix);
        return;
    }
    for (int i = 0; i < str.length(); i++) {
        permute(str.substring(0, i) + str.substring(i + 1), prefix + str.charAt(i));
    }
}
```

## 13. Faqat raqamlardan iboratligini tekshirish

```java
public static boolean isNumeric(String str) {
    if (str.isEmpty()) return true;
    if (!Character.isDigit(str.charAt(0))) return false;
    return isNumeric(str.substring(1));
}
```

## 14. Belgilar chastotasi

```java
public static void charFrequency(String str, int index, int[] freq) {
    if (index == str.length()) return;
    freq[str.charAt(index)]++;
    charFrequency(str, index + 1, freq);
}
```

## 15. Stringni belgilarga ajratish (ro'yxat)

```java
public static List<Character> toCharList(String str) {
    List<Character> list = new ArrayList<>();
    return toCharListHelper(str, 0, list);
}

private static List<Character> toCharListHelper(String str, int index, List<Character> list) {
    if (index == str.length()) return list;
    list.add(str.charAt(index));
    return toCharListHelper(str, index + 1, list);
}
```

## 16. Eng uzun palindromik substring

```java
public static String longestPalindrome(String s) {
    if (s == null || s.length() < 1) return "";
    return longestPalindromeHelper(s, 0, s.length() - 1);
}

private static String longestPalindromeHelper(String s, int start, int end) {
    if (start > end) return "";
    if (isPalindrome(s.substring(start, end + 1))) return s.substring(start, end + 1);
    String left = longestPalindromeHelper(s, start + 1, end);
    String right = longestPalindromeHelper(s, start, end - 1);
    return left.length() > right.length() ? left : right;
}
```

## 17. To‘g‘ri qavslar ketma-ketligi

```java
public static boolean isValidParentheses(String str, int index, int balance) {
    if (balance < 0) return false;
    if (index == str.length()) return balance == 0;
    char c = str.charAt(index);
    if (c == '(') balance++;
    else if (c == ')') balance--;
    return isValidParentheses(str, index + 1, balance);
}
```

## 18. Stringni ikkilik ko‘rinishga aylantirish

```java
public static String toBinary(int n) {
    if (n == 0) return "0";
    if (n == 1) return "1";
    return toBinary(n / 2) + (n % 2);
}
```

## 19. Bo‘shliqlarni olib tashlash

```java
public static String removeSpaces(String str) {
    if (str.isEmpty()) return "";
    char c = str.charAt(0);
    if (c == ' ') return removeSpaces(str.substring(1));
    return c + removeSpaces(str.substring(1));
}
```

## 20. Substring birinchi indeksini topish

```java
public static int indexOf(String str, String target, int index) {
    if (index + target.length() > str.length()) return -1;
    if (str.substring(index, index + target.length()).equals(target)) return index;
    return indexOf(str, target, index + 1);
}
```

## 21. Barcha belgilar kombinatsiyasi

```java
public static void combinations(String str, String prefix) {
    System.out.println(prefix);
    for (int i = 0; i < str.length(); i++) {
        combinations(str.substring(i + 1), prefix + str.charAt(i));
    }
}
```

## 22. Subsequence tekshirish

```java
public static boolean isSubsequence(String s, String t) {
    if (s.isEmpty()) return true;
    if (t.isEmpty()) return false;
    if (s.charAt(0) == t.charAt(0)) return isSubsequence(s.substring(1), t.substring(1));
    return isSubsequence(s, t.substring(1));
}
```

## 23. Katta va kichik harflar soni

```java
public static int[] countCase(String str, int index, int[] counts) {
    if (index == str.length()) return counts;
    char c = str.charAt(index);
    if (Character.isUpperCase(c)) counts[0]++;
    if (Character.isLowerCase(c)) counts[1]++;
    return countCase(str, index + 1, counts);
}
```

## 24. Ikkita stringni aralashtirish

```java
public static String mergeAlternately(String a, String b) {
    return mergeHelper(a, b, 0, 0);
}

private static String mergeHelper(String a, String b, int i, int j) {
    if (i >= a.length() && j >= b.length()) return "";
    String result = "";
    if (i < a.length()) result += a.charAt(i);
    if (j < b.length()) result += b.charAt(j);
    return result + mergeHelper(a, b, i + 1, j + 1);
}
```

## 25. Takrorlanuvchi substring orqali tuzilganmi

```java
public static boolean repeatedSubstring(String s) {
    int len = s.length();
    for (int i = 1; i <= len / 2; i++) {
        String sub = s.substring(0, i);
        if (len % i == 0 && s.equals(sub.repeat(len / i))) return true;
    }
    return false;
}
```

## 26. Pastki qatorni boshqa bilan almashtirish

```java
public static String replaceSubstring(String str, String target, String replacement) {
    if (!str.contains(target)) return str;
    int idx = str.indexOf(target);
    return str.substring(0, idx) + replacement + replaceSubstring(str.substring(idx + target.length()), target, replacement);
}
```

## 27. Minimal palindrom kesishlar

```java
public static int minCut(String s) {
    if (s.length() <= 1 || isPalindrome(s)) return 0;
    int min = Integer.MAX_VALUE;
    for (int i = 1; i < s.length(); i++) {
        String left = s.substring(0, i);
        String right = s.substring(i);
        if (isPalindrome(left)) {
            min = Math.min(min, 1 + minCut(right));
        }
    }
    return min;
}
```

## 28. IP manzillarni generatsiya qilish

```java
public static void restoreIp(String s, String path, int k) {
    if (k == 0 && s.isEmpty()) {
        System.out.println(path.substring(1));
        return;
    }
    for (int i = 1; i <= 3 && i <= s.length(); i++) {
        String part = s.substring(0, i);
        if ((part.startsWith("0") && part.length() > 1) || Integer.parseInt(part) > 255) continue;
        restoreIp(s.substring(i), path + "." + part, k - 1);
    }
}
```

## 29. Qavsli kodni dekod qilish

```java
public static String decodeString(String s) {
    return decodeHelper(s, new int[]{0});
}

private static String decodeHelper(String s, int[] index) {
    StringBuilder result = new StringBuilder();
    while (index[0] < s.length() && s.charAt(index[0]) != ']') {
        if (Character.isDigit(s.charAt(index[0]))) {
            int k = 0;
            while (Character.isDigit(s.charAt(index[0]))) {
                k = k * 10 + (s.charAt(index[0]++) - '0');
            }
            index[0]++; // skip '['
            String decoded = decodeHelper(s, index);
            index[0]++; // skip ']'
            result.append(decoded.repeat(k));
        } else {
            result.append(s.charAt(index[0]++));
        }
    }
    return result.toString();
}
```


