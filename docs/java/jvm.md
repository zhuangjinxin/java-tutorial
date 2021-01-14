Java 虚拟机

JVM

JDK 与 JRE 的区别：
JDK：Java Development Kit 的简称，java 开发工具包，提供了 java 的开发环境和运行环境。
JRE：Java Runtime Environment 的简称，java 运行环境，为 java 的运行提供了所需环境。

栈(stack)
堆(heap)
方法区(method area)

GC () 垃圾收集

System.gc()
Runtime.getRuntime().gc()

JVM 参数：
```
-Xms / -Xmx — 堆的初始大小 / 堆的最大大小
-Xmn — 堆中年轻代的大小
-XX:-DisableExplicitGC — 让System.gc()不产生任何作用
-XX:+PrintGCDetails — 打印GC的细节
-XX:+PrintGCDateStamps — 打印GC操作的时间戳
-XX:NewSize / XX:MaxNewSize — 设置新生代大小/新生代最大大小
-XX:NewRatio — 可以设置老生代和新生代的比例
-XX:PrintTenuringDistribution — 设置每次新生代GC后输出幸存者乐园中对象年龄的分布
-XX:InitialTenuringThreshold / -XX:MaxTenuringThreshold：设置老年代阀值的初始值和最大值
-XX:TargetSurvivorRatio：设置幸存区的目标使用率
```
常用参数：-Xms、-Xmx

内存泄漏 OOM