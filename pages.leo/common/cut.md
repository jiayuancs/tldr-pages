# cut [modified]

> Cut out fields from `stdin` or files.
> More information: <https://www.gnu.org/software/coreutils/cut>.

- 常用选项：

```
-d: 指定分隔字符，常与 -f 连用
-f: 根据 -d 指定的字符将一行数据划分为多段，-f 用于指定取出第几段（从 1 开始）
-c: 指定字符区间，区间含义如下：
    -n  表示 [1,n]
    n   表示 n
    n-  表示 [n, +INF)
    n-m 表示 [n, m]
```

- 输出环境变量信息，使用 cut 截取每行第 12 个字符及之后的内容：

`{{export}} | cut -c {{12-}}`

- 输出 PATH 环境变量中的第 5 个和第 7 个路径：

`{{echo $PATH}} | cut -d '{{:}}' -f '{{5,7}}'`

