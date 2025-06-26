# Java Core Questions and Answers

## Computer program nima?
Kompyuter dasturi - bu kompyuter tomonidan bajariladigan ko'rsatmalar (instruktsiyalar) to'plami bo'lib, muayyan vazifani bajarish uchun yoziladi. U odatda dasturlash tilida yoziladi va kompyuter tushunadigan mashina kodiga aylantiriladi.

## Nima uchun hamma dasturlashni o'rganishi kerak?
Dasturlashni o'rganish mantiqiy fikrlash, muammolarni hal qilish ko'nikmalarini rivojlantiradi, avtomatlashtirishni osonlashtiradi va zamonaviy texnologiyalar dunyosida raqobatbardoshlikni oshiradi. Bu har qanday sohada foydali bo'lishi mumkin.

## Java birinchi nomi nima edi?
Java dasturlash tili birinchi marta **Oak** deb nomlangan.

## Java nechta featurelar bor?
Java'ning asosiy xususiyatlari (features) quyidagilar: platformadan mustaqillik, ob'ektga yo'naltirilganlik, xavfsizlik, mustahkamlik, ko'p oqimli (multithreading), oddiylik, dinamiklik va boshqalar. Umumiy hisobda 10-12 ta asosiy xususiyatni sanash mumkin, lekin bu kontekstga bog'liq.

## Compiler nima?
Compiler - bu yuqori darajadagi dasturlash tilida yozilgan kodni mashina tili (bytecode yoki binary kod) ga aylantiradigan dastur. Java'da bu **javac** deb ataladi.

## Interpreter nima?
Interpreter - bu kodni qator-ma-qator o'qib, uni to'g'ridan-to'g'ri bajaradigan dastur. Java'da JVM (Java Virtual Machine) bytecode'ni interpretatsiya qiladi.

## JDK nima?
JDK (Java Development Kit) - Java dasturlarini ishlab chiqish uchun zarur bo'lgan vositalar to'plami, jumladan compiler (javac), JRE va boshqa vositalarni o'z ichiga oladi.

## JLS nima?
JLS (Java Language Specification) - Java dasturlash tilining rasmiy hujjati bo'lib, uning sintaksisi, semantikasi va xatti-harakatlarini belgilaydi.

## JRE nima?
JRE (Java Runtime Environment) - Java dasturlarini ishga tushirish uchun zarur bo'lgan muhit bo'lib, JVM, standart kutubxonalar va boshqa komponentlarni o'z ichiga oladi.

## JVM nima?
JVM (Java Virtual Machine) - Java bytecode'ni ishga tushiradigan virtual mashina bo'lib, platformadan mustaqil ishlashni ta'minlaydi.

## Devtools nima?
Devtools (Developer Tools) - dasturchilar uchun mo'ljallangan vositalar to'plami, masalan, IDE, debugger, compiler va boshqa vositalar dastur ishlab chiqishni osonlashtiradi.

## JDK components?
JDK komponentlari: **javac** (compiler), **java** (JVM), **javadoc**, **jar**, **jdb** (debugger), standart kutubxonalar va boshqa vositalar.

## Bytecode nima?
Bytecode - Java kodi kompilyatsiya qilinganda hosil bo'ladigan oraliq, platformadan mustaqil mashina kodi bo'lib, JVM tomonidan ishga tushiriladi.

## Token nima?
Token - bu Java kodi tarkibidagi eng kichik sintaktik birliklar, masalan, kalit so'zlar, identifikatorlar, operatorlar, literal va boshqalar.

## Translation unit nima?
Translation unit - kompilyator tomonidan birgalikda tahlil qilinadigan va kompilyatsiya qilinadigan kodning bir qismi, odatda bitta `.java` fayli.

## Java-da Tokenlarni nechta type mavjud?
Java'da tokenlar 5 ta asosiy turga bo'linadi: kalit so'zlar, identifikatorlar, literal, operatorlar va separatorlar.

## Java-da Character Set nima?
Java'da Character Set - bu Java dasturlarida ishlatiladigan belgilarni ifodalash uchun ishlatiladigan Unicode standartidir.

## Identifiers nima va Identifiers qoidalari?
Identifiers - o'zgaruvchilar, metodlar yoki sinflarga berilgan nomlar. Qoidalar: harf yoki pastki chiziq (_) bilan boshlanishi kerak, raqam bilan boshlanmaydi, kalit so'z bo'lmasligi kerak va Unicode belgilarni qo'llab-quvvatlaydi.

## Java-da nechi xil turdagi commentlar bor?
Java'da 3 xil comment turi mavjud: bir qatorli (`//`), ko'p qatorli (`/* */`) va dokumentatsiya (`/** */`).

## Java-da nechta keywordlar bor?
Java'da 57 ta kalit so'z (keyword) mavjud, masalan, `class`, `int`, `if`, `for` va boshqalar.

## Java-da nechta turdagi variablelar mavjud?
Java'da 3 turdagi o'zgaruvchilar mavjud: local, instance va static.

## Java-da primative type bilan non-primative nima farqi bor?
Primitive tiplar (`int`, `double`, `boolean`) - oddiy ma'lumot turlari, xotirada to'g'ridan-to'g'ri saqlanadi. Non-primitive tiplar (`String`, `Array`, sinflar) - ob'ektlarga ishora qiladi va xotirada reference sifatida saqlanadi.

## Variable scope nima?
Variable scope - o'zgaruvchining dastur ichida ko'rinadigan yoki ishlatiladigan sohasi (masalan, metod ichida yoki sinf ichida).

## Java-da qancha scopelar mavjud?
Java'da 3 ta asosiy scope mavjud: local scope, instance scope va class (static) scope.

## Java-ni nechinchi versiyasidan Scanner qo'shilgan?
`Scanner` sinfi Java 1.5 (JDK 5) versiyasida qo'shilgan.

## Scanner class qanday resourcelardan ma'lumotlarni o'qiy oladi?
`Scanner` klaviatura (System.in), fayllar, stringlar va boshqa input stream'lardan ma'lumot o'qiydi.

## Java-da nechi xil turdagi data type bor?
Java'da 2 turdagi data tiplari mavjud: primitive (8 ta: `byte`, `short`, `int`, `long`, `float`, `double`, `char`, `boolean`) va non-primitive (sinflar, interfeyslar, massivlar).

## Scanner bug?
`Scanner` sinfida ma'lum "bug"lar mavjud, masalan, `nextLine()` metodi oldingi `nextInt()` yoki `next()` dan keyin qoldiq newline belgisini o'qishi mumkin, bu noto'g'ri inputga olib keladi.

## Console class nima?
`Console` sinfi - foydalanuvchi bilan terminal orqali o'zaro aloqa qilish uchun ishlatiladigan sinf, masalan, parol kiritish yoki formatlangan chiqish uchun.

## Javani nechinchi versiyasida Console taqdim etilgan?
`Console` sinfi Java 1.6 (JDK 6) da taqdim etilgan.

## Scanner va Console o'rtasidagi farq?
`Scanner` umumiy ma'lumot o'qish uchun, `Console` esa terminalga xos operatsiyalar (masalan, parol kiritish) uchun ishlatiladi. `Console` faqat terminal muhitida ishlaydi.

## Scanner class va undan foydalanish
`Scanner` sinfi foydalanuvchi kiritgan ma'lumotlarni o'qish uchun ishlatiladi. Misol:

```java
import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.println("Ismingizni kiriting: ");
        String name = scanner.nextLine();
        System.out.println("Salom, " + name);
        scanner.close();
    }
}
```

## Java-da Operator nima?
Operator - ma'lumotlarni qayta ishlash yoki amal bajarish uchun ishlatiladigan belgi yoki ifoda, masalan, `+`, `-`, `*`.

## Operandlar soniga qarab Operatorlar nechi turga bo'linadi?
Operatorlar 3 turga bo'linadi: unary (1 operand), binary (2 operand), ternary (3 operand).

## Unary operator nima?
Unary operator - faqat bitta operand bilan ishlaydigan operator, masalan, `++`, `--`, `!`.

## Binary operator nima?
Binary operator - ikkita operand bilan ishlaydigan operator, masalan, `+`, `-`, `*`, `/`.

## Ternary operator nima?
Ternary operator - uchta operand bilan ishlaydigan shartli operator (`?:`), masalan: `x > y ? x : y`.

## Expression nima?
Expression - qiymat qaytaradigan operatorlar, o'zgaruvchilar yoki literallarning kombinatsiyasi, masalan, `x + y`.

## Java-da named operator nima?
Java'da "named operator" degan tushuncha mavjud emas. Bu atama odatda boshqa tillarda ishlatilishi mumkin.

## Java-da Arithmetic operator nima?
Arithmetic operatorlar - matematik amallarni bajarish uchun ishlatiladi: `+`, `-`, `*`, `/`, `%`.

## Java-da Arithmetic operationlarni priority levellar qanday?
Prioritet: `()` > `*`, `/`, `%` > `+`, `-`.

## Java-da Relational operatorlar nima?
Relational operatorlar - qiymatlarni solishtirish uchun ishlatiladi: `==`, `!=`, `>`, `<`, `>=`, `<=`.

## Java nechta turdagi Relation operatorlarni qo'llab quvvatlaydi?
Java 6 ta relational operatorni qo'llab-quvvatlaydi: `==`, `!=`, `>`, `<`, `>=`, `<=`.

## Java-da Logical operatorlar nima?
Logical operatorlar - mantiqiy shartlarni baholash uchun ishlatiladi: `&&`, `||`, `!`.

## Java nechta turdagi Logical operatorlarni qo'llab quvvatlaydi?
Java 3 ta logical operatorni qo'llab-quvvatlaydi: `&&`, `||`, `!`.

## Java-da Assignment operator nima?
Assignment operator - o'zgaruvchiga qiymat belgilash uchun ishlatiladi, masalan, `=`, `+=`, `-=`.

## x += y va x = x + y expressionlari o'rtasida farq bormi?
Ikki ifoda funksional jihatdan bir xil, lekin `x += y` qisqaroq yoziladi va ba'zi hollarda optimallashtirilgan bo'lishi mumkin.

## Execution Flow nima?
Execution Flow - dastur kodining bajarilish tartibi, odatda yuqoridan pastga yoki shartlarga qarab.

## Control Flow nima?
Control Flow - dastur oqimini boshqarish uchun ishlatiladigan tuzilmalar, masalan, `if`, `for`, `while`.

## if nima?
`if` - shartli operator bo'lib, shart to'g'ri bo'lsa ma'lum kod blokini bajaradi.

## if nima uchun ishlatamiz?
`if` shartlarga asoslangan qaror qabul qilish uchun ishlatiladi.

## Loop nima?
Loop - kod blokini bir necha marta takrorlash uchun ishlatiladigan tuzilma, masalan, `for`, `while`.

## Loop nima uchun ishlatamiz?
Loop takroriy vazifalarni avtomatlashtirish uchun ishlatiladi.

## Java-da Control Flow ning nechi xil turi mavjud?
Java'da 3 turdagi control flow mavjud: shartli (`if`, `switch`), tsiklik (`for`, `while`, `do-while`) va o'tkazish (`break`, `continue`, `return`).

## Switch statement qanday ishlaydi?
`switch` ma'lum bir o'zgaruvchi qiymatiga qarab turli case'larni bajaradi. Har bir `case` shartga mos kelsa, tegishli kod bloki ishga tushadi.

## Unicode system nima uchun kerak?
Unicode - turli tillardagi belgilarni bir xil standartda ifodalash uchun ishlatiladi, bu global dasturlarni qo'llab-quvvatlash uchun muhim.

## ansi escape code nima?
ANSI escape code - terminalda rang, format yoki kursor harakatini boshqarish uchun ishlatiladigan maxsus belgilar ketma-ketligi.

## Function nima?
Function - ma'lum bir vazifani bajaradigan kod bloki bo'lib, ko'pincha boshqa tillarda ishlatiladigan atama.

## Function va Method o'rtasidagi farq nima?
Method - sinf ichida aniqlangan funksiya. Function esa umumiy atama bo'lib, sinfdan tashqarida ham ishlatilishi mumkin.

## Method Definition nima?
Method Definition - metodning to'liq ta'rifi: header (imzo) va body (kod bloki).

## Method Declaration (header) nima?
Method Declaration - metodning nomi, qaytarish turi, parametrlari va modifikatorlaridan iborat qismi.

## Method Signature nima?
Method Signature - metodning nomi va parametrlari (qaytarish turi kirmaydi).

## Method body nima?
Method body - metodning bajariladigan kod bloki.

## Stack nima?
Stack - dastur xotirasining LIFO (Last In, First Out) tartibida ishlaydigan qismi, metod chaqiruvlari va local o'zgaruvchilar saqlanadi.

## Stack Frame nima?
Stack Frame - har bir metod chaqiruvi uchun yaratiladigan stackdagi ma'lumotlar bloki, o'zgaruvchilar va metod ma'lumotlarini saqlaydi.

## Recursion nima?
Recursion - metodning o'zini ichida chaqirishi, muammoni kichikroq qismlarga bo'lib hal qilish uchun ishlatiladi.

## Method qachon recursive method deb ataladi?
Metod o'zini to'g'ridan-to'g'ri yoki bilvosita chaqirsa, recursive metod deb ataladi.

## Group of recursions?
Rekursiyalar guruhlari: to'g'ridan-to'g'ri (direct) va bilvosita (indirect) rekursiya.

## Type of recursions?
Rekursiya turlari: linear, tail, binary, mutual va nested recursion.

## Java-da String nima?
`String` - Java'da belgilar ketma-ketligini ifodalovchi sinf.

## Java-da String ni nechi xil usulda yaratishimiz mumkin?
`String`ni 2 usulda yaratish mumkin: literal (`"Hello"`) va `new String()` konstruktor yordamida.

## Java-da String nima uchun immutable?
`String` immutable, chunki uning qiymati o'zgartirilmaydi, bu xavfsizlik va optimallashtirish uchun muhim.

## Java-da String classning superclassni nima?
`String` sinfining superclass'i `Object`.

## Array nima?
Array - bir xil turdagi ma'lumotlarni saqlash uchun ishlatiladigan ma'lumotlar tuzilmasi.

## Java-da Arrayni qanday e'lon qilishimiz mumkin?
```java
int[] arr; // e'lon qilish
arr = new int[5]; // yaratish
int[] arr2 = {1, 2, 3}; // e'lon va initialize
```

## Turli data typelar uchun Arrayning default qiymat qanday?
- `int`: 0
- `double`: 0.0
- `boolean`: false
- `Object`: null

## Java-da Array yaratilgandan keyin uni size ni o'zgartira olamizmi?
Yo'q, array o'lchami o'zgarmaydi (fixed size).

## Arrayni size ni manfiy raqam belgilay olamizmi?
Yo'q, manfiy o'lcham `NegativeArraySizeException` tashlaydi.

## Arrayni array size siz e'lon qila olamizmi?
Ha, lekin faqat e'lon qilish mumkin (`int[] arr;`), ammo yaratishda o'lcham kerak.

## Array JVM xotirasi qayerida saqlanadi?
Array'lar heap xotirasida saqlanadi.

## Java-da primative Array JVM qaysi xotirasida saqlanadi?
Primitive array'lar ham heap xotirasida saqlanadi.

## ArrayStoreException nima? Bu exception qachon tashlanadi?
`ArrayStoreException` - array'ga noto'g'ri turdagi element qo'shilganda tashlanadi, masalan, `Integer` array'ga `String` qo'shish.

## Java-da anonymous Array nima? Misol keltiring?
Anonymous array - nomi bo'lmagan, bir marta ishlatiladigan array. Misol:
```java
new int[] {1, 2, 3};
```

## Agar arrayni initialize qilmasangiz nima bo'ladi?
Agar array initialize qilinmasa, uning elementlari default qiymatlarga ega bo'ladi (masalan, `int` uchun 0).

## Java-da Jagged Array nima?
Jagged Array - har bir qatori turli o'lchamga ega bo'lgan 2D array.

## Array ni afzalliklari nimada?
- Tez kirish (index orqali)
- Oddiy va samarali
- Bir xil turdagi ma'lumotlarni saqlash

## Array ni kamchiliklari nimada?
- Fixed size
- Dinamik ravishda o'zgartirib bo'lmaydi
- Insert/delete operatsiyalari sekin

## Java-da String Constant pool nima?
String Constant Pool - heap xotirasidagi maxsus joy bo'lib, string literallar saqlanadi va takroriy foydalanish uchun optimallashtiriladi.

## Java-da String literal nima?
String literal - qo'shtirnoq ichidagi matn, masalan, `"Hello"`.

## String literal xotirada qanday saqlanadi?
String literallar String Constant Pool'da saqlanadi.

## Nima uchun Java String literaldan foydalanadi?
String literallar xotirani tejash va samaradorlikni oshirish uchun ishlatiladi.

## Quyidagi code da nechta object yaratiladi?
```java
String s = new String("Hello");
```
2 ta ob'ekt: `"Hello"` (String Pool'da) va `new String` (heap'da).

## Quyidagi code da nechta object yaratiladi?
```java
String s1 = new String("Scientech");
String s2 = new String("Scientech");
String s3 = "Scientech";
String s4 = "Scientech";
```
3 ta ob'ekt: `"Scientech"` (String Pool'da), `s1` va `s2` uchun alohida heap'da.

## String class qanday interfacelardan implement olgan?
`String` sinfi `Serializable`, `Comparable`, `CharSequence` interfeyslarini implement qiladi.

## String Thread-safe mi?
Ha, `String` immutable bo'lgani uchun thread-safe.

## String classni kamchiliklari?
- Immutable bo'lgani uchun tez-tez o'zgartirish qimmat
- Ko'p string operatsiyalari xotirani ko'p ishlatadi

## String wrapper classmi?
Yo'q, `String` wrapper sinf emas, lekin `Character` wrapper sinf hisoblanadi.

## String intern() method nima uchun ishlatiladi?
`intern()` String Pool'dagi stringga ishora qilish uchun ishlatiladi, xotirani tejaydi.

## Java-da Formatting nima?
Formatting - ma'lumotlarni muayyan formatda ko'rsatish, masalan, `String.format()` yordamida.

## String classni format() method javani nechinchi versiyasida taqdim etilgan?
`String.format()` Java 1.5 (JDK 5) da taqdim etilgan.

## String classni format method qachon ishlatishimiz kerak?
Matnni formatlash, masalan, o'zgaruvchilarni string ichiga joylashtirish uchun ishlatiladi.

## '%s' belgisini nima uchun ishlatamiz?
`%s` - `String.format()` da string qiymatni joylashtirish uchun ishlatiladi.

## Java-da MessageFormat class nima uchun ishlatamiz?
`MessageFormat` - dinamik va lokalizatsiya qilingan matnlarni formatlash uchun ishlatiladi.

## MessageFormat format() method nima?
`MessageFormat.format()` - ma'lumotlarni belgilangan shablon asosida formatlaydi.

## string format methodiga bitta misol yozing.
```java
String formatted = String.format("Ism: %s, Yosh: %d", "Ali", 25);
System.out.println(formatted); // Ism: Ali, Yosh: 25
```

## string format method foydalanib kirib kelgan strngga "Welcome to " qo'shimchasini qo'shib ekranga chiqaruvchi dastur yozing.
```java
import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.println("Matn kiriting: ");
        String input = scanner.nextLine();
        String result = String.format("Welcome to %s", input);
        System.out.println(result);
        scanner.close();
    }
}
```

## Programming Principles nima?
Programming Principles - samarali va sifatli kod yozish uchun qoidalar, masalan, DRY, KISS, SOLID.

## Qanday qilib effective code yozasiz?
- Oddiy va aniq kod yozish
- DRY va KISS tamoyillariga rioya qilish
- Modullilik va reusable kod
- Yaxshi nomlash va sharhlar

## DRY nima?
DRY (Don't Repeat Yourself) - kod takrorlanishini minimallashtirish tamoyili.

## KISS nima?
KISS (Keep It Simple, Stupid) - kodni iloji boricha oddiy va tushunarli qilish tamoyili.
