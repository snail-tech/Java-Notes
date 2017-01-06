# ImJavaer(进阶篇)
本项目存放自己平时敲的示例代码，并会在`README.md`中记录，以便自己忘了的时候回来看。每个类中都有测试代码，直接运行可查看效果。

- JDK使用版本: 1.7
- 构建工具: Maven

## 项目结构及内容简介

####Java And Concurrency
    |com.elong.concurrency  //并发编程模块
        |UnsafeSequence.java
        |-----------------  //非线程安全的数值生成器
        |Sequence.java
        |-----------------  //线程安全的数值生成器
        |NoVisibility.java
        |-----------------  //在没有同步的情况下共享变量
        |OneValueCache.java
        |-----------------  //对数值及其因数分解结果进行缓存的不可变容器类
        |PersonSet.java
        |-----------------  //通过实例封闭和加锁机制使一个类成为线程安全的(类的状态变量并不是线程安全的)
        |TestHarness.java
        |-----------------  //同步工具类: 闭锁: 使用CountDownLatch类启动和停止线程
        |BoundedHashSet.java
        |-----------------  //同步工具类: 使用Semaphore为容器设置边界
        |barrierTest.java
        |-----------------  //同步工具类: CyclicBarrier
        |custom.cache.*
        |-----------------  //构建高效的、可伸缩的结果缓存
        |BrokenPrimeProducer.java
        |-----------------  //素数阻塞队列示例
        |BlockingQueue.java
        |-----------------  //一个阻塞队列的简单实现
        |CASDemo.java
        |-----------------  //原子包boolean原子性示例
        |FairLock.java
        |-----------------  //公平锁的实现
        |Lock.java
        |Synchronizer.java
        |LockTest.java
        |-----------------  //锁的实现与测试
        |MyWaitNotify.java
        |-----------------  //测试notify和wait的执行流程
        |QueueObject.java
        |-----------------  //信号量对象
        |ReadWriteLock.java
        |-----------------  //可重入的读写锁
        |ThreadLocalTest.java
        |-----------------  //ThreadLocalTest
        |TreeNode.java
        |-----------------  //死锁示例
        
####Design Patterns
    |com.elong.design.patterns  //设计模式
        |EnumSingleton.java
        |SingletonObject.java
        |-----------------  //单例模式
        |Service.java
        |Provider.java
        |Services.java
        |-----------------  //服务提供者模式
        |Student.java
        |-----------------  //Builder模式
        |SetObserver.java
        |ForwardingSet.java
        |ObservableSet.java
        |-----------------  //避免过度同步(观察者模式)
        
####Java Best Practices
    |com.peierlong.best.practices   //最佳实践
        |PhoneNumber.java
        |-----------------  //覆盖equals的同时要覆盖hashCode
        |Complex.java
        |-----------------  //使可变性最小化
        |Figure.java
        |FigureTrue.java
        |-----------------  //类层次优于标签类
        |Favorites.java
        |-----------------  //类型安全的异构容器的实现
        |AnnotatedElement.java
        |-----------------  /使用asSubclass方法在编译时读取类型未知的注解
        |Operation.java
        |-----------------  //利用枚举类型来实现特定运算
        |ReflectiveTest.java
        |-----------------  //使用反射类获取对象的实例
        |Phase.java
        |-----------------  //使用嵌套的EnumMap来构建关联的一对枚举
        |Period.java
        |-----------------  //必要时进行保护性拷贝
        
####Java NIO
    |com.peierlong.nio  //NIO使用示例
        |TiemServer.java
        |MultiplexerTimeServer.java
        |-----------------  //NIO创建的TimeServer服务端
        |TimeClient.java
        |TimeClientHandle.java
        |-----------------  //NIO创建的TimeClient客户端
        