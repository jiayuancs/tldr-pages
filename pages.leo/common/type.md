# type [modified]

> 显示shell将执行的命令类型。
> More information: <https://manned.org/type>.

- 命令类型：

```
外部命令: file
命令别名: alias
bash 内置命令: builtin
```

- 查看命令类型，如指定 -t 选项，则仅输出 file/alias/builtin 其中一个单词：

`type [-t] {{command}}`

- 显示所有包含名称为 command 的可执行文件的位置：

`type -a {{command}}`

- 返回命令的完整路径（仅有当命令是外部命令时有效）：

`type -p {{command}}`
