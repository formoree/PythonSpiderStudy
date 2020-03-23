## pyhton简单文本操作

#### 文本创建
##### Step 1
```
file = open("name.txt","w+")
```
  * 声明f变量来打开一个名字为name，类型为w+的文本文件。Open具有两个参数，我们要打开的文件以及我们像对文件执行的操作或者是操作类型的字符串。
  * “w”指示写和+。如果库中不存在文件，则将创建他
  * “w”旁边可用选项“r”（读），“a”（附加和加号）

##### Step 2 
```
for i in range(10):
    f.write("This is line %d\r\n"%(i+1))
``` 
* 在for循环中通过write函数输入到文件中
* 输出这是行号 %d显示整数 
* ‘\r’是回车，’\n’是换行，前者使光标到行首，后者使光标下移一格。通常用的Enter是两个加起来。
  
##### Step 3
```
f.close()
```
* 这将关闭存储的文件的实例

#### 文件附加
```
//Step 1 
f = open("name.text","a+")

//Step 2
for i in range (2):
    f.write("Appended line %d\r\n"%(i+1))

```

#### 文件读取
```
//Step 1
f=open("name.txt","r") //"r"阅读模式

//Step 2
if f.mode == 'r'//mode函数检查文件是否处于打开模式

//Step 3
contents = f.read()
print(contents)
```

#### 逐行读取文件
```
f1 = f.readlines()
for x in f1:
    print(x)
```

![]( \Snipaste_1.png)
