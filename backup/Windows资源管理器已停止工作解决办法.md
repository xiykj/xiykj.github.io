　　今天在单位同事说她的电脑资源管理器老是停止工作，过去一看还真是如此，把计算机文件打开着，隔个几分钟就停止工作
<img src = 'https://img2020.cnblogs.com/blog/2034475/202012/2034475-20201208141308281-1965155116.png'>
　　

## 解决方法：

### 先在windows更新中把最近几天的系统更新都卸载了，然后再按下面修改注册表的方法进行

　　1. 在运行对话框中输入regedit命令，点击确定进入注册表界面
<img src = 'https://img2020.cnblogs.com/blog/2034475/202012/2034475-20201208141403833-663526148.png'>
　　

 　　2. 依次定位到注册表项：HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Policies
<img src = 'https://img2020.cnblogs.com/blog/2034475/202012/2034475-20201208141545834-1138328548.png'>
 　　 

 　　3. 右键点击Policies项，选择【新建】，【项】将其命名为 System
<img src = 'https://img2020.cnblogs.com/blog/2034475/202012/2034475-20201208141638401-1972316773.png'>
　　

 　　4. 接着在System项右侧空白区域选择【新建】，【字符串值】将其命名为 DisableTaskMgr
<img src = 'https://img2020.cnblogs.com/blog/2034475/202012/2034475-20201208141718512-1776488831.png'>
　　

 　　5. 双击打开新建的DisableTaskMgr数值，将其数据设置为0，点击确定再运行电脑观察是否正常
<img src = 'https://img2020.cnblogs.com/blog/2034475/202012/2034475-20201208141750209-368407999.png'>
　　

　　6. 如果还是不行那就只有重装系统了……祝各位运维人员早日铲除Bug ^~~^