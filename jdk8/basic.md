# Java 8的新特性

0. Overview

![Java8Overview](image/Java8Overview.png)
        

1. Lambda表达式
            
            1). 总结：
                    - 本质: 函数式接口的实例化
                    - 以前用匿名实现类表示的现在都可以用lambda表达式来做
                    - 函数式接口: 必须是函数式接口(即只有一个抽象方法)
            1). 左边: 形参列表
                    - 如果lambda形参列表只有一个参数, 一堆()可以省略; 
                    - 多于一个时, 不能省略
                    - 参数类型往往可以省略
            2). 右边: lambda体
                    - 应该使用{}进行包裹
                    - 如果只有一条执行语句, 则{}可以省略, 以及return关键字 (如果{}省了, return一定省掉!!)

![Lambda_Case_1](image/Lambda_Case_1.png)
![Lambda_Case_2](image/Lambda_Case_2.png)

                    
2. Functional Interface 函数式接口

        - 如果一个接口中只声明了一个抽象方法, 则为函数式接口
        - annotation: @FunctionalInterface
        - 在java.util.function包下定义了java 8的丰富的函数式接口
        - java内置的4大核心函数式接口
            1). 消费型接口 Consumer<T>,    void accept(T t)
            2). 供给型接口 Supplier<T>,    T get()
            3). 函数型接口 Function<T, R>, R apply(T t)
            4). 断定型接口 Predicate<T>,   boolean test(T t)


3. 方法引用:
        
        - 本质: 函数式接口的实例化
        - 使用要求: 接口中的抽象方法的形参列表和返回值类型与方法引用的方法的形参列表和返回值类型相同!!
        - 三种使用场景:
            1) 对象 ：： 非静态方法
![MethodRefObjCallNonstaicMethod](image/MethodRefObjCallNonstaicMethod.png)
    
            2) 类 ：： 静态方法
![MethodRefClassCallStaticMethos](image/MethodRefClassCallStaticMethos.png)
            
            3) 类 ：： 非静态
                ...
