# Java

## 一.JDK  开发工具包

### 1.JDK、javaSE、javaEE

2014 -JDK-8 LTS（长期支持版）

2018 -JDK-11 LTS（长期支持版）

2021 -JDK-17 LTS（长期支持版）

2.

JavaSE（Java Standard Edition）是**Java平台的标准版**，它提供了Java语言的核心功能和基本库。JavaSE包含了Java编程语言、Java虚拟机（JVM）、Java类库等基本组件，可以用于开发桌面应用程序、命令行工具和一些简单的服务器应用。JavaSE提供了面向对象的编程模型、异常处理、多线程、网络编程、输入输出等基本功能，是Java开发的基础。

JavaEE（Java Enterprise Edition）是**Java平台的企业版**，它是在JavaSE的基础上扩展而来，专注于开发大型、分布式、可扩展的企业级应用。JavaEE提供了一系列的API和规范，用于开发企业级应用，包括Web应用、企业级JavaBean（EJB）、消息中间件、事务处理、持久化等。JavaEE还提供了一些高级特性，如分布式计算、集群、负载均衡等，以满足企业级应用的需求。



### 2.java.exe\javac.exe

java.exe 执行工具

javac.exe 编译工具



常用窗口命令：

D：  (要切盘才能进行目录操作)      dir 当前目录           cd 进入目录     cd ..         cd \

cls   清屏



编写代码( xxx.java)----使用javac编译（生成字节码原件 xxx.class）-----使用java运行（java xxxx）



### 3.Java的组成和跨平台：

1.JVM：java虚拟机，真正运行java的地方

2.核心类库： java自己写好的程序

1+2=**JRE ：java运行环境**

**开发工具（java+javac 开发环境）**+JRE=JDK



java的跨平台、工作原理

**一次编译，处处可用**!!!!

在各个系统安装jvm虚拟机，开发一次后可在各个系统运行。



path环境变量用于记住程序路径，**方便在命令行窗口任意目录启动程序**

JAVA_HOME告诉操作系统JDK安装在哪个位置，方便其他技术通过环境变量找到JDK。



企业开发使用集成开发环境（IDE）：把编写，编译，执行多种功能综合到一起。

Eclipse、lntelliJ IDEA



结构

*project（项目工程）

*module（模块）

*package（包）

*class（类）



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

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



github 令牌：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

github SSH密钥（ed25519）生成：

![image-20231207012149232](D:\Typora_picture\image-20231207012149232.png)

### 4.IDEA工程结构化管理项目

中其他操作

删除类文件、修改类名称；

修改类模块；导入类模块；删除模块

打开工程、关闭工程

快捷键：ctrl+d   复制本行到下一行

​               ctrl+x    删除



## 二.入门

1.注释

单行注释：//

多行注释： /*  +  回车       /*    */

文档注释：/**    */

编译后的.class文件中无注释



**字面量**就是告诉程序员：数据在程序中的书写格式。

字符：' A' 

字符串： “abc”

布尔值：true、false

空值： null

\n   \t代表一个tab



**变量：**   

数据类型 变量名称 = 数据；

变量声明才能使用！！！

变量在一个大括号内生效。



**关键字：**

public、class、int、double

合法标识符：数字、字母、下划线 组成；不能以数字开头；

变量里的数据在计算机中的存储原理

最小单元：字节1Byte(8位一组)  1B=8b



ASCII： "0"->48 ,    ‘A’->65 ,   'a'->97

八进制和十六进制是为了更好地表示二进制

八进制：二进制每三位为一个单元

十六进制：二进制每四位为一个单元



基本数据类型：

byte 1                           float 4        float b =3.14F                    char   2

short 2                          double 8                                                boolean   1

int 4

long 8   long a = 20L



**引用数据类型**：string、数组



自动类型转换： 类型范围小的变量可以直接赋值给类型范围大的

​                           byte a = 1;

​                           int   b = a;

**表达式的最终结果类型由表达式中的最高类型决定的**

**在表达式中，byte、short、char是直接转换成int类型参与运算的**



强制类型转换：

类型范围大的变量不可以直接赋值给类型范围大的

数据类型 a = (数据类型) b

浮点数转整数直接舍弃小数部分。



运算符：两个整数相除还是整数（舍弃小数部分）

int a =5  int b=2   **System.out.println(1.0*a / b)**  转换成double类型



“+”做连接符：能算则算，不能算则连接



扩展运算符：**中间自带强制类型转换！！！**

a+=b   ------->  a=(a类型)a +b;



&与&&、|与|| 用法效果一样，逻辑一致；

但是&&、||效率更高，算一半不满足直接退出，不算剩下一半。



三元运算符： （类型） a = 表达式？ 真：假；



import java.util.Scanner



条件为区间使用  if分支结构

 条件为区间使用switch

   **switch 穿透性**：**匹配到对应case,没有break时，后续不用匹配case继续执行直到break。** 减少代码  可以多个case执行内容重复，利用穿透性

   case不能为变量，只能为字面量



循环

知道循环几次：使用for

不知道循环几次：使用while

for循环控制循环的变量只在循环中使用，while不行

写死循环用while写（不知道次数）  eg服务器程序

import java.util.Random



**数组：**

数组变量名中存储的是数组在内存中的地址

静态数组：数据类型[] 数组名称 = new 数据类型[]{}

动态数组：数据类型[] 数组名称 = new 数据类型[n]    （int默认为0 ，double默认为0.0,string默认null，bool默认false）





数组内存分配：

![image-20240109010344515](D:\Typora_picture\image-20240109010344515.png)



![image-20240109010459167](D:\Typora_picture\image-20240109010459167.png)





数组变量存储的null,表示数组变量没有指向数组对象，可以输出这个变量（null），但是不能通过数组变量去访问数据或者数组长度。



字符串、数组属于引用数据类型。

引用数据类型指的是类（class）、接口（interface）、数组（［］）

1,基本数据类型:被创建时,在栈内存中会被划分出一定的内存,并将数值存储在该内存中.

2,引用数据类型:被创建时,首先会在栈内存中分配一块空间,然后在堆内存中也会分配一块具体的空间用来存储数据的具体信息,即hash值,然后由栈中引用指向堆中的对象地址.



**方法：**

基本类型的参数传递存储的数据值；

引用类型的参数传输存储的地址值；

**方法重载：**

一个类中：出现多个**方法的名称相同**，但是他们的**形参列表是不同的**，那么它们就是方法重载了。

形参列表是不同：个数、类型、顺序不同，不关心形参的名称。



return可以用在无返回值的方法中，作用：立即跳出并结束当前方法的执行。



**循环外部指定标签：**

![image-20240115003037904](D:\Typora_picture\image-20240115003037904.png)

OUT标签------循环推出指定循环



**对象：**

类型 名 = new 数据名();

变量+方法



成员变量有初始值：int默认为0 ，double默认为0.0,string默认null，bool默认false



执行原理：

![image-20240116012753924](D:\Typora_picture\image-20240116012753924.png)



tips：

1.一个代码文件中可以写多个class类，但是只能用一个public修饰（且public修饰的类名必须成为代码文件名）

2.java存在自动垃圾回收机制，会自动清楚掉垃圾对象（没有被任何变量引用）





**this**关键字：

1.this就是一个变量，可以用在**方法**中，一般用来拿到当前方法对象的属性。

2.主要解决变量冲突问题（局部变量和成员变量名冲突）



构造器（本质是一个特殊方法）

1.类似C++构造函数

2.特点：创建对象时，对象会自动调用构造器。

3.应用场景：创建对象时，进行初始化赋值



tips：

1.如果不写,JAVA会自动生成无参构造器。

2.如果定义了有参构造器，java不会自动写无参构造函数，建议自己写。



封装：

合理隐藏、合理暴露（变量隐藏、写出set、get方法访问）



实体JavaBean(实体类)：只保存数据的java类。

1.成员变量必须私有，为它们提供set、get方法访问，必须有无参构造器

2.数据和业务分离



![image-20240119010819861](D:\Typora_picture\image-20240119010819861.png)



## 三.JAVA常用API



API文档

java.lang：String

java.util:     ArrayList



### 1.包：

管理不同程序，类似于文件夹，建包有利于维护和管理。



tips:

1.同一个包下，可以直接访问其他方法。

2.访问其他包下的程序，必须导包。

3.java.lang包不需要导入（java.util需要）

4.方法名一样，另外一个要带包名



### 2.String常用方法

![image-20240122002041945](D:\Typora_picture\image-20240122002041945.png)

tips:

1.string对象内容不可改变（改变则产生新的字符串常量，指向不同地址）

2.以“ ” 方式写的对象，会被存储到字符串常量池（堆内存），同样的字符串指向同一个地址（同python字符串驻留机制，在编译阶段驻留，也就是包含运算的结果，不包含变量调用）

3.以New方式写的对象，产生新的对象在堆内存中。

**主要目的是节约内存！！！**



### 3.ArrayList 

![image-20240122002333577](D:\Typora_picture\image-20240122002333577.png)

1.集合大小可变，类型可变，泛型类

ArrayList<string> list = new ArrayList<>

希望集合内的数据类型是固定的。



tips：

1.所有存放数据的容器基本操作都是**增删改查**

2.遍历删除元素会漏删除问题： ①i-- ②采用后续遍历



### 4.简单实战(ATM项目)



