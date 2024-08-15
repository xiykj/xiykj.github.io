　　这两天突然想在树梅派上写博客文章，因照片素材都是存在手机上的，每次插拔usb接口实在太麻烦了，想着能不能用无线传输文件呢？

　　之前在windows中用过CHFS搭建服务进行文件共享，感觉传输速率和使用都挺方便，也知道CHFS有Linux版本，而且这个软件是开源的，试想着看那就试试吧！访问CHFS官网 http://iscute.cn/chfs 进行软件下载，因为我这是树梅派，树梅派的架构是arm，这点可以在 终端输入 uname -a 查看自己的Linux版本号
![1](https://img2020.cnblogs.com/blog/2034475/202006/2034475-20200611105522161-1182684116.png)
　　
　　1.命令行进行文件解压 unzip chfs-linux-arm-2.0.zip
![2](https://img2020.cnblogs.com/blog/2034475/202006/2034475-20200611110137864-757001625.png)
　　
　　2.进入管理员模式或者以sudo运行（以下所有命令都以管理员运行）

　　3.在 etc 文件下新建一个chfs文件目录命令：  sudo mkdir /etc/chfs

　　4.将刚解压的chfs文件复制到 /etc/chfs 目录下命令：   sudo /home/pi/Downloads/chfs /etc/chfs

　　5.进入 /etc/chfs 目录下命令：  cd /etc/chfs

　　6.建立配置文件  config.ini  输入命令：  sudo vim config.ini 

　　　　进入vim编辑模式按下字母 i 键，复制以下语句
```
port=96
path=/home/pi
rule=::pi:raspberry:d
log=/etc/chfs/logs
```

　　然后按 esc 键退出编辑模式，输入  :wq 保存退出

> port     为端口号
> path    是你要共享的文件根目录
> rule     是帐号以及权限设置
> log      是日志文件

　　7.给 chfs目录赋予权限，用  sudo chmod -R 755 chfs   出错检查R是否为大写 是否是管理员权限

　　8.命令运行 sudo nohup /etc/chfs/chfs --file=/etc/chfs/config.ini &
　　　　输入后出现以下结果
![3](https://img2020.cnblogs.com/blog/2034475/202006/2034475-20200611113512494-1861986756.png)
　　　　
　　9.输出到nohup.out了，我们用 sudo cat nohup.out  来查看开放那个ip 就可以直接连接了
![4](https://img2020.cnblogs.com/blog/2034475/202006/2034475-20200611114050656-927378399.png)
　　　　
　　10.这里我们可以看到服务器地址是 192.168.43.155:96 我们直接在浏览器中输入地址即可访问，可以对文件进行操作
![5](https://img2020.cnblogs.com/blog/2034475/202006/2034475-20200611114323067-655834980.png)