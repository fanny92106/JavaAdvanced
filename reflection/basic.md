# Reflection
        
    
1. why

        - 动态性
        
2. what
    
        - 在运行时判断任意一个对象所属的类
        - 在运行时构造任意一个类的对象
        - 在运行时"判断"任意一个"类"所具有的成员变量和方法
        - 在运行时"调用"任意一个"对象"的成员变量和方法
        - 在运行时处理注解
        - 在运行时获取泛型信息
        - 生成动态代理

3. 反射相关的主要API

        - java.lang.Class
        - java.lang.reflect.Method
        - java.lang.reflect.Field
        - java.lang.reflect.Constructor
        
4. Simple Case

![PersonClass](imagePool/PersonClass.png)
![ReflectionSimpleCase](imagePool/ReflectionSimpleCase.png)


5. java.lang.Class 类

        - 类的加载过程: java.exe命令对某个字节码文件进行解释运行时， JVM会将编译后的.class文件加载到内存中
        - Class的实例: 内存中被加载的这些类就是"运行时类"，作为Class的实例
        - 获取运行时类的 4种 方式: 
![getRuntimeClassInstance](imagePool/getRuntimeClassInstance.png)


6. 哪些类型可以有Class对象

        - 外部类，成员内部类，静态内部类，局部内部类，匿名内部类
        - interface 接口
        - []: 数组
        - enum: 枚举
        - annotation: 注解
        - primitive type: 基本数据类型
        - void
        - Object
        - Class 


7. 反射的使用场景

        - a.创建运行时类的对象 (eg: 框架中大量使用反射，容器通过反射创建JavaBean, 子类继承父类时保证调用super()时，父类有此无参构造器)
![createRuntimeClassObject](imagePool/createRuntimeClassObject.png)

           动态性的体现
![dynamicReflection](imagePool/dynamicReflection.png)
