[toc]



# IDEA 好用的插件

## 插件安装方法

1. 打开设置对话框

![](https://raw.githubusercontent.com/HomanLiang/pictures/main/programming-summary/idea-plugin/image-20201215181326227.png)

2. 选中`Plugins`选项，并搜索对应的插件，再点击`Install`，最后重启IDEA完成安装

![](https://raw.githubusercontent.com/HomanLiang/pictures/main/programming-summary/idea-plugin/image-20201215181457657.png)



## Free Mybatis plugin

mybatis 插件，让你的mybatis.xml像java代码一样编辑。我们开发中使用mybatis时时长需要通过mapper接口查找对应的xml中的sql语句，该插件方便了我们的操作



## MyBatis Log Plugin

MyBatis Log Plugin 这款插件是直接将Mybatis执行的sql脚本显示出来，无需处理，可以直接复制出来执行的，如图：

![](https://raw.githubusercontent.com/HomanLiang/pictures/main/programming-summary/idea-plugin/Image_202012151743.png)

注：日志等级要求是 debug 级别



## Lombok

当我们创建一个实体时，通常对每个字段去生成GET/SET方法，但是万一后面需要增加或者减少字段时，又要重新的去生成GET/SET方法，非常麻烦。可以通过该插件，无需再写那么多冗余的get/set代码。



## Key promoter

Key promoter 是IntelliJ IDEA的快捷键提示插件，会统计你鼠标点击某个功能的次数，提示你应该用什么快捷键，帮助记忆快捷键，等熟悉了之后可以关闭掉这个插件



## Gsonformat

可根据json数据快速生成java实体类。自定义个javaBean(无任何内容，就一个空的类)，复制你要解析的Json，然后alt+insert弹出如下界面或者使用快捷键 Alt+S，在里面粘贴刚刚复制的Json，点击OK即可

![](https://raw.githubusercontent.com/HomanLiang/pictures/main/programming-summary/idea-plugin/Image_202012151746.png)



## Grep console

自定义日志颜色，idea控制台可以彩色显示各种级别的log，安装完成后，在console中右键就能打开

![Image [3]](https://raw.githubusercontent.com/HomanLiang/pictures/main/programming-summary/idea-plugin/Image_202012151747.png)

![Image [4]](https://raw.githubusercontent.com/HomanLiang/pictures/main/programming-summary/idea-plugin/Image_202012151749.png)



## Maven Helper

在插件安装好之后，我们打开pom.xml文件，在底部会多出一个Dependency Analyzer选项

![Image](https://raw.githubusercontent.com/HomanLiang/pictures/main/programming-summary/idea-plugin/Image_202012151750.png)

点开这个选项

![Image [2]](https://raw.githubusercontent.com/HomanLiang/pictures/main/programming-summary/idea-plugin/Image_202012151751.png)

找到冲突，点击右键，然后选择Exclude即可排除冲突版本的Jar包。



## Alibaba Java Coding Guidelines

阿里巴巴代码规范检查插件

使用方法：在你需要检查的代上面，点击右键，选择编码规约扫描

![Image](https://raw.githubusercontent.com/HomanLiang/pictures/main/programming-summary/idea-plugin/Image_20201215175201.png)

将会出现如下所示的检查结果，并会给出编码规范和提示：

![Image [2]](https://raw.githubusercontent.com/HomanLiang/pictures/main/programming-summary/idea-plugin/Image_20201215175202.png)



## Rainbow Brackets

可以实现配对括号相同颜色，并且实现选中区域代码高亮的功能

![Image](https://raw.githubusercontent.com/HomanLiang/pictures/main/programming-summary/idea-plugin/Image_20201215175301.png)

**区域代码高亮**：ctrl + 鼠标右键

![1583165-20200506083554372-1336846467](https://raw.githubusercontent.com/HomanLiang/pictures/main/programming-summary/idea-plugin/Image_20201215175402.gif)



**非选中部分暗淡效果**：alt + 鼠标右键

![1583165-20200506083557225-152030681](https://raw.githubusercontent.com/HomanLiang/pictures/main/programming-summary/idea-plugin/Image_20201215175501.gif)



## Presentation Assistant—快捷键展示

安装这个插件之后，你用键盘快捷键所做的操作都会被展示出来，非常适合自己在录制视频或者给别人展示代码的时候使用。比如我使用快捷键 command+9打开 Version Control ，使用了这个插件之后的效果如下图所示：

![640](https://raw.githubusercontent.com/HomanLiang/pictures/main/programming-summary/idea-plugin/Image_20201215175601.gif)



## Codota—代码智能提示

Codota 这个插件用于智能代码补全，它基于数百万Java程序，能够根据程序上下文提示补全代码。相比于IDEA自带的智能提示来说，Codota 的提示更加全面一些,如下图所示。

我们创建线程池现在变成下面这样：

![640 (1)](https://raw.githubusercontent.com/HomanLiang/pictures/main/programming-summary/idea-plugin/Image_20201215175801.gif)

上面只是为了演示这个插件的强大，实际上创建线程池不推荐使用这种方式， 推荐使用 ThreadPoolExecutor 构造函数创建线程池。我下面要介绍的一个阿里巴巴的插件-Alibaba Java Code Guidelines 就检测出来了这个问题，所以，Executors下面用波浪线标记了出来。

除了，在写代码的时候智能提示之外。你还可以直接选中代码然后搜索相关代码示例。

![Image](https://raw.githubusercontent.com/HomanLiang/pictures/main/programming-summary/idea-plugin/Image_20201215175802.png)

**从经过测试或证明过的程序中获得编码建议**

 如果我们觉得给出的提示不够清晰，可以使用快捷键： ctrl + shift + o ， 快速查询相关使用案例，同时可以通过添加关键字进行过滤，查找到更加精确的代码样例

![1583165-20200506083603411-2030861919](https://raw.githubusercontent.com/HomanLiang/pictures/main/programming-summary/idea-plugin/Image_20201215175904.gif)

**不脱离IDE发现并利用更多开源代码**

 当你不知道某个类如何使用时，可以直接使用快捷键：ctrl + shift + y ， 然后输入关键字，会查询到很多【开源框架】中使用该类的经典案例。不用脱离 IDE，没有广告，没有废话，只有经典的代码样例，你说爽不爽？

![1583165-20200506083609023-846614841](https://raw.githubusercontent.com/HomanLiang/pictures/main/programming-summary/idea-plugin/Image_20201215180005.gif)

Codota 还有一个在线网站，在这个网站上你可以根据代码关键字搜索相关代码示例，非常不错！我在工作中经常会用到，说实话确实给我带来了很大便利。网站地址：https://www.codota.com/code ，比如我们搜索 Files.readAllLines相关的代码，搜索出来的结果如下图所示：

![Image [2]](https://raw.githubusercontent.com/HomanLiang/pictures/main/programming-summary/idea-plugin/Image_20201215180007.png)

Codota 插件的基础功能都是免费的。你的代码也不会被泄露，这点你不用担心。



## RoboPOJOGenerator

```
File-> new -> Generate POJO from JSON
```

![Image](https://raw.githubusercontent.com/HomanLiang/pictures/main/programming-summary/idea-plugin/Image_20201215180201.png)

然后将JSON格式的数据粘贴进去之后，配置相关属性之后选择“Generate”

![Image [2]](https://raw.githubusercontent.com/HomanLiang/pictures/main/programming-summary/idea-plugin/Image_20201215180302.png)



## CodeGlance

英文直译【代码一瞥】，细心的朋友已经在开篇的图中看到了这个设置，安装该插件后，IDE右侧会出现一个mini 视图，比如看 ConcurrentHashMap 源码，那么长的内容，可以通过该插件快速的拖动到大概位置，方便很多

![Image](https://raw.githubusercontent.com/HomanLiang/pictures/main/programming-summary/idea-plugin/Image_20201215180401.png)



## CamelCase

编码离不开字符串的使用，安装该插件后，可以通过快捷键 shift + alt + U 快速的切换字符串格式，当然如果你只是单纯的切换大小写，使用 shift + cmd + U 更便捷一些

![1583165-20200506083621895-1504098966](https://raw.githubusercontent.com/HomanLiang/pictures/main/programming-summary/idea-plugin/Image_20201215180402.gif)

### 多行编辑

先来体验一下从xml文件拷贝字段新建实体对象

![1590194629508-870b695b-9f20-450b-ab2b-9f43fa08a556](https://raw.githubusercontent.com/HomanLiang/pictures/main/programming-summary/idea-plugin/Image_20201215180603.gif)

一般我们为了新建多表连接后映射的 ResultMap ，耗费不少时间，那么我们就来试一试这个多行编辑

表字段存在下划线，而实体中不允许，更是讨厌 ，等着一招教你解决

![1590195365159-ec4abcbb-d248-4885-9b06-9fa014e715e4](https://raw.githubusercontent.com/HomanLiang/pictures/main/programming-summary/idea-plugin/Image_20201215180605.gif)

前提条件，安装一个idea的插件，用来驼峰与下划线互转的：CamelCase

步骤：

1. 多行选择，按住ALT(windows)/option(Mac) ，拉动鼠标就可
2. 选中字段对象
   - Win Ctrl+shift+左箭头
   - Mac option+shift+左箭头
3. 复制，然后新建实体对象，右键选择 Paste without Formatting，也就是无格式粘贴
4. 然后下划线转驼峰对象，插件有快捷键
   - Win Shift + Alt + U
5. 选中多行，直接输入即是多行编辑，编辑完成后使用代码格式化即可



## Leetcode Editor

LeetCode插件，可以在IDEA中在线刷题。上班摸鱼属实方便，表面上我在干活，实际上我在刷算法题。

![Image](https://raw.githubusercontent.com/HomanLiang/pictures/main/programming-summary/idea-plugin/Image_20201215180901.png)



## RestfulToolkit

搜索URL，准确的说是搜索SpringMVC项目里，Controller层的@RequestMapping里的URL，通过URL匹配到相应的Controller层方法。

![Image [2]](https://raw.githubusercontent.com/HomanLiang/pictures/main/programming-summary/idea-plugin/Image_20201215181001.png)

使用：快捷键：Ctrl + \ 或Ctrl + Alt + N



## Jclasslib Bytecode Viewer

看类的字节码文件

![Image](https://raw.githubusercontent.com/HomanLiang/pictures/main/programming-summary/idea-plugin/Image_20201215181101.png)



## JProfiler

分析内存jvm内存



## SequenceDiagram

SequenceDiagram 插件可以根据代码调用链路自动生成时序图，这对梳理工作中的业务代码有很大的帮助，堪称神器，暴赞！
 TIP：双击顶部的类名可以跳转到对应类的源码中，双击调用的方法名可以直接跳入指定方法的源码中



## anyrule

正则表达式工具
快捷键是alt + a







