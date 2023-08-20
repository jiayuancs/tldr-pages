# g++ [modified]

> Compiles C++ source files.
> Part of GCC (GNU Compiler Collection).
> More information: <https://gcc.gnu.org>.

- 常用选项：

```
-o: 指定输出文件名
-g: 生成调试信息
-std=c++17: 指定 C++17 标准
-Wall: 显示常见警告
-I: 指定头文件路径
-L: 指定库文件路径
-l: 指定库文件名
-fPIC: 生成位置无关的代码
-shared: 生成动态链接库
-D: 定义宏

分阶段：
  -E: 只预处理，不编译，得到 .i 文件
  -S: 只编译，不汇编，得到 .s 文件
  -c: 只汇编，不链接，得到 .o 文件
  无: 链接，生成可执行文件
```

- Choose a language standard to compile for (C++98/C++11/C++14/C++17):

`g++ {{path/to/source.cpp}} -std={{c++98|c++11|c++14|c++17}} -o {{path/to/output_executable}}`

- Include libraries located at a different path than the source file:

`g++ {{path/to/source.cpp}} -o {{path/to/output_executable}} -I{{path/to/header}} -L{{path/to/library}} -l{{library_name}}`

- Compile and link multiple source code files into an executable binary:

`g++ -c {{path/to/source_1.cpp path/to/source_2.cpp ...}} && g++ -o {{path/to/output_executable}} {{path/to/source_1.o path/to/source_2.o ...}}`

- 制作动态库：

`g++ -c {{path/to/source.cpp}} -fPIC && g++ -shared -o {{path/to/libname.so}} {{path/to/source.o}}`

- 制作静态库：

`g++ -c {{path/to/source.cpp}} && ar rcs {{path/to/libname.a}} {{path/to/source.o}}`

