# Super keyword




### super 调用属性和方法

    1). 在子类的方法和构造器中，通过 "super.属性" 或 "super.方法" 的方式，显示地调用父类中声明的属性或方法。通常情况下 (即子类和父类中的定义的属性名和方法名不同时), 我们都省略"super." 而直接调用属性和方法
    2). 当子类和父类中定义了同名的属性时，我们想要在子类中调用父类中声明的属性，则必须显示地使用"super.属性"的方式，表明
    调用的是父类中声明的属性；当子类重写了父类中的方法后，我们想在子类的方法中调用父类中被重写的方法时，则必须显式地使用
    “super.方法"的方式，表明调用的是父类中被重写的方法
    
    

### super 调用构造器

    1). 我们可以在子类的构造器中显式地使用"super(形参列表)"的方式，调用父类中声明的指定的构造器。
    2). ”super(形参列表)"的使用，必须生命在子类构造器的首行
    3). 在构造器的首行，如果没有显式地声明“this(形参列表)" 或"super(形参列表)", 则默认调用的是父类中空参构造器
    4). 在类的多个构造器中，至少有一个类的构造器使用了"super(形参列表)", 调用了父类中的构造器



### 子类对象实例化的全过程

    1). 从结果上来看: （继承性)
        子类继承父类以后，就获取了父类中声明的属性或方法
        创建子类的对象，在堆空间中，就会加载所有父类中声明的属性
        
    2). 从过程上来看: 
        当我们通过子类的构造器创建子类对象时，我们会直接或间接地调用父类的构造器，进而调用父类的父类的构造器，直到调用了
        java.lang.Object类中的空参构造器为止。正因为加载过所有的父类的结构，所以才可以看到内润中有父类中的结构，子类对象
        才可以考虑进行调用
        
        
        明确: 虽然创建子类对象时，调用了父类的构造器，但是自始至终就创建过一个对象，即为new的子类对象
        new + 构造器 才会创建对象

