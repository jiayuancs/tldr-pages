# whereis [modified]

> Locate the binary, source, and manual page files for a command.
> More information: <https://manned.org/whereis>.

- 列出 whereis 会去查询的几个主要目录：

`whereis -l`

- 查询 ssh 相关文件：

`whereis {{ssh}}`

- 指定查询范围，b 为二进制文件，m 为 man 手册文件，s 为源文件，u 表示不是上述三类文件

`whereis -{{b|m|s|u}} {{ls}}`

