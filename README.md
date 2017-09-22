# 三宝机器人局域网群控服务器搭建教程

> ### **写在前面的话：**

这是一篇非常详细的局域网搭建教程，由Frank根据研发的原始的PDF教程改编而来。在此教程中，为了照顾很多新手（比如不知道一些基础的网络知识的人，例如，不懂路由器WIFI配置，不懂什么是WAN,什么是LAN,什么是 Cent OS系统, 文档中涉及的一些基础的linux命令等等），我们添加了一部分相关注释和说明，尽量降低该文档的操作难度，让这部分也能力愉快的参考该文档完成局域网搭建工作。

---

**本教程目录如下：**

* [**1.前提**](https://frank202020.gitbooks.io/group-control/content/part1/)
  * [1.1 硬件要求](https://frank202020.gitbooks.io/group-control/content/part1/1.1.html)
  * [1.2 局域网环境](https://frank202020.gitbooks.io/group-control/content/part1/1.2.html)
* [**2.CentOS-7.2系统安装**](https://frank202020.gitbooks.io/group-control/content/part2/)
  * [2.1 选择开机启动模式](https://frank202020.gitbooks.io/group-control/content/part2/2.1.html)
  * [2.2 系统安装](https://frank202020.gitbooks.io/group-control/content/part2/2.2.html)
    * [2.2.1 进入图形化](https://frank202020.gitbooks.io/group-control/content/part2/2.2.1.html)
    * [2.2.2 未进入图形化界面的处理方法](https://frank202020.gitbooks.io/group-control/content/part2/2.2.2.html)
* [**3.局域网服务器环境搭建**](https://frank202020.gitbooks.io/group-control/content/part3/)
  * [3.1 关闭系统防火墙](https://frank202020.gitbooks.io/group-control/content/part3/3.1.html)
  * [3.2 在局域网服务器上安装旗翰云](https://frank202020.gitbooks.io/group-control/content/part3/3.1.html)
  * [3.3 账号管理](https://frank202020.gitbooks.io/group-control/content/part3/3.3.html)
    * [3.3.1 添加账号](https://frank202020.gitbooks.io/group-control/content/part3/3.3.1.html)
    * [3.3.2 删除账号](https://frank202020.gitbooks.io/group-control/content/part3/3.3.2.html)
* [**4.环境配置**](https://frank202020.gitbooks.io/group-control/content/part4/)
  * [4.1 PC端Q-Link的环境配置](https://frank202020.gitbooks.io/group-control/content/part4/4.1.html)
  * [4.2 机器人端环境配置](https://frank202020.gitbooks.io/group-control/content/part4/4.2.html)
* [**5.群控文件管理**](https://frank202020.gitbooks.io/group-control/content/part5/)
  * [5.1 PC端Q-Link端群控文件配置](https://frank202020.gitbooks.io/group-control/content/part5/5.1.html)
  * [5.2 机器人端环境配置](https://frank202020.gitbooks.io/group-control/content/part5/5.2.html)
* [**6.常见FAQ解答**](https://frank202020.gitbooks.io/group-control/content/part6/)
  * [6.1 选择开机启动顺序之后， 页面一直没有进入图像化界面](https://frank202020.gitbooks.io/group-control/content/part6/6.1.html)
  * [6.2 第一次完成安装系统重启之后，系统继续提示 install Centos 界面，安装进入循环](https://frank202020.gitbooks.io/group-control/content/part6/6.2.html)
  * [6.3 搭载好服务器之后再 PC-Qlink 端发现登不上去，显示网络错误](https://frank202020.gitbooks.io/group-control/content/part6/6.3.html)
  * [6.4 在连接 PC Q-link 时显示账号或密码有错误，无法成功登陆 PC Q-link](https://frank202020.gitbooks.io/group-control/content/part6/6.4.html)
  * [6.5 输入的账号和密码和 account\_info.conf 文件中设置的一致，但是还是登不上 PC Q-link](https://frank202020.gitbooks.io/group-control/content/part6/6.5.html)
  * [6.6 已按照 4、 5 操作但是还是登不上 PC Q-link](https://frank202020.gitbooks.io/group-control/content/part6/6.6.html)
  * [6.7 服务器已经搭载完成，在 PC-Qlink 端添加机器人没有反应，不能添加机器人为好友](https://frank202020.gitbooks.io/group-control/content/part6/6.7.html)
  * [6.8 已登上 PC Q-link，并且成功添加机器人为好友，群控组已经建立，但是点击舞蹈键，机器人没有反应](https://frank202020.gitbooks.io/group-control/content/part6/6.8.html)
  * [6.9 服务器搭载完成后，去其他地方做演示，但是显示屏连上服务器之后屏幕显示的是黑屏，但是之前演示的时候没有遇到过这种情况](https://frank202020.gitbooks.io/group-control/content/part6/6.9.html)
  * [6.10 若是按照上述方法仍然无法成功实现群控，请您再次安装本文档步骤重新部署群控环境](https://frank202020.gitbooks.io/group-control/content/part6/6.10.html)



