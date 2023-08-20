# rar [modified]

> The RAR archiver. Supports multi-volume archives that can be optionally self-extracting.
> More information: <https://manned.org/rar>.

- 安装：

`sudo apt install rar`

- 压缩文件：

`rar a {{path/to/archive_name.rar}} {{path/to/file1}} {{path/to/file2}} {{path/to/file3}}`

- 压缩目录：

`rar a -r {{path/to/archive_name.rar}} {{path/to/directory}}`

- 解压到当前目录（也可以使用 unrar 命令，用法相同）：

`rar x {{path/to/archive_name.rar}}`

- 解压到指定目录（目录必须存在），
- （也可以使用 unrar 命令，用法相同）：

`rar x {{path/to/archive_name.rar}} {{path/to/directory}}`
