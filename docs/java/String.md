Java String

String、StringBuilder、StringBuffer 区别
String 声明的是不可变的对象，每次操作都会生成新的 String 对象，然后将指针指向新的 String 对象;
StringBuffer、StringBuilder 可以在原有对象的基础上进行操作;

StringBuffer 是线程安全的，而 StringBuilder 是非线程安全的，
但 StringBuilder 的性能却高于 StringBuffer，
在单线程环境下推荐使用 StringBuilder，多线程环境下推荐使用 StringBuffer

String 常用方法：
* length()：返回字符串长度
* equals()：字符串比较
* substring()：截取字符串
* replace()：字符串替换
* replaceAll()：字符串替换
* trim()：去除字符串两端空白
* split()：分割字符串，返回一个分割后的字符串数组
* indexOf()：返回指定字符的索引
* charAt()：返回指定索引处的字符
* getBytes()：返回字符串的 byte 类型数组
* toLowerCase()：将字符串转成小写字母
* toUpperCase()：将字符串转成大写字符


字符串反转:
```java
// StringBuffer reverse
StringBuffer stringBuffer = new StringBuffer();
stringBuffer.append("abcdefg");
System.out.println(stringBuffer.reverse()); // gfedcba

// StringBuilder reverse
StringBuilder stringBuilder = new StringBuilder();
stringBuilder.append("abcdefg");
System.out.println(stringBuilder.reverse()); // gfedcba
```