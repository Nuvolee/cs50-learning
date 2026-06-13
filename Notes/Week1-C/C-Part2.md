---
Title: CS50 Week1 - C -Part2
Labels: 随笔
Keywords: CS50,C
Date: 2026-06-09
---


# 借助库实现ask
```
#include <cs50.h>
#include <stdio.h>

int main(void)
{
    string answer = get_string("What's u name? ");
    printf("hello, %s\n", answer);
}
```

## 保存函数的返回值
`string` `answer` = `get_string("What's u name? ");`  
- `string`：返回值的`类型`
- `answer`：返回值的`变量名`
- `get_string( )`:函数
返回值的类型  返回值的变量名  =  函数


## 占位符 %s
printf("hello, `%s`\n"`,` `answer`);
- `%s`：占位符
- `answer`:要替换占位符的变量  
- `,`:区分第一个输入和第二个参数  
注意：`answer`这个输入，是由用户提供的。`hello`这个输入，是我们提供的。




# Linux
使用CLI命令行界面。

## 常用命令
|命令|作用|
|-|-|
|mkdir 文件夹名|创建文件夹|  
|rm 文件名|删除文件|  
|mv 文件名 目标地址/|移动文件|
|mv 原文件名 新文件名|重命名|
|cd 目标位置/|切换目录|
|cp 源文件名 新文件名|复制备份|
|.|当前文件夹|
|..|父文件夹(向上返回一级)|



# 计数器
`code compare.c`  

```
#include <cs50.h>
#include <stdio.h>

int main(void)
{
    int x = get_int("What's x? ");
    int y = get_int("What's y? ");

    if (x < y)
    {
        printf("x is less than y\n");
    }

    else if (x > y)
    {
        printf("x is greater than y\n");
    }
    else
    {
        printf("x is equal to y\n");
    }
}
```

`make compare`  
`./compare`



# 

`code agree.c`  

```
#include <cs50.h>
#include <stdio.h>

int main(void)
{
    char c = get_char("Do you agree? ");

    if (c == 'y' )
    {
        printf("Agreed.\n");
    }
    else if (c == 'n')
    {
        printf("Not agreed.\n");
    }
}
```

- if (c == 'y' ) 中使用单引号`'`：在C中，比较单个字符时，用char类型和单引号。


`make agree`  
`./agree`


## BUG
但是如果输入其他内容
```
$ ./agree
Do you agree? No
Do you agree? Y
Not agreed.  
```
因为`get_char`函数的特点是：获取的数据类型是特定的。  


# 逻辑运算符
`||`    或  
`&&`    与  

```
#include <cs50.h>
#include <stdio.h>
int main(void)
{
    char c = get_char("Do you agree? ");

    if (c == 'y' || c =='Y')
    {
        printf("Agreed.\n");
    }
    else
    {
        printf("Not agreed.\n");
    }
}
```


# loops 循环
`code cat.c`

```
#include <stdio.h>

int main(void)
{
    printf("Meow\n");
    printf("Meow\n");
    printf("Meow\n");
}

```

`make cat`  
`$ ./cat
Meow
Meow
Meow`  


## while循环修改
```
#include <stdio.h>

int main(void)
{
    int i = 3;
    while (i > 0)
    {
        printf("Meow\n");
        i--;
    }
}
```

```
$ make cat
$ ./cat
Meow
Meow
Meow
```


## 修改
```
#include <stdio.h>

int main(void)
{
    int i = 0;
    while (i < 3)
    {
        printf("Meow\n");
        i++;
    }
}
```

```
$ make cat
$ ./cat
Meow
Meow
Meow
```

## for循环修改
```
#include <stdio.h>

int main(void)
{
    for (int i = 0; i < 3; i++)
    {
        printf("Meow\n");
    }
}
```

```
$ make cat
$ ./cat
Meow
Meow
Meow
```

