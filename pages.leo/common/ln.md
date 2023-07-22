# ln [modified]

> Creates links to files and directories.
> More information: <https://www.gnu.org/software/coreutils/ln>.

- 创建符号链接：

`ln -s {{/path/to/file_or_directory}} {{path/to/symlink}}`

- f 表示强制覆盖已存在的文件：

`ln -sf {{/path/to/new_file}} {{path/to/symlink}}`

- 创建硬链接：

`ln {{/path/to/file}} {{path/to/hardlink}}`

