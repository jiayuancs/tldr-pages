# sort [modified]

> Sort lines of text files.
> More information: <https://www.gnu.org/software/coreutils/sort>.

- 常用选项：

```
-f: 忽略大小写
-b: 忽略最前面的空格字符
-M: 以月份的名字来排序，例如 JAN, DEC 等
-n: 使用纯数字进行排序
-r: 反向排序
-u: 去除重复的行
-o: 将结果写到指定的文件中
-t: 指定分隔符号，将一行文本分隔为若干字段(field)
-k: 按照哪个字段(field)进行排序
```

- -k 选项指定的排序字段常用格式：

```
2.3      从第 2 个字段的第 3 个字符开始到行尾结束
2.3,4.2  从第 2 个字段的第 3 个字符开始到第 4 个字段的第 2 个字符结束
3        按 [3, +INF) 字段排序
3,3      只按第 3 个字段排序
3,6      按 [3, 6] 字段排序
3,3nr    使用纯数字(n)的方法，按第 3 个字段进行逆序(r)排序
```

- 按照第 3 个字段对 /etc/passwd 中的行进行排序，n 用于指定使用数字进行排序：

`sort -t={{:}} -k={{3,3n}} {{/etc/passwd}}`

- 按照第 3 个字段排序，如果相等则按照第 6 个字段排序：

`sort -t={{:}} -k={{3,3n}} -k{{6,6}} {{/etc/passwd}}`
