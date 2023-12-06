# Java

## 一.JDK  开发工具包

1.

2014 -JDK-8 LTS（长期支持版）

2018 -JDK-11 LTS（长期支持版）

2021 -JDK-17 LTS（长期支持版）

2.

JavaSE（Java Standard Edition）是Java平台的标准版，它提供了Java语言的核心功能和基本库。JavaSE包含了Java编程语言、Java虚拟机（JVM）、Java类库等基本组件，可以用于开发桌面应用程序、命令行工具和一些简单的服务器应用。JavaSE提供了面向对象的编程模型、异常处理、多线程、网络编程、输入输出等基本功能，是Java开发的基础。

JavaEE（Java Enterprise Edition）是Java平台的企业版，它是在JavaSE的基础上扩展而来，专注于开发大型、分布式、可扩展的企业级应用。JavaEE提供了一系列的API和规范，用于开发企业级应用，包括Web应用、企业级JavaBean（EJB）、消息中间件、事务处理、持久化等。JavaEE还提供了一些高级特性，如分布式计算、集群、负载均衡等，以满足企业级应用的需求。



2.java.exe\javac.exe

java.exe 执行工具

javac.exe 编译工具



常用窗口命令：

D：  (要切盘才能进行目录操作)      dir 当前目录           cd 进入目录     cd ..         cd \

cls   清屏



编写代码( xxx.java)----使用javac编译（生成字节码原件 xxx.class）-----使用java运行



Java的组成和跨平台：

1.JVM：java虚拟机，真正运行java的地方

2.核心类库： java自己写好的程序

1+2=**JRE ：java运行环境**

**开发工具（java+javac 开发环境）**+JRE=JDK



java的跨平台、工作原理

**一次编译，处处可用**!!!!

在各个系统安装jvm虚拟机，开发一次后可在各个系统运行。



path环境变量用于记住程序路径，方便在命令行窗口任意目录启动程序

JAVA_HOME告诉操作系统JDK安装在哪个位置，方便其他技术通过环境变量找到JDK



企业开发使用集成开发环境（IDE）：把编写，编译，执行多种功能综合到一起。

Eclipse、lntelliJ IDEA



结构

*project（项目工程）

*module（模块）

*package（包）

*class（类）



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