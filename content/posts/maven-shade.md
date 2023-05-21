---
title: "Maven shade 打包不同版本依赖出现 ClassCastException 异常"
date: 2023-05-21T14:56:39Z
keywords: ["Maven"]

tags:
- Maven
- Java
categories:
- 技术

---

## 前言
先来说一下什么是 `ClassCastException` 异常
```markdown
ClassCastException 是一个 Java 异常，表示尝试将一个对象强制转换为不兼容的类型时发生了错误。这个错误通常发生在以下情况下：

1. 尝试将一个对象转换为它的子类，但实际上该对象不是该子类的实例。
2. 尝试将一个对象转换为与其不相关的类。
3. 尝试在继承层次结构中进行不兼容的类型转换。
通常，当你尝试将一个对象转换为一个不兼容的类型时，编译器不会报错，但在运行时会抛出 ClassCastException 异常。
```
然后再来说一下为什么会出现这个问题?  
当我们想在项目上使用不同版本的依赖，比如 `Jedis-2.4.1`和`Jedis-3.4.1`,在进行打包的时候如果不改变`Jedis`的路径，
会导致不同的版本互相引用冲突，所以会使用`Maven`打包工具所带的插件[Maven Shade Plugin](https://maven.apache.org/plugins/maven-shade-plugin/)
中的[Relocating Classes](https://maven.apache.org/plugins/maven-shade-plugin/examples/class-relocation.html)功能来重命名所打包的依赖包名。
但是如果你的代码出现了`函数式编程`相关代码，比如`Consumer`、`Function`等，如果你使用`2.4.X`版本的插件，函数式编程类将不会修改包名，
这也是为什么转型的时候出了问题，因为插件默认引用的是重命名前的包名。

### 解决办法
更新`Maven Shade Plugin`版本为最新即可！
