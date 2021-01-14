Java 线程

线程 和 进 程的区别：

线程的基本状态 以及 状态之间的关系

synchronized 关键字的用法
java.util.concurrent.locks.Lock
Lock有比synchronized更精确的线程语义和更好的性能，而且不强制性的要求一定要获得锁。
synchronized会自动释放锁，而Lock一定要求程序员手工释放，并且最好在 finally 块中释放（这是释放外部资源的最好的地方）。

线程池（thread pool）

Executors
newSingleThreadExecutor
newFixedThreadPool
newCachedThreadPool
newScheduledThreadPool