Windows刚安装完系统后、有些软件必须要先update patch后才能进行软件安装，如果补丁一个个用手操作的话简直要feng了，现在通过Windows命令for循环来批量安装Windows补丁程序，又快又方便，释放自己的双手简直爽飞了，以下是Windows中for命令批量安装补丁程序代码：
```
@Echo Off
color 0a
Title Install Windows Update pack
Echo 正在安装Windows系统补丁，请稍等......
for %%i in (*.exe) do %%i /passive /norestart /nobackup
For %%F In (*.msu) Do Call :Update %%F
Shutdown.exe -r -t 30
Exit
:Update
Echo 现在Update补丁程序:      %1    安装完成
Start /Wait %1 /quiet /norestart
GoTo :EOF
Exit
```
将以上代码复制粘贴在记事本中，然后另存文件名称为：Windows_patch.bat，文件类型选择所有（注：.bat文件是Windows中的批处理程序）/不会操作的朋友在这里附上下载地址：https://pan.baidu.com/s/1ZH-62opziEeYwn5jskNblw 　提取码：w32c

将下载的所有补丁程序和 Windows_patch.bat 文件放在同一个文件夹中，然后双击“Windows_patch.bat”文件运行程序。

程序运行过程如下图：列表中会显示当前正在update的补丁程序名称和安装结果。
![1](https://img2020.cnblogs.com/blog/2034475/202006/2034475-20200604093333951-577597651.png)
安装结束后、程序将在1分钟后Reset PC，重启完成后就安装好了所有的补丁程序。

我也是最近在学习计算机语言，以后会将自己所学习的知识一起分享给大家。