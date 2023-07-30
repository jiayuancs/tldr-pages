# wc [modified]

> Count lines, words, and bytes.
> More information: <https://www.gnu.org/software/coreutils/wc>.

- 常用选项：

```
-l: 行数
-w: 单词(word)数
-m: 字符(character)数
-c: 字节(byte)数
```

- 从左到右依次输出行数、单词数、字符数：

`wc {{path/to/file}}`

- 统计行数：

`wc -l {{path/to/file}}`

