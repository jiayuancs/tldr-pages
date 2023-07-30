# xargs [modified]

> Execute a command with piped arguments coming from another command, a file, etc.
> The input is treated as a single block of text and split into separate pieces on spaces, tabs, newlines and end-of-file.
> More information: <https://pubs.opengroup.org/onlinepubs/9699919799/utilities/xargs.html>.

- 常用选项：

```
-d: 指定分隔符，默认为空格
-p: 询问用户是否执行相应的命令
-t: 显示将要执行的命令
-E: 指定终止标志字符串，xargs 分析到含有这个标志的时候就停止，不能与 -d 连用
-n: 每次执行命令使用多少个参数，默认是所有
-L: 从标准输入一次读取多少行作为命令参数
-I: 指定一个占位符，将参数一行行地传给后面的占位符
-0: 用于指定输入数据的字段分隔符为 null 字符，通常与 find 命令一起使用，确保 find 命令
    使用的 null 字符能够正确地被 xargs 命令处理
```

- 将所有参数一次性传递给后面的命令：

`{{arguments_source}} | xargs {{command}}`

- 删除当前目录下所有以 .backup 为后缀的文件，-print0 选项使用 null 字符分隔文件名：

`find . -name {{'*.backup'}} -print0 | xargs -0 rm -v`

- 指定占位符为 _，将参数一行行地替换掉命令后面的 _ 占位符：

`{{arguments_source}} | xargs -I _ {{command}} _ {{optional_extra_arguments}}`

- 并行执行，使用 -P 指定最大进程数量，默认为 1，如指定为 0，则使用尽可能多的进程数量：

`{{arguments_source}} | xargs -P {{max-procs}} {{command}}`

