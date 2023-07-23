# sed [modified]

> Edit text in a scriptable manner.
> See also: `awk`, `ed`.
> More information: <https://www.gnu.org/software/sed/manual/sed.html>.

- 命令格式：

`sed [选项] [sed内置命令字符] [输入文件]`

- 常用选项：

```
-n: 取消 sed 的默认输出( sed 默认输出不匹配的内容)，常与内置命令 p 一起使用
-i: 直接将结果写入原文件，而不输出到控制台，不用 -i 则修改的仅是内存数据
-e: 多次编辑
-r: 支持扩展正则表达式
```

- 常用命令字符：

```
a: append，在指定行后添加一行/多行文本
d: delete，删除匹配行
i: insert，在指定行前插入一行/多行文本
p: print，打印匹配行的内容，通常与 -n 选项一起使用
s/正则/替换内容/g: 匹配正则内容，然后替换内容，g 表示全局替换
```

- 匹配范围：

```
'':  匹配所有行
'n': 匹配第 n 行
/pattern/: 与模式 pattern 匹配的每一行
范围区间: 'n,m' 表示 [n,m]，n,+m 表示 [n,n+m]
步长: n~m 表示从 n 开始，步长为 m，即：n,n+m,n+2m,...
```

- 输出以 hello 结尾的行：

`sed -n '{{/hello$/p}}' {{path/to/file}}`

- 输出 [2, 5] 行的内容：

`sed -n '{{2,+3p}}' {{path/to/file}}`

- 将 apple 替换为 mango，并写回到文件中：

`sed -i '{{s/apple/mango/g}}' {{path/to/file}}`

- 删除以 # 开头的行，并写回到文件中：

`sed -i '{{/^#/d}}' {{path/to/file}}`

- 在第 2 行下面添加一行 "Hello world"，并写回到文件中：

`sed -i '{{2a Hello world}}' {{path/to/file}}`

