# Proxy


1. 静态代理: 
    
        - 代理类和被代理类在编译期间就确定下来了
![staticProxyClass](imagePool/staticProxyClass.png)
![staticProxyUseCase](imagePool/staticProxyUseCase.png)


2. 动态代理: 

        - 由代理工厂在运行时动态地生产代理类实例
        - Proxy.newInstance(classLoader, interfaces, invokeHandler)
![proxyClientClass](imagePool/proxyClientClass.png)
![proxyFactoryCreateProxyObjAtRuntime](imagePool/proxyFactoryCreateProxyObjAtRuntime.png)
![proxyTest](imagePool/proxyTest.png)
