# grep [modified]

> Find patterns in files using regular expressions.
> More information: <https://www.gnu.org/software/grep/manual/grep.html>.

- 命令格式：

`grep '正则' [路径] [选项]`

- 常用选项：

```
-r: 递归
-i: 忽略大小写
-n: 输出行号
-v: 排除匹配
-E: 使用扩展正则表达式
-o: 仅显示匹配的字符串本身，而不是输出整行
-w: 仅显示完整匹配的单词
-c: 统计匹配的行数
--color=auto: 匹配的地方高亮（默认 grep 是 grep --color=auto 的别名）
```

- 搜索非空行：

`grep '{{^$}}' {{file}} -nv`

- 输出非空行和非#开头的行

`grep '{{(^$)|(^#)}}' {{file}} -nvE`

