---
Title: CS50 Week1 - C
Labels: 随笔
Keywords:  CS50
Date: 2026-06-08
---

```mermaid
flowchart LR
A[source code] --> B[compiler编译器]
B --> C[machine code]
```
---



# Visual Studio Code
`https://cs50.dev/`
- GUI:graphical user interface"图形用户界面"
- CLI:command-line interface"命令行界面"
---



# Hello world
## 创建文件
`$ code hello.c`    
用 VS Code 打开（或创建）一个名为 hello.c 的文件  


## 编写代码
```
#include <stdio.h>

int main(void)
{
    printf("hello, world\n");
}
```


## 编译代码
`make hello`  
hello.c → 你写的源代码  
hello → 编译后生成的可执行程序  
把源代码编译成机器代码,生成一个叫做hello的新文件


## 运行程序
./hello  
`./`进入当前文件夹

> [!WARNING]
> 注意是`/`



> [!NOTE]
> 📌本节命令总结  
> `code hello.c`    # 创建或打开 hello.c  
> `make hello`      # 编译程序  
> `./hello`         # 运行程序  
---


# 代码释义
`printf("hello, world\n");`
- `printf()`   格式化打印输出
- `hello, world`   要打印的内容
- `""`    打印的开始、结束位置
- `\n`    换行(转义序列，为了美观)
- `;`    结束语句  



类似于数学中的函数表示法f(x)
```mermaid
flowchart LR
A[arguments 参数] --> B[function 函数]
B --> C[side effects 副作用]
```
---



# 常见错误
清空终端窗口：`Ctrl+L`或者输入`clear`  

## 假设代码最后忘记写`;`结束
```
1 #include <stdio.h>
2
3 int main(void)
4 {
5     printf("hello, world\n")
6 }
```

使用`make hello`来编译时，会报错如下：  
```
hello.c:5:29: error: expected ';' after expression
    5 |    printf("hello, world\n")
      |                            ^
      |                            ;
1 error generated.make: *** [<builtin>: hello] Error 1
```

- `hello.c`  出错的文件名
- `5`    问题出现在第五行
- `29`    从左到右第29个字符
- `error: expected ';' after expression`    表达式后面应该有个分号
- `^`    指向出错的位置



## 忘记写 #include <stdio.h>
```
1 int main(void)
2 {
3     printf("hello, world\n");
4 }
```

忘记写 #include <stdio.h>时，会出现以下报错：
```
hello.c:3:5: error: call to undeclared library function 'printf' with type 'int (const char *, ...)'; ISO C99 and later do not support implicit function declarations [-Wimplicit-function-declaration]
    3 |     printf("hello, world\n");
      |     ^
hello.c:3:5: note: include the header <stdio.h> or explicitly provide a declaration for 'printf'
1 error generated.
make: *** [<builtin>: hello] Error 1
```
- error: call to undeclared library function 'printf' with type 'int    # 调用了未声明的函数，返回了Int类型



# header files 头文件
以.h结尾，而非以.c结尾的文件。  
这些头文件中包含别人已写好的代码，供你在自己的程序中使用。  
同理，`printf`是C语言的一个功能特性，但如果想使用它，需要包含相应的库，具体就是`让程序包含定义了该函数的头文件`————`stdio.h`  

> [[!WARNING]]
> 不要把`stdio.h`写成`studio.h`  
> standardio.h


由上可知`#include <stdio.h>`的作用是：  
告诉编译器，我并没有写所有要用的代码，请从`standardio.h`这个文件里引入`printf`的定义。


> [!IMPORTANT]
> 查找C语言内容的传统方法：查阅官方`技术手册`页，简称`Manual Pages`  
> `manual.cs50.io`
