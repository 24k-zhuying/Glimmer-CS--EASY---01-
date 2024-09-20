# 第一个程序

1. 高级计算机语言与低级计算机语言，各有什么优劣，你更喜欢哪一类计算机语言？

答：==高级语言开发效率高，易于理解，并方便在各种平台上运行，但其执行效率较低且对硬件控制能力有限。==

​	==低级语言执行效率高，对硬件的控制能力强，但其难以学习和使用，配置各种环境较繁琐可移植性差。==

2. 尝试解读`hello.c`中每一行的内容。

答：==第一行引用头文件，第三行定义main函数，第四行打印“Hello，world”， 第五行返回0。==

3. 删去该程序的哪一行不会影响运行结果？

答:==第5行。==

4. int类型是计算机存储什么元素的方式？为什么main函数要使用int进行声明/定义？

答：==整形数，main函数返回值0是一个整数==

5. 请调整上述程序的内容，使其输出内容改为`Hello gilmmer!`并附上运行截图

```c
#include <stdio.h>

int main() {
    printf("Hello gilmmer!");
    return 0;
}
```

[![QQ20240918-231826](C:\Users\ASUS\Pictures\QQ20240918-231826.png)](https://github.com/24k-zhuying/Glimmer-CS--EASY---01-/blob/main/QQ20240918-231826.png)

# 基础语法运用

```c
#include <stdio.h>

int main() {
    int code;
    printf("Show me your code,please.\n");

    while( 1 ){
        scanf("%d",&code);
        if(code >= 100000 && code <= 999999){
            printf("I am super hacker!\n");

            return 0;
        }
        else {
            printf("Fake code!\n");
        }
    }
    return 0;
}

```

## 课后题

```
/*在说明文档之外，请提交一份C语言代码，要求编译后的程序实现输入两个整数m,n，输出它们的最大公约数。其中0<m,n<2^31*/

#include <stdio.h>

int main() {
   int m, n;
   int t;

   printf("请分别输入m与n的值\n");
   scanf("%d %d", &m, &n);

    while( m % n )//当m%n等于0时跳出循环
    {   
        t = m % n;
        m = n;
        n = t;
    }
        printf("最大公约数为%d\n", n);
    return 0;//辗转相除法
}


```



