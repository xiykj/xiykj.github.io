## Top命令：

　　Top相当于Windows中的任务管理器
<img src = 'https://img2020.cnblogs.com/blog/2034475/202006/2034475-20200617095227240-992544115.png'>

　　可以看到，输出结果分两部分，前5行是总览，下面是具体的进程资源占用情况。下面逐行看一下

## 第1行

　　top - 09:52:35 up 41 min, 2 users, load average: 4.25, 4.33, 3.03

　　依次表示：当前时间、系统已经运行的时间、当前登录的用户数、系统在过去的1分钟，5分钟，15分钟的负载

　　（PS：从这一行我们可以知道以下信息

当前时间是09:52:35
系统运行了41分钟
当前有2个用户登录
在过去1分钟，5分钟，15分钟的负载分别是 4.25, 4.33, 3.03，负载超过1，则表示超负荷）

## 第2行

　　Tasks: 173total,   1 running, 172 sleeping,   0 stopped,   0 zombie

　　进程信息

total　　　　进程总数
running　　 运行中的进程数
sleeping　　睡眠中的进程数
stopped　　停止的进程数
zombie　　 僵尸进程数
　　（PS：从这一行我们可以知道，当前总共173个进程）

## 第3行

　　%Cpu(s): 98.9 us, 1.0 sy, 0.0 ni, 0.0 id, 0.0 wa, 0.0 hi, 0.1 si, 0.0 s

　　CPU使用情况

　　us ： 用户进程占用CPU百分比

　　sy ： 内核进程占用CPU百分比

　　ni ： 改变过优先级的进程占用CPU百分比

　　id ： 空闲CPU百分比

　　wa ： IO等待的进程占用CPU百分比

　　hi ： 硬中断占用CPU的百分比

　　si ： 软中断占用CPU的百分比

## 第4行

　　KiB Mem : 949572 total, 55160 free, 537204 used, 357208 buff/cache

　　物理内存使用情况

total　　总的内存大小
used　　已使用
free　　未使用
buffers　　内核缓冲区　　　
　　可用内存 = free + buffers + cached

## 第5行

　　KiB Swap:   102396 total,    91212 free,    11184 used.   240348 avail Mem

　　虚拟内存使用情况

## 其余行
<img src = 'https://img2020.cnblogs.com/blog/2034475/202006/2034475-20200617094808879-1712405038.png'>