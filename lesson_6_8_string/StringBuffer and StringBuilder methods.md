# StringBuilder va StringBuffer Metodlari va Misollar

Java'da `StringBuilder` va `StringBuffer` sinflari satrlar bilan ishlashda o'zgaruvchan (mutable) va o'suvchan (growable) imkoniyatlarni ta'minlaydi. Quyida ularning asosiy metodlari va har biriga misollar keltirilgan. `StringBuilder` va `StringBuffer`ning metodlari bir xil, lekin `StringBuffer` sinxronlashtirilgan bo'lib, ko'p oqimli (multithreaded) muhitda xavfsizroq, `StringBuilder` esa tezroq ishlaydi.

## 1. `append` Metodlari
Satr yoki boshqa ma'lumot turini ob'ektning oxiriga qo'shadi.

### `append(String str)`, `append(char c)`, `append(int i)`, va boshqalar
- **Tavsif**: Har xil ma'lumot turlarini (satr, belgilar, sonlar va boshqalar) qo'shadi.
- **Misol**:
```java
StringBuilder sb = new StringBuilder("Hello");
sb.append(" World"); // String qo'shish
sb.append('!'); // Belgini qo'shish
sb.append(123); // Sonni qo'shish
System.out.println(sb); // Natija: Hello World!123

StringBuffer sbf = new StringBuffer("Java");
sbf.append(" Programming");
System.out.println(sbf); // Natija: Java Programming
```

## 2. `insert` Metodlari
Belgilangan indeksda satr yoki ma'lumotni kiritadi.

### `insert(int offset, String str)`, `insert(int offset, char c)`, va boshqalar
- **Tavsif**: Belgilangan pozitsiyaga ma'lumot kiritadi.
- **Misol**:
```java
StringBuilder sb = new StringBuilder("HelloWorld");
sb.insert(5, ", "); // 5-indeksdan keyin kiritish
System.out.println(sb); // Natija: Hello, World

StringBuffer sbf = new StringBuffer("Java");
sbf.insert(0, "Learn ");
System.out.println(sbf); // Natija: Learn Java
```

## 3. `delete` va `deleteCharAt`
Satrning ma'lum bir qismini yoki belgilangan indeksdagi belgini o'chiradi.

### `delete(int start, int end)`
- **Tavsif**: `start`dan `end-1`gacha bo'lgan qismni o'chiradi.
- **Misol**:
```java
StringBuilder sb = new StringBuilder("Hello, World");
sb.delete(5, 7); // ", " ni o'chirish
System.out.println(sb); // Natija: HelloWorld

StringBuffer sbf = new StringBuffer("Java Programming");
sbf.delete(4, 12); // " Program" ni o'chirish
System.out.println(sbf); // Natija: Java ming
```

### `deleteCharAt(int index)`
- **Tavsif**: Belgilangan indeksdagi belgini o'chiradi.
- **Misol**:
```java
StringBuilder sb = new StringBuilder("Hello");
sb.deleteCharAt(1); // 'e' ni o'chirish
System.out.println(sb); // Natija: Hllo

StringBuffer sbf = new StringBuffer("Java");
sbf.deleteCharAt(2); // 'v' ni o'chirish
System.out.println(sbf); // Natija: Jaa
```

## 4. `replace`
Satrning ma'lum bir qismini boshqa satr bilan almashtiradi.

### `replace(int start, int end, String str)`
- **Tavsif**: `start`dan `end-1`gacha bo'lgan qismni yangi satr bilan almashtiradi.
- **Misol**:
```java
StringBuilder sb = new StringBuilder("Hello, World");
sb.replace(6, 11, "Java"); // "World" ni "Java" bilan almashtirish
System.out.println(sb); // Natija: Hello, Java

StringBuffer sbf = new StringBuffer("Java Programming");
sbf.replace(5, 16, "Code"); // "Programming" ni "Code" bilan almashtirish
System.out.println(sbf); // Natija: Java Code
```

## 5. `reverse`
Satrni teskari tartibga keltiradi.

### `reverse()`
- **Tavsif**: Satrning belgilar tartibini teskari qiladi.
- **Misol**:
```java
StringBuilder sb = new StringBuilder("Hello");
sb.reverse();
System.out.println(sb); // Natija: olleH

StringBuffer sbf = new StringBuffer("Java");
sbf.reverse();
System.out.println(sbf); // Natija: avaJ
```

## 6. `substring` va `subSequence`
Satrning bir qismini qaytaradi.

### `substring(int start)` va `substring(int start, int end)`
- **Tavsif**: Belgilangan indekslardan satrning qismini qaytaradi (yangi `String` sifatida).
- **Misol**:
```java
StringBuilder sb = new StringBuilder("Hello, World");
String sub = sb.substring(7); // 7-indeksdan oxirigacha
System.out.println(sub); // Natija: World
System.out.println(sb.substring(0, 5)); // Natija: Hello

StringBuffer sbf = new StringBuffer("Java Programming");
System.out.println(sbf.substring(5, 16)); // Natija: Programming
```

### `subSequence(int start, int end)`
- **Tavsif**: `substring` bilan o'xshash, lekin `CharSequence` qaytaradi.
- **Misol**:
```java
StringBuilder sb = new StringBuilder("Hello, World");
CharSequence seq = sb.subSequence(0, 5);
System.out.println(seq); // Natija: Hello

StringBuffer sbf = new StringBuffer("Java Programming");
System.out.println(sbf.subSequence(5, 16)); // Natija: Programming
```

## 7. `length` va `capacity`
Satr uzunligi va ichki massiv hajmini qaytaradi.

### `length()`
- **Tavsif**: Satrning belgilar sonini qaytaradi.
- **Misol**:
```java
StringBuilder sb = new StringBuilder("Hello");
System.out.println(sb.length()); // Natija: 5

StringBuffer sbf = new StringBuffer("Java");
System.out.println(sbf.length()); // Natija: 4
```

### `capacity()`
- **Tavsif**: Ichki massivning joriy hajmini qaytaradi.
- **Misol**:
```java
StringBuilder sb = new StringBuilder("Hello");
System.out.println(sb.capacity()); // Natija: 21 (16 + 5)

StringBuffer sbf = new StringBuffer("Java");
System.out.println(sbf.capacity()); // Natija: 20 (16 + 4)
```

## 8. `ensureCapacity`
Ichki massivning minimal hajmini belgilaydi.

### `ensureCapacity(int minimumCapacity)`
- **Tavsif**: Agar joriy hajm yetarli bo'lmasa, ichki massivni kengaytiradi.
- **Misol**:
```java
StringBuilder sb = new StringBuilder();
sb.ensureCapacity(50); // Minimal 50 belgi uchun joy
sb.append("Hello");
System.out.println(sb.capacity()); // Natija: 50 yoki undan katta

StringBuffer sbf = new StringBuffer();
sbf.ensureCapacity(100);
sbf.append("Java");
System.out.println(sbf.capacity()); // Natija: 100 yoki undan katta
```

## 9. `setLength`
Satr uzunligini o'zgartiradi.

### `setLength(int newLength)`
- **Tavsif**: Satr uzunligini qisqartiradi yoki uzaytiradi (uzaytirilganda `\0` bilan to'ldiriladi).
- **Misol**:
```java
StringBuilder sb = new StringBuilder("Hello");
sb.setLength(3); // Qisqartirish
System.out.println(sb); // Natija: Hel
sb.setLength(10); // Uzaytirish
System.out.println(sb); // Natija: Hel (keyingi joylar null belgilar bilan to'ldiriladi)

StringBuffer sbf = new StringBuffer("Java");
sbf.setLength(2);
System.out.println(sbf); // Natija: Ja
```

## 10. `charAt` va `setCharAt`
Belgilangan indeksdagi belgini olish yoki o'zgartirish.

### `charAt(int index)`
- **Tavsif**: Belgilangan indeksdagi belgini qaytaradi.
- **Misol**:
```java
StringBuilder sb = new StringBuilder("Hello");
System.out.println(sb.charAt(1)); // Natija: e

StringBuffer sbf = new StringBuffer("Java");
System.out.println(sbf.charAt(2)); // Natija: v
```

### `setCharAt(int index, char ch)`
- **Tavsif**: Belgilangan indeksdagi belgini almashtiradi.
- **Misol**:
```java
StringBuilder sb = new StringBuilder("Hello");
sb.setCharAt(1, 'a');
System.out.println(sb); // Natija: Hallo

StringBuffer sbf = new StringBuffer("Java");
sbf.setCharAt(0, 'j');
System.out.println(sbf); // Natija: java
```

## 11. `toString`
Ob'ektni `String` sifatida qaytaradi.

### `toString()`
- **Tavsif**: `StringBuilder` yoki `StringBuffer` ob'ektini `String`ga aylantiradi.
- **Misol**:
```java
StringBuilder sb = new StringBuilder("Hello");
String result = sb.toString();
System.out.println(result); // Natija: Hello

StringBuffer sbf = new StringBuffer("Java");
System.out.println(sbf.toString()); // Natija: Java
```

## 12. `trimToSize`
Ichki massivning hajmini satr uzunligiga moslashtiradi.

### `trimToSize()`
- **Tavsif**: Ortiqcha xotira joyini qisqartiradi.
- **Misol**:
```java
StringBuilder sb = new StringBuilder(100); // Dastlabki hajm 100
sb.append("Hello");
System.out.println(sb.capacity()); // Natija: 100
sb.trimToSize();
System.out.println(sb.capacity()); // Natija: 5

StringBuffer sbf = new StringBuffer(50);
sbf.append("Java");
System.out.println(sbf.capacity()); // Natija: 50
sbf.trimToSize();
System.out.println(sbf.capacity()); // Natija: 4
```

## Xulosa
`StringBuilder` va `StringBuffer` sinflari satrlar bilan ishlashda samarali va moslashuvchan vositalardir. `StringBuilder` bir oqimli (single-threaded) muhitda tezroq ishlaydi, `StringBuffer` esa ko'p oqimli (multithreaded) muhitda xavfsiz.
