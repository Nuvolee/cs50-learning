---
Title: CS50 Week1 - C -Part1
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
- string：返回值的`类型`
- answer：返回值的`变量名`
- get_string():函数
- 返回值的类型  返回值的变量名  =  函数


## 占位符 %s
printf("hello, `%s`\n"`,` `answer`);
- %s：占位符
- answer:要替换占位符的变量
- `,`:区分第一个输入和第二个参数




