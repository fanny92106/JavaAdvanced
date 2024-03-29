# <Generic>

1. Basic

        - jdk1.5之后加入
        - 类型安全 (编译时就会进行类型检查, 保证数据类型安全)
        - 安全地向下强制转型操作
        - 不能使用原始数据类型
        - Java 强类型的体现
        - 如果没有指定特定泛型, 默认类型为java.lang.Object类型
        - 泛型类可能有多个参数, 此时应将多个参数一起放在尖括号内, eg: <E1,E2,E3>
        - 泛型类的构造器如下: public GenericClass(){...}, 不带泛型<T>
        - 泛型不同的引用不能相互赋值
            ArrayList<String> list1 = ..
            ArrayList<Integer> list2 = ..
            list1 = list2 (xxx)
        - 泛型如果不指定, 将被擦除, 泛型对应的类型均按照Object处理, 但不等价于Object. 经验: 泛型要使用一路都用, 要不用一路都不要用
        - 静态方法中不能使用泛型 (static要早于实例化)
        - 自定义异常类不能声明带有泛型, 也不能catch带泛型的异常
            public class MyException<T> extends Exception {}
        
        
2. 自定义泛型类, 泛型接口, 泛型方法

        - 在方法中出现了泛型的结构, 泛型参数与类的泛型参数没有任何关系.
        即泛型方法所属的类是不是泛型类都没有关系

![GenericClassAndGenericMethod](imagePool/GenericClassAndGenericMethod.png)

![GenericUseCase](imagePool/GenericUseCase.png)

        - 重点: 子类继承带泛型的父类 (eg: DAO操作CrudRepository)

![DAOBaseClass](imagePool/DAOBaseClass.png)

![StudentDAOExtendsDAOBaseClass](imagePool/StudentDAOExtendsDAOBaseClass.png)



3. 泛型在继承方面的体现

        - 类A是类B的父类, G<A>和G<B>二者不具备父子类关系, 二者是并列关系
![List<Object>AndList<String>](imagePool/List<Object>AndList<String>.png)

       - 使用通配符声明公共父类, 但就不能用它来添加数据, 除了null
![ParentGenericClass](imagePool/ParentGenericClass.png)

       - 有限制条件的通配符?
            ? extends Person: ?代表的类型是Person类或Person子类
            ? super Person: ?代表的类型是Person类或Person父类
