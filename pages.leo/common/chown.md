# chown [modified]

> Change user and group ownership of files and directories.
> More information: <https://www.gnu.org/software/coreutils/chown>.

- 改变所属用户和用户组：

`chown {{user}}:{{group}} {{path/to/file_or_directory}}`

- 递归改变所有者：

`chown -R {{user}} {{path/to/directory}}`

- h 选项改变符号链接文件本身的所有者（不更改其指向的文件所有者）：

`chown -h {{user}} {{path/to/symlink}}`

- Change the owner of a file/directory to match a reference file:

`chown --reference={{path/to/reference_file}} {{path/to/file_or_directory}}`

