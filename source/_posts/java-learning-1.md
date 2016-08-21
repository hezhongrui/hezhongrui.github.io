---
title: Java 学习笔记（一）
date: 2016-08-20 20:27:10
tags:
---
![bamboo_cat](http://7xw3qx.com1.z0.glb.clouddn.com/16-8-21/16376256.jpg)
<div align = center>竹林里的猫</div>
最近由于工作的原因，要从头开始学习 Java 了，以后可能会在这里每天更新学习笔记，我相信这些笔记对于初学者会有点帮助。
<!-- more -->
Java 的 Hello World 入门程序

``` java
public class Hello{
	public static void main(String args []){
		System.out.println("Hello World!");
	}
} 
``` 

- JVM 是 Java Virtual Machine (Java 虚拟机)的缩写。
- JRE 是 Java Runtime Environment 的缩写，即 Java 运行环境。
- JDK 是 Java Development Kit 的缩写，即 Java 的软件开发工具集。
- Java 的源文件是以 `.java` 为后缀，编译出来的同名文件则是以 `.class` 为后缀。
- 环境变量 path 和 classpath 分别用于寻找 Java 命令程序和类文件的路径。
- Javac 命令行工具用于编译源程序，java 命令用于运行该程序，注意运行时不加后缀名。

在运行这个 Hello World 程序的时候，编译器报了一个错：
> `错误: 需要class, interface或enum`

但是我仔细检查这短短几行代码，没有发现任何问题。在网上搜索了一下，有人说可能是编辑器的问题，我自己使用的是 Sublime Text 2 ，于是把代码复制粘贴到 Vim 里，保存并重新运行，这次果然成功了。所以我觉得，对于语法要求严格的语言，最好还是用可靠的编译器，或者是用类似 Vim 这类久经考验的纯文本编辑器。

虽然现在才开始学 Java 有点晚了，有不少人认为 Java 技术已经是明日黄花，就像现在的 C++ 一样，但是我觉得，至少在看得见的未来，Java 应该还会是应用最广泛的编程语言之一。至于晚不晚，就像那句不知哪位哲人说的话：「种一颗树的最佳时机是十年以前，其次是现在」。而我们每一个人，其实真正拥有的永远都只有现在。
