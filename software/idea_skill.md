[toc]



# IDEA 常用技巧

## 1.常用配置

### 1.1.用*标识编辑过的文件 
1. `Editor–>General –> Editor Tabs`
2. 在IDEA中，你需要做以下设置, 这样被修改的文件会以*号标识出来，你可以及时保存相关的文件
3. Mark modifyied tabs with asterisk

### 1.2.显示行号
`File -> Settings ->Editor ->General -> Appearance =>Show line numbers选中`

### 1.3.修改为Eclipse快捷键
`File -> Settings -> Keymap => Keymaps改为 Eclipse copy`

### 1.4.设置maven
1. 在File->settings->搜索maven
2. Mavan home directory--设置maven安装包的bin文件夹所在的位置
3. User settings file--设置setting文件所在的位置
4. Local repository--设置本地仓库

### 1.5.默认设置（Other Settings）
IDEA不像Eclipse那样可以在一个窗口中打开多个项目，IDEA每次打开一个新的项目都需要开一个新的窗口或者覆盖掉当前窗口，所以在打开多个项目的时候就需要开多个窗口，但是如果不设置好默认设置，每次打开一个新的窗口就要重新设置。例如：每次打开新的项目的时候maven的本地仓库地址都要重新设置。通过设置Other Settings就可以解决这类问题。File-->Other Settings-->Preferences for New Projects。然后在左上角的搜索框中搜maven，就能看到如下图所示配置了

![Image](https://homan-blog.oss-cn-beijing.aliyuncs.com/programming-summary/idea_skill/20210427211052.png)

配置默认打开的项目的JDK也和这个类似，`File-->Other Settings-->Structure for New Projects`。然后就可以看到项目配置（Project Settings）和平台配置(Platform Settings)了

![Image [2]](https://homan-blog.oss-cn-beijing.aliyuncs.com/programming-summary/idea_skill/20210427211105.png)

### 1.6.自动编译开关
在IDEA当中自动编译是需要手动打开的，`File-->settings-->Build,Execution,Deployment-->Compiler`，然后将下图红框处勾上

![Image [3]](https://homan-blog.oss-cn-beijing.aliyuncs.com/programming-summary/idea_skill/20210427211116.png)

### 1.7.自动引包
DEA默认是没有开启自动引包功能的。需要手动打开，位置在：`File-->Settings-->Editor-->General-->Auto Import`。然后在下图的1和2的位置上进行勾选。勾选上1的位置后，IDEA 将在我们书写代码的时候自动帮我们优化引入的包，比如自动去掉一些没有用到的包。勾选上2的位置后，IDEA 将在我们书写代码的时候自动帮我们导入需要用到的包。但是对于那些同名的包，还是需要手动 Alt + Enter 进行导入的，IntelliJ IDEA 目前还无法智能到替我们做判断

![Image [4]](https://homan-blog.oss-cn-beijing.aliyuncs.com/programming-summary/idea_skill/20210427211124.png)

### 1.8.内存使用量展示
由于日常开发时都是在公司的办公电脑上进行的，所以内存总是不够用，但是又不清楚IDEA具体实时的占用了多少内存。这个时候对于一些内存并不是太够的开发人员来说能看到实时的内存使用量还是比较好的。IDEA是提供这项功能的，但是需要手动的打开。具体位置在：`File-->Settings-->Apperance-->Window Options-->Show Memory indicator`

![Image [5]](https://homan-blog.oss-cn-beijing.aliyuncs.com/programming-summary/idea_skill/20210427211135.png)

### 1.9.悬浮提示
有时候在看代码的时候，不清楚一个类具体是干什么的，就会点进去看这个类的注释，但是强大的IDEA是支持不用点进去就可以看到注释的以及类的相关信息的。但是需要手动打开。具体位置在：`File-->Settings-->Editor-->General`。然后在下图所示的位置上进行勾选，后面的时间是悬浮提示的显示时间

![Image [6]](https://homan-blog.oss-cn-beijing.aliyuncs.com/study-demo/project-manage/20210427210827.png)

### 1.10.Ctrl+鼠标滚轴修改字体大小
IDEA也支持向浏览器那样按住Ctrl+鼠标滚轴来改变编辑区的字体的大小，设置的开关在：`File-->Settings-->Editor-->General`

![Image [7]](https://homan-blog.oss-cn-beijing.aliyuncs.com/programming-summary/idea_skill/20210427211149.png)

### 1.11.显示多行Tab
当我们打开的标签页多了的时候，默认的会隐藏在右侧，当我们需要的时候在右侧找到后再打开。IDEA是支持多行显示的，这样在大屏幕的显示器上也不用总去点击右侧的去找刚才打开过的文件了（其实通过Ctril+E也可以找到刚才打开过的文件）。具体开关位置在：`File-->Settings-->Editor-->General-->Editor Tabs`

![Image [8]](https://homan-blog.oss-cn-beijing.aliyuncs.com/programming-summary/idea_skill/20210427211159.png)

### 1.12.显示行号，显示svn/git最近提交人
在编辑区直接操作，能看到每一行代码的最近一次修改人，以及提交记录信息。这样每行代码都有记录。能很快定位到谁动过代码，然后找到指定的人来解决问题

![772743-20181225233620846-929596446](https://homan-blog.oss-cn-beijing.aliyuncs.com/programming-summary/idea_skill/20210427211210.gif)

### 1.13.IntelliJ换行CRLF, LF, CR的解释和默认设置
在window下开发有一个大坑，就是换行默认是CRLF，也就是回车换行，但是Linux下只有换行LF，这样代码提交后，会出现编译问题，所以最好的办法是在IntelliJ下设置默认为LF。首先我们先介绍CRLF，LF和CR这三种东西，CR是MAC老版本的做法，就是回车，但是后来的MAC系统统一换成LF了，LF是Linux下的做法，就是换行，这个做法比较自然，为什么要回车换行呢，是吧。微软采用的是CRLF，看上去好像是兼容了CR和LF，但是实际完全不是那么回事，就是回车并换行，好鸡肋啊，微软一直保持这种做法，开发人员大多在Linux下，所以对于开发人员来说还是比较坑的。下面介绍设置详解：
第一步：`File->Settings…`

![Image [9]](https://homan-blog.oss-cn-beijing.aliyuncs.com/programming-summary/idea_skill/20210427211219.png)

第二步：`Editor->Code Style`
可以看到，默认是System-Dependent，这个其实还是很牛叉的，根据系统自动配置，但是你是windows系统，默认是CRLF，服务器是Linux，你就得自己换了。

![Image [10]](https://homan-blog.oss-cn-beijing.aliyuncs.com/programming-summary/idea_skill/20210427211233.png)

我们设置成下面这样，保存就好了

![Image [11]](https://homan-blog.oss-cn-beijing.aliyuncs.com/programming-summary/idea_skill/20210427211244.png)

创建文件时，就能看到默认是LF了

![Image [12]](https://homan-blog.oss-cn-beijing.aliyuncs.com/programming-summary/idea_skill/20210427211254.png)

### 1.14.类注释模板
- `File–Setting–Editor–File and Code Templates–Class`
- 注释模板：

    ```
    /**
     *
     *
     *@description: 
     *@author: Homan Liang
     *@time: ${DATE} ${TIME}
     * 
     */
    ```

![Image [13]](https://homan-blog.oss-cn-beijing.aliyuncs.com/programming-summary/idea_skill/20210427211322.png)

### 1.15.Postfix Completion配置

`Postfix Completion`其实就是关于代码补全的一些模板。我们可以在`Settings`—>`Editor`—>`General`—`Postfix Completion`中看到它的一些模板。下面我们一起看看常用的一些语法。

![图片](https://homan-blog.oss-cn-beijing.aliyuncs.com/programming-summary/idea_skill/20210427215604.png)

#### 1.15.1.if 相关 

定义一个`boolean`类型的变量`flag`和一个`String`类型的变量`name`来进行测试。

```
boolean flag = true;
String name = "Java旅途";
```

1. 判断条件成立。

   语法：

    ```
    flag.if
    ```

	效果：

    ```
    if (flag) {}
    ```

1. 判断条件不成立。

	语法：

    ```
    flag.else
    ```

	效果：

    ```
    if (!flag) {}
    ```

1. 判断条件等于 null。

	语法：

    ```
    string.null
    ```

	效果：

    ```
    if (string == null) {}
    ```

1. 判断条件不等于 null。

	语法：

    ```
    string.notnull 或者 string.nn
    ```

	效果：

    ```
    if (string != null) {}
    ```

1. 使用 switch 判断。

	语法：

    ```
    string.switch
    ```

	效果：

    ```
    switch (string) {}
    ```

1. 使用 while 判断。

	语法：

    ```
    flag.while
    ```

	效果：

    ```
    while (flag) {}
    ```

#### 1.15.2.for 相关

定义一个`String`类型的数组来测试。

```
String[] param = {"1","2","3"};
```

1. 从第一个元素进行遍历。

	语法：

    ```
    param.fori
    ```

	效果：

    ```
    for (int i = 0; i < param.length; i++) {}
    ```

1. 从最后一个元素进行遍历。

	语法：

    ```
    param.forr
    ```

	效果：

    ```
    for (int i = param.length - 1; i >= 0; i--) {}
    ```

1. 增强 for 循环。

	语法：

    ```
    param.for 或者 param.iter
    ```

	效果：

    ```
    for (String s : param) {}
    ```

#### 1.15.3.变量相关

新定义一个`User`类，添加`name`和`age`两个属性用来测试。

```
public class User {
    
    private String name = "Java旅途";
    private int age = 18;
    
    public User() {}

    public User(String name, int age) {
        this.name = name;
        this.age = age;
    }
}
```

1. 创建一个对象。

	语法：

    ```
    User.new
    ```

	效果：

    ```
    new User();
    ```

1. 创建一个局部变量。

	语法：

    ```
    new User().var
    ```

	效果：

    ```
    User user = new User();
    ```

1. 创建一个全局变量。

	语法：

    ```
    new User().field
    ```

	效果：

    ```
    private User user;
    user = new User();
    ```

1. 强制转换对象类型，假如我们将 Object 转换为 User。

	语法：

    ```
    new object.castvar
    ```

	效果：

    ```
    User user = (User) new Object();
    ```

#### 1.15.4.其他常用

1. 返回语句。

	语法：

    ```
    "".return
    ```

	效果：

    ```
    return "";
    ```

1. 打印语句。

	语法：

    ```
    flag.sout
    ```

	效果：

    ```
    System.out.println(flag);
    ```

1. 捕获处理异常。

	语法：

    ```
    new User().try
    ```

	效果：

    ```
    try {
        new User();
    } catch (Exception e) {
        e.printStackTrace();
    }
    ```

1. 抛出异常。

	语法：

    ```
    new Exception().throw
    ```

	效果：

    ```
    throw new Exception();
    ```

1. 给变量加锁。

	语法：

    ```
    string.synchronized
    ```

	效果：

    ```
    synchronized (string) {}
    ```

### 1.16.避免IDEA自动导入“*”的问题

避免IDEA自动导入“*”的问题

编译器操作：

左上角 `File->settings->Editor->Code Style->java->imports`

设置  `Class count to use import with '*'`  值为 `500`

设置 `Names count to use static import with '*'` 值为 `300`

![img](https://homan-blog.oss-cn-beijing.aliyuncs.com/programming-summary/idea_skill/20210623205448.png)



## 2.快捷键
### 2.1.编辑类快捷键
| 快捷键                                                       | 说明                                             |
| ------------------------------------------------------------ | ------------------------------------------------ |
| sout + Tab                                                   | 快速打印输出                                     |
| psvm + Tab                                                   | 生成main方法                                     |
| 在字符串或者数字……后面输入 .var，然后回车                    | 快速定义局部变量                                 |
| 在值后面输入.field                                           | 快速定义成员变量                                 |
| 在字符串后面输入.format，回车                                | 快速格式化字符串                                 |
| 非空：.notnull 或者 .nn，空：.null                           | 快速判断（非）空                                 |
| 输入 .not 可以让布尔值快速取反，再输入 .if 可快速生成 if 判断语句块 | 快速取反判断                                     |
| .for, .fori, .forrl                                          | 快速遍历集合                                     |
| 在对象后面输入.synchronized                                  | 快速生成同步锁                                   |
| 非空：.notnull 或者 .nn，空：.null                           | 快速判断（非）空                                 |
| 非空：.notnull 或者 .nn，空：.null                           | 快速判断（非）空                                 |
| Ctrl+Alt+O                                                   | 优化导入的类和包                                 |
| Alt+Insert                                                   | 生成代码(如get,set方法,构造函数等)               |
| Ctrl+Alt+T                                                   | 把选中的代码放在 TRY{} IF{} ELSE{} 里            |
| Ctrl + O                                                     | 重写方法                                         |
| Ctrl + I                                                     | 实现方法                                         |
| Ctr+shift+U                                                  | 大小写转化                                       |
| ALT+回车                                                     | 导入包,自动修正                                  |
| ALT+/ ，CTRL+空格                                            | 代码提示                                         |
| CTRL+J                                                       | 自动代码                                         |
| Ctrl+Shift+J                                                 | 整合两行为一行                                   |
| CTRL+SHIFT+SPACE                                             | 自动补全代码                                     |
| CTRL+ALT+L                                                   | 格式化代码                                       |
| Shift+F6                                                     | 重构-重命名 (包、类、方法、变量、甚至注释等)     |
| CTRL+P                                                       | 方法参数提示                                     |
| Ctrl+Alt+V                                                   | 提取变量                                         |
| Ctrl＋Shift＋Backspace                                       | 跳转到上次编辑的地                               |
| CTRL+ALT+ left/right                                         | 前后导航编辑过的地方                             |
| ALT+7                                                        | 靠左窗口显示当前文件的结构                       |
| Ctrl+F12                                                     | 浮动显示当前文件的结构                           |
| ALT+F7                                                       | 找到你的函数或者变量或者类的所有引用到的地方     |
| CTRL+ALT+F7                                                  | 浮动找到你的函数或者变量或者类的所有引用到的地方 |
| CTRL+E                                                       | 最近打开的文件                                   |
| F2 或Shift+F2                                                | 高亮错误或警告快速定位                           |
| Ctrl+X                                                       | 删除行                                           |
| Ctrl+D                                                       | 复制行                                           |
| Ctrl+H                                                       | 显示类结构图                                     |
| Ctrl+Shift+Alt+T                                             | 重构一切                                         |
### 2.2.查找、替换类快捷键
| 快捷键                 | 说明                                                         |
| ---------------------- | ------------------------------------------------------------ |
| 双击SHIFT              | 在项目的所有目录查找文件                                     |
| Ctrl+N                 | 查找类                                                       |
| Ctrl+Shift+N           | 查找文件                                                     |
| Ctrl + F               | 在当前文件中查找                                             |
| Ctrl + Shift + F       | 在整个项目或者指定窗口中查找文本                             |
| Ctrl + R               | 在当前文件进行文本替换                                       |
| Ctrl + Shift+R         | 在指定窗口替换文本                                           |
| Ctrl + W               | 自动按语法选中代码                                           |
| Ctrl + Shift + W       | 反向自动按语法选中代码                                       |
| Ctrl + G               | 定位行                                                       |
| Ctrl＋Shift＋Backspace | 跳转到上一次编辑的位置                                       |
| Ctrl + alt + ←/→       | 前后跳转编辑过的地方                                         |
| Ctrl + Shift + Alt + N | 查找 变量 / 方法                                             |
| Alt + F7               | 找到你的函数或者变量或者类的所有引用到的地方                 |
| Alt + F3               | 高亮显示所有该选中文本，按 Enter 选中下一个，按 Esc 高亮消失 |
| F4                     | 在当前类中查找变量的来源                                     |
| Ctrl + Shift + F7      | 高亮显示所有该选中文本，按 Esc 高亮消失                      |
### 2.3.编译、运行类快捷键
| 快捷键            | 说明                  |
| ----------------- | --------------------- |
| Ctrl + F9         | 编译项目              |
| Ctrl + Shift + F9 | 编译当前文件          |
| Shift + F10       | 正常启动              |
| Alt + Shift + F10 | 弹出 Run 的可选择菜单 |
| Shift + F9        | debug模式启动         |
| Alt + Shift + F9  | 选择 Debug            |
### 2.4.Debug快捷键
| 快捷键        | 说明              |
| ------------- | ----------------- |
| alt+F8        | debug时选中查看值 |
| Alt+Shift+F9  | 选择 Debug        |
| Alt+Shift+F10 | 选择 Run          |
| Ctrl+Shift+F9 | 编译              |
| Ctrl+Shift+F8 | 查看断点          |
| F7            | 步入              |
| Shift+F7      | 智能步入          |
| Alt+Shift+F7  | 强制步入          |
| F8            | 步过              |
| Shift+F8      | 步出              |
| Alt+Shift+F8  | 强制步过          |
| Alt+F9        | 运行至光标处      |
| Ctrl+Alt+F9   | 强制运行至光标处  |
| F9            | 恢复程序          |
| Alt+F10       | 定位到断点        |
### 2.5.重构快捷键
| 快捷键         | 说明     |
| -------------- | -------- |
| Shift + F6     | 重命名   |
| Ctrl + Alt + C | 抽取常量 |
| Ctrl + Alt + F | 抽取字段 |
| Ctrl + Alt + M | 抽取方法 |
| Ctrl + Alt + P | 抽取参数 |
| Ctrl + Alt + V | 抽取变量 |
### 2.6.其他类快捷键
| 快捷键             | 说明                                                         |
| ------------------ | ------------------------------------------------------------ |
| Ctrl + C           | 复制文件名                                                   |
| Ctrl + Shift + C   | 复制文件的完整路径                                           |
| Ctrl + E           | 显示最近打开的文件                                           |
| Ctrl + Shift + E   | 显示最近修改的文件列表的弹出层                               |
| Ctrl + P           | 方法参数提示                                                 |
| Ctrl + Q           | 可以看到当前方法的声明                                       |
| Ctrl + Alt + Space | 类名或接口名提示                                             |
| Ctrl + F12         | 显示当前文件的结构                                           |
| Ctrl + H           | 显示当前类的结构图                                           |
| Ctrl + Q           | 显示注释文档信息                                             |
| Ctrl + [           | 移动光标到当前所在代码的花括号开始位置                       |
| Ctrl + ]           | 移动光标到当前所在代码的花括号结束位置                       |
| Ctrl + K           | 版本控制提交项目，需要此项目有加入到版本控制才能够使用       |
| Ctrl + T           | 版本控制更新项目，需要此项目有加入到版本控制才能够使用       |
| Ctrl + Tab         | 切换编辑窗口。如果在切换的过程又按Delete键，则是关闭对应选中的窗口 |

## 3.调试技巧
### 3.1.条件断点
循环中经常用到这个技巧，比如：遍历1个大List的过程中，想让断点停在某个特定值。

![Image [14]](https://homan-blog.oss-cn-beijing.aliyuncs.com/programming-summary/idea_skill/20210427211343.png)

参考上图，在断点的位置，右击断点旁边的小红点，会出来一个界面，在Condition这里填入断点条件即可，这样调试时，就会自动停在i=10的位置

![](https://homan-blog.oss-cn-beijing.aliyuncs.com/programming-summary/idea_skill/20210427211357.png)

### 3.2.回到"上一步" 
该技巧最适合特别复杂的方法套方法的场景，好不容易跑起来，一不小心手一抖，断点过去了，想回过头看看刚才的变量值，如果不知道该技巧，只能再跑一遍。

![Image [16]](https://homan-blog.oss-cn-beijing.aliyuncs.com/programming-summary/idea_skill/20210427211406.png)

参考上图，method1方法调用method2，当前断点的位置j=100，点击上图红色箭头位置的Drop Frame图标后，时间穿越了

![Image [17]](https://homan-blog.oss-cn-beijing.aliyuncs.com/programming-summary/idea_skill/20210427211413.png)

回到了method1刚开始调用的时候，变量i变成了99

注：好奇心是人类进步的阶梯，如果想知道为啥这个功能叫Drop Frame，而不是类似Back To Previous 之类的，可以去翻翻JVM的书，JVM内部以栈帧为单位保存线程的运行状态，drop frame即扔掉当前运行的栈帧，这样当前“指针”的位置，就自然到了上一帧的位置。

### 3.3.多线程调试
多线程同时运行时，谁先执行，谁后执行，完全是看CPU心情的，无法控制先后，运行时可能没什么问题，但是调试时就比较麻烦了，最明显的就是断点乱跳，一会儿停这个线程，一会儿停在另一个线程，比如下图：

![Image [18]](https://homan-blog.oss-cn-beijing.aliyuncs.com/programming-summary/idea_skill/20210427211422.png)

如果想希望下一个断点位置是第2句诗句，可能要失望了：

![Image [19]](https://homan-blog.oss-cn-beijing.aliyuncs.com/programming-summary/idea_skill/20210427211433.png)

如果想让线程在调试时，想按自己的愿意来，让它停在哪个线程就停在哪个线程，可以在图中3个断点的小红点上右击，

![Image [20]](https://homan-blog.oss-cn-beijing.aliyuncs.com/programming-summary/idea_skill/20210427211439.png)

即：Suspend挂起的条件是按每个线程来，而非All。把这3个断点都这么设置后，再来一发试试

![Image [21]](https://homan-blog.oss-cn-beijing.aliyuncs.com/programming-summary/idea_skill/20210427211450.png)

注意上图中的红框位置，断点停下来时，这个下拉框可以看到各个线程（注：给线程起个容易识别的名字是个好习惯！），我们可以选择线程“天空中的飞鸟”

![Image [22]](https://homan-blog.oss-cn-beijing.aliyuncs.com/programming-summary/idea_skill/20210427211505.png)

断点如愿停在了第2句诗。

### 3.4.远程调试
这也是一个装B的利器，本机不用启动项目，只要有源代码，可以在本机直接远程调试服务器上的代码，打开姿势如下：
1. 项目启动时，先允许远程调试

    ```
    java -server -Xms512m -Xmx512m -Xdebug -Xnoagent -Djava.compiler=NONE -Xrunjdwp:transport=dt_socket,server=y,suspend=n,address=9081 -Djava.ext.dirs=. ${main_class}
    ```

	起作用的就是

    ```
    -Xdebug -Xnoagent -Djava.compiler=NONE -Xrunjdwp:transport=dt_socket,server=y,suspend=n,address=9081
    ```

	注意：远程调试从技术上讲，就是在本机与远程建立scoket通讯，所以端口不要冲突，而且本机要允许访问远程端口，另外这一段参数，放要在-jar 或 ${main_class}的前面

2. idea中设置远程调试

    ![Image [23]](https://homan-blog.oss-cn-beijing.aliyuncs.com/programming-summary/idea_skill/20210427211559.png)

    然后就可以调试了

    ![Image [24]](https://homan-blog.oss-cn-beijing.aliyuncs.com/programming-summary/idea_skill/20210427211610.png)

    前提是本机有项目的源代码 ，在需要的地方打个断点，然后访问一个远程的url试试，断点就会停下来。

### 3.5.临时执行表达式/修改变量的运行值
调试时，可以临时执行一些表达式，参考下图：点击这二个图标中的任何1个都可以

![Image [25]](https://homan-blog.oss-cn-beijing.aliyuncs.com/programming-summary/idea_skill/20210427211620.png)

点击+号后，就可以在新出现的输入框里输入表达式，比如i+5

![Image [26]](https://homan-blog.oss-cn-beijing.aliyuncs.com/programming-summary/idea_skill/20210427211627.png)

然后回车，马上就能看到结果 

![Image [27]](https://homan-blog.oss-cn-beijing.aliyuncs.com/programming-summary/idea_skill/20210427211634.png)

当然，如果调试时，想动态修改变量的值，也很容易，在变量上右击，然后选择Set Value，剩下的事，地球人都知道。

![Image [28]](https://homan-blog.oss-cn-beijing.aliyuncs.com/programming-summary/idea_skill/20210427211641.png)

### 3.6.断点处添加 log

![图片](https://homan-blog.oss-cn-beijing.aliyuncs.com/programming-summary/idea_skill20220607133503.png)

勾选上 `Evaluate and log`, 并自定义你想查看的 log/变量，比如这里的 `"interested" + i`, 这样以 Debug 模式运行程序（正常模式运行，不会打印这些 log）：

```
interested 7
interested 5
interested 1
interested 2
interested 0
Found 2 interested values
```

如果你在多处添加了这种断点，简单的看 log 可能偶尔还是不够直观，可以勾选上面图片绿色框线的 `"Breakpoint hit" message` :

```
Breakpoint reached at top.dayarch.TestDebug.isInterested(TestDebug.java:49)
interested 6
Breakpoint reached at top.dayarch.TestDebug.isInterested(TestDebug.java:49)
interested 0
Breakpoint reached at top.dayarch.TestDebug.isInterested(TestDebug.java:49)
interested 9
Breakpoint reached at top.dayarch.TestDebug.isInterested(TestDebug.java:49)
interested 8
Breakpoint reached at top.dayarch.TestDebug.isInterested(TestDebug.java:49)
interested 1
Found 3 interested values
Disconnected from the target VM, address: '127.0.0.1:0', transport: 'socket'

Process finished with exit code 
```

如果你想要更详细的信息，那就勾选上 `Stack trace` (大家自己查看运行结果吧)，有了这个功能，上面说的一些问题都不复存在了

### 3.7.字段断点

如果你阅读源码，你一定会有个困扰，类中的某个字段的值到底是在哪里改变的，你要一点点追踪调用栈，逐步排查，稍不留神，就可能有遗漏

> 我们可以在 IntelliJ IDEA 中为某个字段添加断点，当字段值有修改时，自动跳到相应方法位置

使用起来很简单：

1. 在字段定义处鼠标左键添加断点（会出现「眼睛」的图标）
2. 在「眼睛」图标上鼠标右键
3. 在弹框中勾选上 `Field access` 和 `Field modification` 两个选项

![图片](https://homan-blog.oss-cn-beijing.aliyuncs.com/programming-summary/idea_skill20220607133836.png)

如果修改字段值的方法比较多，也可以在 `Condition` 的地方定义断点进入条件, 有了这个功能的加成，相信你阅读源码会顺畅许多

### 3.8.异常断点

除了阅读源码，一定是遇到了异常我们才开始调试代码，代码在抛出异常之后会自动停止，但是我们希望：

> 代码停在抛出异常之前，方便我们查看当时的变量信息

这时我们就用到了 `Exception Breakpoints`, 当抛出异常时，在 catch 的地方打上断点，可以通过下图的几个位置获取栈顶异常类型，比如这里的 `NumberFormatException`

![图片](https://homan-blog.oss-cn-beijing.aliyuncs.com/programming-summary/idea_skill20220607133921.png)

知道异常类型后，就可以按照如下步骤添加异常断点了：

![图片](https://homan-blog.oss-cn-beijing.aliyuncs.com/programming-summary/idea_skill20220607133921.png)

然后在弹框中选择 NumberFormatException

![图片](https://homan-blog.oss-cn-beijing.aliyuncs.com/programming-summary/idea_skill20220607133921.png)

重新以 Debug 模式运行程序：

![图片](https://homan-blog.oss-cn-beijing.aliyuncs.com/programming-summary/idea_skill20220607133921.png)

程序「一路绿灯式」定位到抛出异常的位置，同时指出当时的变量信息，三个字：稳，准，狠，还有谁？

### 3.9.方法断点

当阅读源码时，比如 Spring，一个接口的方法可能被多个子类实现，当运行时，需要查看调用栈逐步定位实现类，IDEA 同样支持在接口方法上添加断点（快捷键 `cmd+F8`/`ctrl+F8`）：

1. 鼠标左键在方法处点击断点（♦️形状）
2. 断点上鼠标右键

勾选上绿色框线上的内容，同样可以自定义跳转条件 Condition

![图片](https://homan-blog.oss-cn-beijing.aliyuncs.com/programming-summary/idea_skill20220607133921.png)

当以 Debug 模式运行程序的时候，会自动进入实现类的方法（注意断点形状）：

![图片](https://homan-blog.oss-cn-beijing.aliyuncs.com/programming-summary/idea_skill20220607133921.png)

看到这你应该想到常见的 Runnable 接口中的 run 方法了，同样是有作用的，大家可以自行去尝试了



## 4.小技巧

### 4.1.书签
首先介绍的是 IDEA 的书签功能，可以通过书签快速跳转到相应的源码。
IDEA 书签分为两种，

- 匿名书签，可以生成无数个，使用快捷键 F11 快速生成。
- 标记书签，可以用数字或字母标记书签，总共只能生成 10 个数字以及 26 个字母的标记书签，使用快捷键 Ctrl+F11生成。

两种标签区别如下。

![Image [29]](https://homan-blog.oss-cn-beijing.aliyuncs.com/programming-summary/idea_skill/20210427211651.png)

使用快捷键 Shift + F11，可以打开书签管理窗口，在这里可以删除标签，排序标签，以及给标签添加简单的解释。

![Image [30]](https://homan-blog.oss-cn-beijing.aliyuncs.com/programming-summary/idea_skill/20210427211701.png)

另外使用数字标记的标签，可以使用 Ctrl + 数字键 跳转到相应标签，快速查看源码。

![16b3b2fe5704c473](https://homan-blog.oss-cn-beijing.aliyuncs.com/programming-summary/idea_skill/20210427211707.gif)

### 4.2.收藏夹
第二个介绍的是收藏夹功能，在 IDEA 中，这个功能位于 Favorites。

这个功能可以将文件，文件夹，甚至外部文件加入到 IDEA Favorites。

上面说的标签以及断点会自动加入到 Favorites中。

使用 `Alt + 2` 可以快速打开 Favorites 列表。

![Image [31]](https://homan-blog.oss-cn-beijing.aliyuncs.com/programming-summary/idea_skill/20210427211719.png)

### 4.3.变量命名 / 代码提示
`alt + return `

这里演示一个idea根据提示替换代码的例子(只是简单演示idea的提示与替换功能，代码本身毫无意义)

![](https://homan-blog.oss-cn-beijing.aliyuncs.com/programming-summary/idea_skill/20210427211731.png)

## 5.问题
### 5.1.解决.properties文件中文编码
设置路径为： `file->setting->editor->file encodings`如图所示

![Image](https://homan-blog.oss-cn-beijing.aliyuncs.com/programming-summary/idea_skill/20210427212756.png)

其实据测试，主要是图中5那个地方在生效。不过为了统一，把所有的都设置也没什么毛病。

### 5.2.Intellij IDEA运行报Command line is too long解法
**报错内容:**

Error running 'ServiceStarter': Command line is too long. Shorten command line for ServiceStarter or also for Application default configuration.
**解法:**

修改项目下 `.idea\workspace.xml`，找到标签 `<component name="PropertiesComponent">` ， 在标签里加一行  `<property name="dynamic.classpath" value="true" />`

### 5.3.获取git仓库时更新类型update type 的选择
![Image [2]](https://homan-blog.oss-cn-beijing.aliyuncs.com/programming-summary/idea_skill/20210427212808.png)

### 5.4.Intellij idea 中启动多个tomcat server失败问题解决
如我在由eclipse转intellij Idea中提到，由于由Eclipse刚投入Intellij的怀抱不久，对一些使用尚不熟悉，尤其这两天在Intellij中配置启动多个Tomcat出现了问题。
#### 5.4.1.问题描述
Intellij idea中，为在本地调试两个系统之间的调用，配置两个本地tomcat server，设置不同的端口号，如8081和8082，Deploy中加入两个系统各自的 `Artifact xxx:war, Application context` 设置为 `“/“`，即访问地址分别为 http://localhost:8081/ 和 http://localhost:8082/ 

问题来了，分别单独启动两个server时都能成功；但是同时启动两个系统时，两个系统都会出现问题。其中较先启动的server报错为：`StandardServer.await: Invalid command ” received`，然后会有一个系统报出异常，提示找不到xml或者properties等

#### 5.4.2.寻求解决方法
报出的找不到xml或properties等异常，肯定是误报，因为单独启动时是没有问题的

根据 `StandardServer.await: Invalid command ” received` 百度或者google，得到的结果基本是端口的问题。但是我已经配置了不同的端口号，除上述的http port外，我还查看了 `server.xml` 中的 `shut down port`、`ajp port` 等等，均不相同。大略可以排除端口号的问题。

请教同事，同事解释 `Application context` 不能同为 `”/”`，Intellij会将web发布到tomcat目录下的ROOT中，两者必然冲突。提供了两种解决方案：
1. Application context区别开，如 `”/weba/”` 和 `”/webb/”`
1. 将tomcat安装目录复制一份，用两套tomcat部署

我恍然同时，又觉得Eclipse完全可以实现啊，Intellij这都实现不了是不是有点low了。

#### 5.4.3.问题解决
最终的最终，我发现了问题所在。在Deploy中加入的Artifact不应该是war，而应该选择第二种war explored！

搜索了war和war explored的区别。网上大都在讨论两者最大的区别是explored支持热加载，方便本地修改调试。但是针对本文的问题，没有找到直接解释。

自己浅析一下：war理所当然会打为war包，发布时候脱离了你本地项目目录，发布到了Tomcat目录 `\webapps\ROOT` 下；explored方式，是将web root指向了你的本地项目。因此war形式会产生冲突，而explored方式不会，且explored方式可以热加载。