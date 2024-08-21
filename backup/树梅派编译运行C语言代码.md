　　因为树梅派自带gcc套件，gcc是支持C语言，下面就教大家在树梅派上编写C语言程序

　　1.首先用vim编辑代码，编写一个简单的C语言程序如下，并将文件名改为test.c，如下图所示：
```P4
#include <stdio.h>
#include <stdlib.h>
//#include <system.h>
int main()
{
    printf("cat，江西省乐安县山砀镇\n");
    printf("以下班车开往乐安:\n\n");
    //system("color 0a");
    printf("      蕉坑\n");
    printf("丰城============乐安\n");
    printf("      山砀\n\n");
    int a;
    scanf("%d",&a);
    printf("刚才输入的a=%d\n",a);
    printf("a+100=%d\n",a+100);
    return 0;
}
```
<img src = 'https://img2020.cnblogs.com/blog/2034475/202007/2034475-20200701100847479-590631549.png'>
<br/>

　　2.用gcc编译test.c文件，编译完成后会在相同目录下生成可执行程序文件 "test.exe"，命令如下：
```P4
gcc test.c -o test
```

<img src = 'https://img2020.cnblogs.com/blog/2034475/202007/2034475-20200701101352844-1972649266.png'>

<img src = 'https://img2020.cnblogs.com/blog/2034475/202007/2034475-20200701101752071-818764055.png'>
<br/>

　　3.运行可执行文件test，输入以下命令即可运行
```P4
./test
```
