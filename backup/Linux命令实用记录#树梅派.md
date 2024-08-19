### 查看内存使用情况

free -m            查看内存使用情况
free -m -s 10            内存情况每隔10秒刷新一次
<br/>

### 终止命令并退出

ctrl+C             终止命令
<br/>

### 查看进程内存占用情况

top            查看进程内存情况
<br/>

### 查看Linux版本

uname -a            查看linux内核版本
<br/>

### 查看cpu配置

cat /proc/cpuinfo            查看cpu信息
lscpu　　        查看cpu信息
<br/>

### 查看树梅派型号

cat /proc/device-tree/model            查看树梅派版本信息
<br/>

### 查看cpu温度

vcgencmd measure_temp            查看cpu温度
<br/>

### 查看cpu时钟频率

vcgencmd get_config arm_freq            查看cpu时钟频率
<br/>

### 查看GPIO

gpio readall            查看GPIO定义
pinout                查看GPIO定义
<br/>

### 查看磁盘使用情况

sudo df -h            查看磁盘使用情况
<br/>

### 调节音量大小

alsamixer            树梅派图形化调节音量大小
<br/>

### 树梅派设置

sudo raspi-config            树梅派设置中心
<br/>

### 终端清屏命令

clear            命令终端清屏
ctrl+L            命令终端清屏
<br/>

### 查找命令

find ./ -name '*郑源*'            在当前目录下查找文件名中间有“郑源”两字
find ./ -name '郑*'            查找以“郑”字开头的所有文件
find / -name '*.flac'            全盘查找所有“flac”格式的文件
find / -iname 't*'　　        全盘查找所有以t开头的文件，加iname不区分t的大小写
<br/>

### 安装#搜索软件

sudo apt-get update            更新软件源列表
sudo apt-get install XXX            安装软件，XXX指具体软件包名
sudo apt-cache search XXX            搜索软件包名，XXX为软件包名
<br/>

### 查看历史使用过的命令

history            查看历史使用过的命令
<!-- ##{"script":"<script src='https://blog.meekdai.com/Gmeek/plugins/GmeekTOC.js'></script>"}## -->
