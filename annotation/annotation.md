# Annotation


### Definition
    - 框架 = 注解 + 反射 + 设计模式
    - JDK5.0开始，Java增加了对元数据(meta data)的支持，即Annotation
    
    
### Use Case
    1. 生成文档相关的注解  
        - @param
        - @author
    2. 在编译时进行格式检查(JDK内置的三个基本注解)
        - @Override: 编译时校验子类重写方法的正确性，只能用于方法
        - @Deprecated: 表示修饰的元素(类，属性，构造器，方法)已过时，但仍可使用
        - @SuppressWarnings: 抑制编译器警告, eg: 变量定义后未使用
    3. 跟踪代码依赖性，实现替代配置文件的功能
        - @Component


## 
