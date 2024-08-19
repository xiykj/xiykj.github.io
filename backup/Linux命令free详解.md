## free命令

　　查看计算机中内存使用情况，默认 free 会以 KB 为单位显示信息。free 同样提供给我们 b (B), -k (KB), -m (MB), -g (GB) and –tera (TB)这些单位，要显示我们想要的单位，只要选择一个并在 free 后面跟上
<img src = 'https://img2020.cnblogs.com/blog/2034475/202006/2034475-20200617101458505-1374605463.png'>

- > total 总物理内存
- > used 已经使用的物理内存
- > free 没有使用过的物理内存
- > shared 多进程共享内存
- > buff/cache 读写缓存内存，这部分内存是当空闲来用的，当free内存不足时，linux内核会将此内存释放
- > available 还可以被 应用程序 使用的物理内存

　　
## 若buff/cache过高而free过低，可用以下命令进行释放优化

　　echo 1 > /proc/sys/vm/drop_caches:表示清除pagecache
　　echo 2 > /proc/sys/vm/drop_caches:表示清除回收slab分配器中的对象（包括目录项缓存和inode缓存）slab分配器是内核中管理内存的一种机制，其中很多缓存数据实现都是用的pagecache
　　echo 3 > /proc/sys/vm/drop_caches:表示清除pagecache和slab分配器中的缓存对象