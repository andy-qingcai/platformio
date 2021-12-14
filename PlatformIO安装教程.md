## 什么是PlatformIO

​	[PlatformIO](https://platformio.org/)是一个用于物联网开发的开源生态系统。它提供跨平台的开发环境和统一的调试器，还支持远程单元测试和固件更新...

## PlatformIO的用处是什么

​	简单来说，就是不管你用什么型号的芯片，都可以直接在platformio这个平台上直接编码烧录。对于有些芯片，官方的编码软件可能是你没有接触过的，这时你就需要熟悉新得软件，而platformio集成了大多数芯片的SDK，使得在这一个平台上就可以解决绝大部分的问题。

## 如何安装PlatformIO

 1.  在线安装(安装的成功率低)

     首先你得有个VScode，然后在扩展这里搜索点击安装就可以了

     ![image-20211214154744756](C:\Users\liu84\AppData\Roaming\Typora\typora-user-images\image-20211214154744756.png)

 2.  官方包安装(程序复杂，成功率高)

​		安装PlatformIO时，大部分可能卡在Core部分无法安装，所以直接去官方下载Core并安装，首先给出[官方文档](https://docs.platformio.org/en/latest/core/installation.html)

  1.   安装python

       ​	官方文档中，安装PlatformIO是基于python来实现的，为了省去python配置环境路径的步骤，选择Microsoft Store 中下载python 3.7，高版本可能出现问题

​			安装完python后，先win+R 打开CMD ，输入python，这时如果弹出了Python的版本信息，则		为安装成功

 2.  安装virtualenv 

     输入pip install virtualenv 安装python的虚拟环境管理包 virtualenv

 3.  创建虚拟环境

     创建格式为：virtualenv  虚拟环境名

     如：virtualenv andy

     由于Platformio默认安装在C:\Users\Username中，所以要在Username下创建一个名为.platformio 的文件夹( 这里的USername表示登入的windows的用户的文件名)

​		然后win + R 打开cmd ，输入指令

~~~cmd
call C:\
cd C:\Users\Username\.platformio
virtualenv andy
~~~

4. 安装虚拟环境必备组件

~~~
call C:\
cd C:\Users\Username\.platformio
andy\Scripts\activate
pip install git
pip install  platformio
~~~

 5.   正式安装Platformio

     这时就可以回到VScode，在拓展中选择旧版本安装，选择的python路径就是虚拟环境内的python路径，等待上半小时，差不多就安装完了(可能还要失败个几次)



