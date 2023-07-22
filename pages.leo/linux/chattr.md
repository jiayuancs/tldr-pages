# chattr [modified]

> 修改文件或目录的隐藏属性，配套使用 `lsattr`.
> More information: <https://manned.org/chattr>.

- 增加 i 属性，让一个文件或目录不可被删除或更改，即使是超级用户：

`chattr +i {{path/to/file_or_directory}}`

- 删除 i 属性：

`chattr -i {{path/to/file_or_directory}}`

- 递归地添加 i 属性：

`chattr -R +i {{path/to/directory}}`

- 常用属性：

```
A: 在存取文件或目录时不更改其 atime
a: 只能增加数据，不能删除或修改数据（仅 root 可设置）
i: 什么都不能变（仅 root 可设置）
```
