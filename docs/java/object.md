Object 类

有哪些方法：
clone(), equals(), hashCode(), toString(), notify(), notifyAll(),
wait(), finalize(), getClass()

如何实现对象克隆
1). 实现 Cloneable 接口并重写 Object 类中的 clone() 方法；
2). 实现 Serializable 接口，通过对象的序列化和反序列化实现克隆，可以实现真正的深度克隆；


== 和 equals 的区别：
equals 本质上就是 ==，只不过 String 和 Integer 等重写了 equals 方法，把它变成了值比较。

hashCode()相同，equals() 不一定 true：
```java
String str1 = "通话";
String str2 = "重地";
System.out.println(str1.hashCode());
System.out.println(str2.hashCode());
System.out.println(str1.equals(str2));
```