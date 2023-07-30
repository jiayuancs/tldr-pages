# paste [modified]

> Merge lines of files.
> More information: <https://www.gnu.org/software/coreutils/paste>.

- 将两个文件中的行与行合并到一起，默认使用 TAB 分隔：

`paste {{file1}} {{file2}}`

- -d 选项指定合并时使用的分隔符：

`paste -d {{delimiter}} {{file1}} {{file2}}`

- -s 选项表示将文件中的所有行合并为单行([s]ingle line)，默认使用 TAB 分隔：

`paste -s {{path/to/file}}`

