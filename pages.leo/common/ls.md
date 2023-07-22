# ls [modified]

> List directory contents.
> More information: <https://www.gnu.org/software/coreutils/ls>.

- List files one per line:

`ls -1`

- a 表示所有文件，h 表示以易读的方式显示文件大小，l 表示详细信息：

`ls -ahl`

- time 选项用于指定显示的时间类型，默认为 mtime；
- full-time 选项用于显示完整的时间：

`ls --time={{atime/ctime}} --full-time`

- 仅列出目录：

`ls -d`

- 列出 inode 号码：

`ls -i`

- 在文件名后添加特殊符号以标识文件类型；
- * 为可执行文件，/ 为目录，= 为 socket 文件，| 为 FIFO 文件：

`ls -F`
