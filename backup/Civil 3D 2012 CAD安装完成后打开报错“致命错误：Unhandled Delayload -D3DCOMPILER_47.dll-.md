 今天在客户电脑上安装完cad 2012后打开cad显示报错：致命错误:Unhandled Delayload "D3DCOMPILER-47.dll"
![1](https://img2020.cnblogs.com/blog/2034475/202012/2034475-20201207170056581-411438569.png)
查询原因是缺少微软的补丁KB4019990（文后将提供补丁的下载链接）；因为CAD软件启动时 "D3DCOMPILER_47.dll" 文件没有集成在系统中，所以微软原版系统刚安装完的时候并不是把所有的.dll文件都安装完全的，需要自己另外安装的即可解决问题。

### 解决方法是电脑安装补丁程序（KB4019990）
补丁程序下载
1，链接地址
　　　　链接：https://pan.baidu.com/s/1mAj8_1C5T0l4Bm8LM2mCMA 

　　　　提取码：mykm

2，在打开的网页中选择和自己电脑一样系统对应的补丁进行下载。
![2](https://img2020.cnblogs.com/blog/2034475/202012/2034475-20201207170203105-166744640.png)
3，下载完成后双击安装补丁程序
![3](https://img2020.cnblogs.com/blog/2034475/202012/2034475-20201207170236001-2069391892.png)
 4，安装成功后再启动CAD 2012就可以正常运行了
![4](https://img2020.cnblogs.com/blog/2034475/202012/2034475-20201207170259196-1449772479.png)