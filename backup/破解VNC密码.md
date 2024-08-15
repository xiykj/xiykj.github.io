VNC由Olivetti & Oracle研究室所开发，此研究室在1999年併入美国电话电报公司（AT&T）。AT&T於2002年中止了此研究室的运作，并把VNC以GPL释出。

　　由於VNC以GPL授权，衍生出了几个VNC软体：　　　
```
- RealVNC：由VNC团队部份成员开发，分為全功能商业版及免费版。
- TightVNC：强调节省频宽使用。
- UltraVNC：加入了TightVNC的部份程式及加强效能的图型映射驱动程式，并结合Active Directory及NTLM的帐号密码认证，但仅有Windows版本。

### Vine Viewer：MacOSX的VNC用户端。
　　这些软体各有所长，例如UltraVNC支援档案传输以及全萤幕模式。而这些软体间大多遵循基本的VNC协定，因此大多可互通使用。

- http://www.realvnc.com/   　         REALVNC
- http://www.tightvnc.com/               TIGHTVNC
- http://ultravnc.com/                       ULTRAVNC
```
　　有时候，在Windows端忘记了VNC的远程登入密码，无法通过远程控制计算机，把vnc卸载了密码还是原来的（因为vnc从第一次进行安装的时候就把password写入系统注册表中）

　　这里涉及的hack软件为“K8fcukVNC4”，具体使用方法：

　　请输入RealVNC密码Hex值,Hex可以从注册表中获得 默认所在注册表位置如下

　　　　3.x 在 HKEY_CURRENT_USER\Software\ORL\WinVNC3\Password ===windows 95
　　　　3.x 在 HKEY_LOCAL_MACHINE\SOFTWARE\ORL\WinVNC3\Default\Password ===Win NT
　　　　4.x 在 HKEY_LOCAL_MACHINE\SOFTWARE\RealVNC\WinVNC4 ===WinXP or Win2003
　　　　5.x 在 HKEY_LOCAL_MACHINE\SOFTWARE\RealVNC\vncserver ===WinXP or Win2003

　　　　提示: 5.x 的加密算法已改 暂时没法破解 但是也可以用"替换法"来提权

　　　　用法: K8fuckVNC4.exe "16,b0,5a,07,f6,ab,0f,c3"

　　软件下载链接：链接：https://pan.baidu.com/s/13CMLUwhnGq66bhF_936SvQ 　　提取码：77lt 
![image](https://github.com/user-attachments/assets/29edd88e-1e47-4a89-8329-eb25846ad1e9)

 　　这是我的vnc密码所在的注册表位置；我这里用的是Tightvnc
![2](https://img2020.cnblogs.com/blog/2034475/202005/2034475-20200526170706871-845600530.png)
