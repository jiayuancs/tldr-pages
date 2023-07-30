# uniq [modified]

> Output the unique lines from the given input or file.
> Since it does not detect repeated lines unless they are adjacent, we need to sort them first.
> More information: <https://www.gnu.org/software/coreutils/uniq>.

- 常用选项：

```
-i: 忽略大小写
-c: 统计每项出现的次数
-u: 仅显示不重复的行
-d: 仅显示重复的行
```

- 忽略掉重复的行（对于重复的行，仅显示其中一行）：

`sort {{path/to/file}} | uniq`

- 仅显示不重复的行：

`sort {{path/to/file}} | uniq -u`

- 仅显示重复的行：

`sort {{path/to/file}} | uniq -d`

- 统计各行数显的次数：

`sort {{path/to/file}} | uniq -c`

- 按出现次数从大到小排序：

`sort {{path/to/file}} | uniq -c | sort -nr`
