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




