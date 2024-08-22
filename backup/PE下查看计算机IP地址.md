　　今天早上同事说他的电脑系统崩了，无法进系统，他之前部门分配的固定IP地址也找不见了，问能在PE下找到IP地址不，我说那就试试吧！

　　功夫不负有心人，找了一圈资料，终于知道IP地址等信息存在系统注册表中，万幸的是没有提前把系统盘格式化了，哈哈 ^~^ 请允许我不厚道地笑两声，话不多说，直奔主题

### 1. 用U盘工具进入PE系统，打开注册表编辑工具
<img src = 'https://s3.bmp.ovh/imgs/2024/08/22/e6b52650679f2590.png' >


### 2. 进入注册表编辑工具后，定位到 HKEY_LOCAL_MACHINE 项
<img src = 'https://s3.bmp.ovh/imgs/2024/08/22/94a5865c7c0de38b.png' >


### 3. 点击菜单上“文件”，“加载配置单元”选项
<img src = 'https://s3.bmp.ovh/imgs/2024/08/22/ba7af2d3dcdd5211.png' >


### 4. 选择系统目录下的system文件，一般在 C:\windows\system32\config 目录下
<img src = 'https://s3.bmp.ovh/imgs/2024/08/22/f1645780a2604a92.png' >


### 5. 这里名称随便起一个，我这里示范用 test
<img src = 'https://s3.bmp.ovh/imgs/2024/08/22/fd0f1bcfaac36d4c.png' >


### 6. 加载完成后在 HKEY_LOCAL_MACHINE 下就有刚新增的 test 项了
<img src = 'https://s3.bmp.ovh/imgs/2024/08/22/2f8796c6c40ef530.png' >


### 7. 展开test项，依次定位到“HKEY_LOCAL_MACHINE\test\ControlSet001\Services\Tcpip\Parameters\Interfaces"项
<img src = 'https://s3.bmp.ovh/imgs/2024/08/22/4cb1ebfd22b1a68b.png' >


### 8. 在Interfaces下有许多小项，这里面每一项都代表着网卡信息，依次查看就能获取你之前设置的IP地址了
<img src = 'https://s3.bmp.ovh/imgs/2024/08/22/2a66feb3ccbf042c.png' >