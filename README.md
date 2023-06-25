# C-p29-2-
C语言学习笔记 p29数据的存储(2)
#include<stdio.h>
int main()
{
    //写一段代码实现判断大小端
    int a=1;
    char* p=(char*)&a;
    if(*p==1)
    {
        printf("小端\n");
    }
    else
    {
        printf("大端\n");
    }
    return 0;
}

//函数方法
chack_sys()
{
    int a=1;
    char* p=(char*)&a;
    //1小端
    //0大端
    return *p;
}

//方法2
int check_sys()
{
    int a=1;
    return *(char*)&a;
}
int main()
{
    //返回1-小端
    //返回0-大端
    int ret=check_sys();
    if(ret==1)
    {
        printf("小端\n");
    }
    else
    {
        printf("大端\n");
    }
    return 0;
}

int main()
{
    char a=-128;
    //10000000000000000000000010000000
    //11111111111111111111111101111111
    //11111111111111111111111110000000-补码
    //11111111111111111111111110000000-由于符号为1所以整形提升也全补1
    printf("%u\n",a);
    return 0;
}

//有符号的char范围是-128到127，无符号的char是0-255

int main()
{
    
    return 0;
}
