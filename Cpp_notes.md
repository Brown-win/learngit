# C++基础入门学习笔记一



# 一、C++基础概念

### 1.打出第一个程序

编写一个C++程序的步骤如下：

- 创建文件
- 编写代码
- 编译
- 运行

```c++
#include <iostream>
using namespace std;
int main()
{
    cout << "Welcome to C++!" << endl;
    return 0;
}
```



运行结果：

![初学C++](D:\Desktop\makedown 笔记\初学C++.jpg)

------



### 2.注释

#### (1)用//

例如：

```c++
//这是注释
```



#### (2)用 /*      */ 包围

例如：

```c++
/*
这是注释
但是用两行来写
*/
```

注意：注释在程序中不会被运行出来！

----

### 3.变量和常量

#### (1)变量

```c++
int a = 10;  //定义变量
cout << "a = " << endl;  //输出变量
```

#### (2)常量

- `#define ` 宏常量

  ```c++
  #define Day 7   //Day 是常量
  cout << "一周共有： " << Day << "天" << endl;
  ```

  

- `const` 修饰的变量

  ```c++
  const int month = 12;
  cout << "一年共有" << month << "个月份" << endl;
  ```

  

  -----

  

### 4.关键字

记住：系统已使用的单词不能用作变量名和常量名！

----

### 5.标识符

- 标识符不能是关键字
- 标识符只能由字母、数字、下划线组成
- 第一个字符必须为字母或下划线（第一个字符不能是数字） 
- 标识符中字母区分大小写

----

## 二、数据类型

### 1.整型 

- 短整型 (-32768~32767)（2字节） 
  `short num1 = 10;`
- 整型（4个字节） 
  `int num2 = 10;`
- 长整型（4个字节） 
  `long num3 = 10;`
- 长长整型（8个字节） 
  `long long num4 = 10;`

----

### 2.`sizeof`关键字

用来求内存空间

用法：sizeof()  括号内可以放数据类型也可以存放变量

```c++
short num1 = 10;  //示例 
cout <<"short占用的内存空间为："<< sizeof (short) <<endl; 
	
int num2 = 20;   //示例
cout <<"int占用的内存空间为："<< sizeof (int) <<endl; 
```

运行结果：

![sizeof](D:\Desktop\makedown 笔记\sizeof.jpg)

----

### 3.实型（浮点型）

#### (1)单精度 float（4个字节）

`float f1 = 3.14f;     //加一个f令它为单精度
	cout << "f1 = " << f1 << endl; `

#### (2)双精度double（8个字节）

`double f2 = 3.14159256;
cout << "f2 = " << f2 << endl; `



- 各自统计一下float和double的内存空间：

```c++
cout << "float占用的内存空间为：" << sizeof(float) <<endl; 
cout << "double占用的内存空间为：" << sizeof(double) <<endl; 
```

运行结果：

![sizeof](D:\Desktop\makedown 笔记\sizeof2.jpg)



- 一点小知识：科学计数法

```c++
//科学计数法 
float f3 = 3e2;   //3 * 10 ^ 2
cout << "f3 = " << f3 << endl;

float f4 = 3e-2;   //3 * 10 ^ -2
cout << "f4 = " << f4 << endl; 
```

运行结果：

![科学计数法](D:\Desktop\makedown 笔记\科学计数法.jpg)

---

### 4.字符型

char ch = "a";  

注意：不能用双引号，单引号内只能有一个字符	

```c++
char ch = 'a'; 
cout << ch << endl; 
```



- 小知识：求字符型对应的ASCII编码

```c++
cout << (int)ch << endl;  
cout << "a对应的ASCII编码为 " << (int)ch << endl;
```

运行结果：

![ASCII](D:\Desktop\makedown 笔记\ASCII编码.jpg)

----

### 5.转义字符

| 转义字符 |        含义        |
| :------: | :----------------: |
|    \a    |        警报        |
|    \n    |        换行        |
|    \t    | 水平制表（一个Tab) |
|   \\\\   | 代表一个反斜号“/"  |

 ....

---

### 6.字符串型

#### (1)C风格字符串

```c
char str[] = "hello world";  //c风格 
cout  << str << endl;
```

#### (2)C++风格字符串

注意：开头需要加入头文集：#include <string>

```c++
string str2 = "hello world";
cout  << str2 << endl; 
```

---

### 7.布尔数据类型

- true--真--1 , 非0的值代表真 
- false--假--0

```c++
//（1）创建bool数据类型
bool flag = true; 
cout << flag << endl; 

flag = false ;
cout << flag << endl;

//（2）查看bool类型所占的空间
cout << "bool类型所占的内存空间为： " << sizeof (flag) << endl; 
```

运行结果：

![bool](D:\Desktop\makedown 笔记\布尔类型.jpg)

---

### 8.数据的输入

```c++
int h = 0;
cout << "请给整型变量h赋值：" << endl;
cin >> h;
cout << "变量h的值为：" << h << endl; 
```

- `cin`是令用户从键盘中键入

---



*笔记一 告一段落了*