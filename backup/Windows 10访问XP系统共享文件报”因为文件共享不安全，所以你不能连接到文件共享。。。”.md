　　今天单位同事说他在电脑上访问XP系统共享的打印机时，结果出现下面报错：因为文件共享不安全，所以你不能连接到文件共享，此共享需要过时的SMB1协议…
<img src = 'https://img2020.cnblogs.com/blog/2034475/202012/2034475-20201208105047672-1483129223.png'>
　　

### 解决方法：

　　1. 打开计算机“控制面板”，找到“程序”，在左侧点击“启用或关闭Windows功能”
<img src = 'https://img2020.cnblogs.com/blog/2034475/202012/2034475-20201208105302083-774827153.png'>
　　

 　　2. 往下拖动：找到“SMB 1.0/CIFS 文件共享支持”把前面勾选上
<img src = 'https://img2020.cnblogs.com/blog/2034475/202012/2034475-20201208105350458-2081729669.png'>
　　
 　　3. 确定后重启计算机就可以正常访问了
<img src = 'https://img2020.cnblogs.com/blog/2034475/202012/2034475-20201208105424416-329483421.png'>
　　

### 除了以上方法，微软官方也提供了通过PowerShell来进行设置的方法，用管理员权限打开Powershell之后，可以参考下面的命令：   

#### SMB v1
```
　　检测: Get-WindowsOptionalFeature –Online –FeatureName SMB1Protocol

　　禁用: Disable-WindowsOptionalFeature -Online -FeatureName SMB1Protocol

　　启用: Enable-WindowsOptionalFeature -Online -FeatureName SMB1Protocol
```
#### SMB v2/v3
```
　　检测:Get-SmbServerConfiguration | Select EnableSMB2Protocol

　　禁用:Set-SmbServerConfiguration –EnableSMB2Protocol $false

　　启用:Set-SmbServerConfiguration –EnableSMB2Protocol $true
```