[toc]



# Typora 集成 PicGo 快速处理文章图片

参考文章:https://mp.weixin.qq.com/s/y9cSrNbJ94rYz1Hphi5efQ



## PicGo 配置

### 版本要求

1. PicGo 2.2.0 及以上



### 下载路径

1. **GitHub**:https://github.com/Molunerfinn/PicGo/releases
2. 百度网盘（PicGo-Setup-2.2.2.exe）：https://pan.baidu.com/s/14S0-c_aql75Ti0l4jLEd7w



### 相关配置

1. [官方指南](https://picgo.github.io/PicGo-Doc/zh/guide/)

2. [GitHub 图床配置](https://picgo.github.io/PicGo-Doc/zh/guide/config.html#github%E5%9B%BE%E5%BA%8A)

   注：现在默认分支是mian

3. `PicGo 设置`=>`选择显示的图床`=>勾选`GitHub图床`，方便后面使用

   ![](https://raw.githubusercontent.com/HomanLiang/pictures/main/programming-summary/typora-picgo/typora_picgo_001.png)

4. 激活PicGo-Server

   2.2.0 版本之后，PicGo 内部会默认开启一个小型的服务器，用于配合其他应用来调用 PicGo 进行上传。

    `PicGo 设置`=>`设置Server`，参考下图进行设置即可

   ![](https://raw.githubusercontent.com/HomanLiang/pictures/main/programming-summary/typora-picgo/typora_picgo_002.png)

   

## Typora  配置

### 版本要求

1. Typora 0.9.84 及以上



### 设置

1. `文件`=>`偏好设置`=>`图像`，参考图片中的进行配置，选择本机 PicGo 的路径

![](https://raw.githubusercontent.com/HomanLiang/pictures/main/programming-summary/typora-picgo/typora_picgo_004.png)



2. 验证图片上传

   这里还可以验证图片上传功能

   验证成功会返回下图结果：

   ![typora_picgo_003](https://raw.githubusercontent.com/HomanLiang/pictures/main/programming-summary/typora-picgo/typora_picgo_003.png)

   

3. 如果验证失败，请确定端口是否和`PicGo-Server一致`，如上图红框所示。



## 使用

上面的设置完成后，在 Typora 里写字时，就可以自动上传图片到图床啦

### 拖拽

可以直接选择图片，然后拖拽到编辑页面

![](https://raw.githubusercontent.com/HomanLiang/pictures/main/programming-summary/typora-picgo/typora_picgo_005.gif)



### 编辑器内插入

使用快捷键 Ctrl + Shift + I，可以调出插入图片的功能

![](https://raw.githubusercontent.com/HomanLiang/pictures/main/programming-summary/typora-picgo/typora_picgo_006.gif)





### 复制粘贴

也可以直接复制图片，然后再编辑器中直接粘贴。或者截图后直接粘贴（比如 Snipaste）

![typora_picgo_007](https://raw.githubusercontent.com/HomanLiang/pictures/main/programming-summary/typora-picgo/typora_picgo_007.gif)



这里需要多一个点击上传图片的操作。

然后图片就可以上传到图床了。





另外，还可以看到所有的上传在 PicGo 的相册里都能找到：

![typora_picgo_008](https://raw.githubusercontent.com/HomanLiang/pictures/main/programming-summary/typora-picgo/typora_picgo_008.png)









































