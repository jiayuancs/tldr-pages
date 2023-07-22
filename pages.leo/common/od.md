# od [modified]

> Display file contents in octal, decimal or hexadecimal format.
> Optionally display the byte offsets and/or printable representation for each line.
> More information: <https://www.gnu.org/software/coreutils/od>.

- 查看 "hello" 每个字符的 ASCII 值，x 表示十六进制：

`echo hello | od -t xCc`

- 常用格式：

`od -t [type] file`

- 其中 [type] 可为：

```
a：使用默认的字符输出
c：使用ASCII字符输出
d[size]：十进制(decimal)
f[size]：浮点数值(float)
o[size]：八进制(octal)
x[size]：十六进制(hex)
```


- 其中 size 可为：

```
C: sizeof(char)
S: sizeof(short)
I: sizeof(int)
L: sizeof(long)
D: sizeof(double)
```
