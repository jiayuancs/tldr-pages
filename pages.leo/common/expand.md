# expand [modified]

> Convert tabs to spaces.
> More information: <https://www.gnu.org/software/coreutils/expand>.

- 将文件中的 Tab 字符转换为 8 个空格字符，输出到 stdout:

`expand {{path/to/file}}`

- -t 选项指定 Tab 字符转换为的空格数量：

`expand -t={{number}} {{path/to/file}}`

