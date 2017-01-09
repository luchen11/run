# run
##把编译运行链接一起，使用一个命令<br>
支持c/c++/java语言 可以添加运行参数<br>
这个版本的必须要添加添加文件的后缀<br>
##eg:<br>
有一个C语言文件名叫test.c<br>
使用命令 

```
$ run -c test
```
Java与c++文件同理<br>

##注意 
编译Java的时候使用的是gcj编译器，<br>
这是GNU项目中的一个软件，用来把Java代码编译为二进制可执行代码，如果你的电脑中没有，请自行下载gcj<br>
Debian系列与Readhat系列分别使用如下的下载使用命令<br>

```
$ sudo ap-get install gcj

$ sudo yum install gjc
```

 
##另：该程序的c/c++编译器使用的是clang系列，<br>
clang可以在命令行自行下载，也可以更改本代码为gcc系列编译器<br>
更改本代码方法：将代码中的 f_cp函数内

```
cc="clang++ -std=c++11 -lpthread -lm  -Wall"
```
更改为

```
cc="g++ -std=c++11 -lpthread -lm  -Wall"
```

同理更改f_c的代码为

```
cc="gcc -std=c++11 -lpthread -lm  -Wall"

```

如果你本地的编译器不支持C++11或C11,请去掉

```
-std=c++11
-std=c11
```
这两个选项

##编译多个文件
改脚本支持编译多个文件，但要注意文件的顺序<br>
根据依赖关系，有依赖关系的文件放在后面。

##后言
这个脚本是我在学习Linux编程的时候编写的，当时是为了执行C代码的命令较短。<br>
该脚本计较适合做算法练习的同学使用，以及编写较小的程序。<br>
后来在电脑上一直使用这个脚本，即使换了Mac后，也一直在使用。<br>
希望有人能够喜欢，以及提出宝贵的意见与建议。<br>
如果你能star该项目，那将非常感谢！！
