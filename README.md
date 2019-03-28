# Android-environment-architecture

[版权所有，转载注明]()

>换了个新笔记本，刚好写一篇对于初学者的Android环境搭建指南。内容从全新笔记本到新建一个项目。顺便学习一下简书怎么写文档。后续Android环境搭建链接在本文末尾。如有问题还请大佬们在评论出指出，谢谢。

## 1.  配置Java环境

### 1.1  下载并安装jdk和jre

- 首先到Oracle官网下载
>https://www.oracle.com/technetwork/java/javase/downloads/index.html

![图片.png](https://upload-images.jianshu.io/upload_images/3722198-381355d0a2e72589.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![图片.png](https://upload-images.jianshu.io/upload_images/3722198-dd9d9c44cb977d75.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

### 1.2  设置jdk和jre路径

- 虽然默认jdk安装在C:\Program Files\Java\jdk1.8.0_201\目录下，但是**Program Files**中间有个空格，cmd命令行运行时会造成机器不识别，这个后面会讲到。所以建议单独设置为两个单独的没有空格的英文文件夹下，因为cmd命令行也不识别中文。【开发工具】【源代码】【公共JRE】这三个都需要点选。

![图片.png](https://upload-images.jianshu.io/upload_images/3722198-5e3fd1b3a115819d.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- jdk安装完了会新弹出一个窗口，是安装jre的，还是建议改地址。如果没有弹出这个窗口就需要看你是不是下错安装包了。可能你下了个Oracle JDK？

![图片.png](https://upload-images.jianshu.io/upload_images/3722198-628e59ccdfcd6319.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

### 1.3  设置Java环境变量

- 我的电脑>属性>高级系统设置
![图片.png](https://upload-images.jianshu.io/upload_images/3722198-9ab1ca6cba6a39ba.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![图片.png](https://upload-images.jianshu.io/upload_images/3722198-1d8841797e0f22a0.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- 打开环境变量
![图片.png](https://upload-images.jianshu.io/upload_images/3722198-5ff936a9971abe26.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
- 用户变量中新建JAVA_HOME变量（全英文路径）
![图片.png](https://upload-images.jianshu.io/upload_images/3722198-26b3ca9a400197b7.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![图片.png](https://upload-images.jianshu.io/upload_images/3722198-6d6b373ffe52f73d.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
- 系统变量中新增JAVA_HOME变量地址
![图片.png](https://upload-images.jianshu.io/upload_images/3722198-f856f7c258b917c2.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
- 点击新建，添加黑括号中的【;%JAVA_HOME%\bin;%JAVA_HOME%\jre\bin】
![图片.png](https://upload-images.jianshu.io/upload_images/3722198-9ab2045684011d91.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![图片.png](https://upload-images.jianshu.io/upload_images/3722198-203fb9ec184a4ae9.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
- 如果不成功就添加绝对路径地址，记得带上bin文件夹
![图片.png](https://upload-images.jianshu.io/upload_images/3722198-6914dc5a863b0b66.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
- 添加CLASSPATH，地址在黑括号中【.;%JAVA_HOME%\lib;%JAVA_HOME%\lib\tools.jar;】
![图片.png](https://upload-images.jianshu.io/upload_images/3722198-42dda42b4184be4d.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![图片.png](https://upload-images.jianshu.io/upload_images/3722198-cc6fdc9807861ded.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
- 如果不成功就添加绝对路径地址
![图片.png](https://upload-images.jianshu.io/upload_images/3722198-18e69264ffda7249.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
- 检测是否配置成功Win+R打开运行菜单，输入cmd，点击确定
![图片.png](https://upload-images.jianshu.io/upload_images/3722198-170b245db68e01d5.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
###1.4 检测是否配置成功
- 在编辑器里输入【java】，回车
![图片.png](https://upload-images.jianshu.io/upload_images/3722198-b506cc0a2ca6aad2.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
- 在编辑器里输入【javac】，回车
![图片.png](https://upload-images.jianshu.io/upload_images/3722198-7e896704f1a87acc.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
- 在编辑器里输入【java -verson】，回车
![图片.png](https://upload-images.jianshu.io/upload_images/3722198-2edd656373ea94ed.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- 如果出现和上面三图所示的界面，说明配置成功。
