---
title: Java 学习笔记（二）
date: 2016-08-21 17:31:33
tags:
---
今日的笔记内容是 Java 的标识符和面向对象编程中的一些基础概念。

<!-- more -->
标识符是程序中我们自己命名的一些名字，比如类名、变量名、方法名、方法参数名等等。关于标识符有几点要求：

- 所有的标识符开头都应该以字母（`A-Z` 或者 `a-z`）、美元符（`$`）、或者下划线（`_`）开始，注意不包括数字，首字母之后可以是任意字符或数字。
- Java 语言自带的关键字不能用作标识符。
- 标识符是大小写敏感的。
- 为了程序的可读性，一般情况下，类名以大写字母开头，比如上一节的入门程序中的类名 `Hello` 就以大写字母 `H` 开头；方法名一般以小写字母开头，比如 `main` 方法以小写字母 `m` 开头。如果名称中包含几个单词，从第二个单词开始每个单词首字母大写，类似 `printMyNote` 这样的。

下面以一个博客应用为例，来模拟面向对象编程里类和对象的关系。
``` java
public class Post{
	private String title;	//private是修饰符，表示属性不能被外部访问
	private String content;	//String是属性变量的数据类型

	public Post(String title, String content){
		this.title = title;
		this.content = content;
	}
	/**无返回值和参数的方法*/
	public void print(){	//public也是修饰符，表示外部可以访问这个方法
		System.out.println(this.title);
		System.out.println(this.content);
	}
	/**有返回值和参数的方法*/
	public int printWithAuthorName(String authorName){
		System.out.println(authorName);
		System.out.println(this.title);
		System.out.println(this.content);

		return this.content.length();	//返回一个整数，表示博客内容的长度
	}
}
```

接着可以在 `NewBlog` 类中，创建和使用 `Post` 对象

``` java
public class NewBlog{
	public static void main(String[] args){
		Post post = new Post("我的博客","这是我的第一篇博客");	//创建博客对象，参数传入博客的标题和内容
		int result = post.printWithAuthorName("LonelyCat");	//调用对象的方法
		System.out.println(result);	//打印返回值
	}
}
```

运行程序就可以看到下面的输出：

> LonelyCat
> 我的博客
> 这是我的第一篇博客
> 9
