# KeiSystem-Java

[KeiSystem](https://github.com/GridScience/KeiSystem/) 的 Java 实现，为将来的应用做准备。

## 状态

由于资源申请获得了通过，不需要分布式 tracker 网络，KeiSystem 暂停开发。此前的计划：将协议修改为基于 HTTP 的请求/请求-响应（因此不需要写底层 TCP 连接）；使用 Apache HttpComponents 替换正在用的 Sun HTTP API。

已完成的部分:

- Tracker 服务器（有少量潜在的bug，见注释）

## 编译

该项目使用依赖库：

- JDK 8
- Apache MINA (2.0.9)

由于该项目使用 IntelliJ IDEA 开发，而且选用了编译 GUI 选项，因此暂时需要 IDEA 的 javac2 支持。以后可能会改变这些限制。

添加 `build.properties`，输入以下内容：

```
path.variable.maven_repository={你的用户 Maven 目录（.m2）}/repository
jdk.home.1.8={你的 JDK 1.8 的目录}
javac2.instrumentation.includeJavaRuntime=false
idea.home=(你的 IntelliJ IDEA 目录}
```

注意最好还是使用斜杠`/`以实现跨平台的支持。

然后使用 ANT 加载 build.xml 进行组建。

## 致谢

使用 Dmytro Chyzhykov 的 [bencode](https://github.com/ffbit/bencode) 作为 B-编码流的编解码库。相当不错的工具。
