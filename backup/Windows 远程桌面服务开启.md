　　今天，同事说她的电脑远程桌面服务开了，但是电脑还是无法远程桌面连接（系统是windows 7 Professional X64）
<img src = 'https://img2020.cnblogs.com/blog/2034475/202012/2034475-20201208112655040-1781087037.png'>
　　
## 解决方法
### 1. 检查发现电脑远程桌面连接都开着的，且是任意版本远程桌面都可以连接
<img src = 'https://img2020.cnblogs.com/blog/2034475/202012/2034475-20201208112711741-244453501.png'>
　　

### 2. 在注册表中检查远程桌面的端口号是不是被篡改了，在“HKEY_LOCAL_MACHINE/SYSTEM/CurrentControlSet/Control/Terminal server/Wds/Tcp”中的 PortNumber 值是 3389，windows远程桌面的默认端口号并未被更改
<img src = 'https://img2020.cnblogs.com/blog/2034475/202012/2034475-20201208112729360-1198313302.png'>
　　

　　在另一个端口号中查询“HKEY_LOCAL_MACHINE/SYSTEM/CurrentControlSet/Control/Terminal server/Winstations/RDP-TCP”中的 PortNumber 值是 3389，windows远程桌面的默认端口号并未被更改
<img src = 'https://img2020.cnblogs.com/blog/2034475/202012/2034475-20201208112804777-273022233.png'>
　　　

### 3. 在windows防火墙中发现防火墙开着的，同事说她的防火墙必须要开启，因为这是一台服务器，防火墙开着那就要把端口权限给开放，在防火墙“入站规则”加入端口即可
<img src = 'https://img2020.cnblogs.com/blog/2034475/202012/2034475-20201208112826087-580387932.png'>
　　　

　　点击“高级设置”进入防火墙权限开放
<img src = 'https://img2020.cnblogs.com/blog/2034475/202012/2034475-20201208112837930-177213142.png'>
　　

　　在“入站规则”中新建规则，选择端口，把3389端口给添加进去
<img src = 'https://img2020.cnblogs.com/blog/2034475/202012/2034475-20201208112858208-1590055141.png'>
　　　　

### 4. 检查3389端口是否在 LISTENING 状态，在cmd命令终端输入： netstat -ano | find "3389"
<img src = 'https://img2020.cnblogs.com/blog/2034475/202012/2034475-20201208112918906-1284936439.png'>
　　

### 5. 如果输入 netstat -ano | find "3389" 后什么也没有，或者端口号后面没有 LISTENING ，那就把远程桌面的服务重启下，服务名为：Remote Desktop Services
<img src = 'https://img2020.cnblogs.com/blog/2034475/202012/2034475-20201208112940260-1292815377.png'>
　　

### 6. 再次连接即可成功，输入用户名和密码便可登入
<img src = 'https://img2020.cnblogs.com/blog/2034475/202012/2034475-20201208113108622-1226406499.png'>

　　