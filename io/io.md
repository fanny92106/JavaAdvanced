# io


1. Definition

        - 用于处理设备之间的数据传输, eg: 读/写文件, 网络传输
        - 数据的输入/输出操作是以"流(stream)"的方式进行
        - 占位在内存角度判断in/out

2. Category

        - 按操作数据单位分为: 字节流 (8 bit), 字符流 (16 bit)
        - 按数据的流向分为: 输入流, 输出流
        - 按流的角色不同分为: 节点流, 处理流 
![StreamCategory](imagePool/StreamCategory.png)

       - 4个抽象基类: 
![4BasicStreamAbstractClass](imagePool/4BasicStreamAbstractClass.png)

       - 4个节点流:
            FileInputStream
            FileOutputStream
            FileReader
            FileWriter
            
       - io流的体系结构
![ioSystem](imagePool/ioSystem.png)
