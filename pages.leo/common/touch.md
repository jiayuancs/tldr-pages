# touch [modified]

> Create files and set access/modification times.
> More information: <https://manned.org/man/freebsd-13.1/touch>.

- 创建文件：

`touch {{path/to/file1 path/to/file2 ...}}`

- 时间类型：

```
mtime(modification time): 修改文件内容时更新
atime(access time): 读取文件时更新
ctime(status time): 文件权限与属性改变时更新（touch无法修改此时间）
```

- 设置 [a]time 或 [m]time 为当前时间，如不指定，则默认同时修改这两个；
- don't create file if it doesn't exist:

`touch -c -{{a|m}} {{path/to/file1 path/to/file2 ...}}`

- 使用 t 选项指定时间：
- don't [c]reate file if it doesn't exist:

`touch -c -t {{YYYYMMDDHHMM.SS}} {{path/to/file1 path/to/file2 ...}}`

- 使用 r(reference) 选项指定一个文件，将其他文件的时间设置为该文件的时间（atime or mtime），
- don't [c]reate file if it doesn't exist:

`touch -c -r {{base_file}} {{path/to/file1 path/to/file2 ...}}`
