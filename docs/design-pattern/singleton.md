单例模式

饿汉式：
```java
public class Singleton {
    private Singleton(){}
    private static Singleton instance = new Singleton();
    public static Singleton getInstance(){
        return instance;
    }
}
```

懒汉式：
```java
public class Singleton {
    private Singleton() {}
    private static Singleton instance = null;
    public static synchronized Singleton getInstance(){
        if (instance == null) {
            instance ＝ new Singleton();
        }  
        return instance;
    }
}
```