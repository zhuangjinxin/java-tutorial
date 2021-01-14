Java 反射

reflection

获得一个类的类对象的方式：
- 类型.class，如：String.class
- 对象.getClass()，如："hello".getClass()
- Class.forName()，如：Class.forName("java.lang.String")

通过反射创建对象的方式：
- 通过类对象调用newInstance()方法，例如：String.class.newInstance()
- 通过类对象的getConstructor()或getDeclaredConstructor()方法获得构造器（Constructor）对象并调用其newInstance()方法创建对象，例如：String.class.getConstructor(String.class).newInstance("Hello");

通过反射获取和设置对象私有字段的值：
通过类对象的getDeclaredField()方法字段（Field）对象，
然后再通过字段对象的setAccessible(true)将其设置为可以访问，
接下来就可以通过get/set方法来获取/设置字段的值了。

通过反射调用对象的方法：
使用 Method.invoke() 方法
```java
String str = "hello";
Method m = str.getClass().getMethod("toUpperCase");
System.out.println(m.invoke(str));
```