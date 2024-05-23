# java笔记

## 多线程编程

### 线程池

1. Runnable、Callable、Future之前的区别和联系

- Runnable接口的run方法实现任务执行逻辑，run函数没有返回值，启动线程运行任务，本质通过Runnable接口实现。

- Callable接口类似于 Runnable，但是它可以返回任务执行的结果，并且可以抛出异常。Thread类不能直接使用Callable接口。

- Future接口表示推迟计算的结果。该接口提供方法检查任务是否完成，获取任务的结果。

2. FeatureTask

FeatureTask类实现了RunnableFuture接口，该接口继承了Runnable和Future接口。该类用于将Runnable和Callable任务提交给线程执行，并通过Future接口获取任务的执行结果。

3. ExecutorService

ExecutorService接口是Java中用于管理和执行异步任务的高级接口。它扩展了Executor接口，提供了更多的功能和控制，使得在多线程环境中更加灵活地管理任务的执行，包括：

- 任务的提交和获取任务结果Feature

- shutdown任务

- 检查任务是否被关闭

4. Executors和ThreadPoolExecutors

Executors提供了创建线程池的静态方法，这些静态方法调用ThreadPoolExecutors创建线程池。


## 函数式编程

1. 函数式编程的优点：行为参数化

2. lambda表达式相比匿名内部类更加简洁

3. 函数式接口：只有一个抽象方法的接口

4. lambda表达式允许你直接以内联的形式为函数式接口的抽象方法提供实例，并把lambda表达式作为函数式接口一个具体实现的实例。

5. 方法引用：方法引用可以被看作仅仅调用特定方法的Lambda的一种快捷写法。


## 流

1. 流允许以声明性方式处理数据集合，类似SQL语句，优点：

- 代码易读

- 可以把几个基础操作链接在一起构成流水线操作

- 可以利用多线程


2. 源

流会使用一个提供数据的源，例如集合、输入和输出资源。

3. 数据处理操作

- 中间操作，结果还是一个流

    - filter、map、reduce、find、match、sort、collect、limit

- 终端操作，关闭流

    - collect

4. 流与集合之间的区别

流与集合之间的差异在于什么时候计算。集合包含数据结构中的所有值，流则按需计算，无需全部元素


5. 流操作

- 筛选操作：filter

- 切片操作：skip，limit

- 映射：map，flatmap

- 查找：findFirst、findAny返回元素

- 匹配：anyMatch、allMatch是否存在，返回boolean值

- 归约操作：reduce(parm1, (parm1, parm2) -> item)

6. 构建流

- 由数值创建流: Stream.of(parm1, parm2, ...)

- 由数组创建流：Arrays.stream(stream)

- 由文件生成流：Files.lines

- 由函数生成流：stream.iterate, stream.generate

  - stream.iterate(parm1, itemA -> itemB)

  - stream.generate(Supplier<T>)

7. 收集操作

- 归约操作

  - Collectors.counting, Collectors.joining, Collectors.reducing 

- 分组、分区

  - Collectors.groupingBy, Collectors.partitionBy
  










