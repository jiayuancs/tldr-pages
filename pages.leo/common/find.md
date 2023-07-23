# find [modified]

> Find files or directories under the given directory tree, recursively.
> More information: <https://manned.org/find>.

- 命令格式：

`find {{root_path}} 选项 参数`

- 常用选项

```
-name: 匹配文件名，可使用通配符 *,?
-iname: 忽略大小写的文件名
-path: 匹配路径
-user/group: 指定用户/用户组
-type: 文件类型，可以为 f,d,l,c,b,p,s
-mtime: 修改时间范围，默认单位为天
-size: 文件大小范围，常用单位有 k,M,G
-nouser/nogroup: 查找没有属主/组的文件
-maxdepth: 最大搜索深度
-mindepth: 最小搜索深度
-exec: 将搜索结果传给其他命令，不进行交互
-ok: 将搜索结果传给其他命令，可进行交互
```

- 范围字段

```
-n: 表示[0, n-1]
 n：表示(n-1, n]
+n: 表示(n, +INF)
```

- 搜索指定后缀名的普通文件，多个条件之间进行 and 运算：

`find {{/etc/nginx}} -name '{{*.conf}}' -type f`

- 使用逻辑运算选项（常用的有 -or, -not），可使用括号运算符（需转义）：

`find {{root_path}} -path '{{**/path/**/*.ext}}' -or \( -name '{{*pattern*}}' \)`

- 搜索文件大小为 (3M, +INF) 的文件，且所属用户不是 root:

`find {{/bin/}} -size {{+3M}} -not -user root`

- 搜索最近 [0, 6] 天内修改的文件：

`find {{/etc/}} -mtime {{-7}}`

- 搜索无主冤魂：

`find {{/}} -nouser`

- 将搜索结果传给其他命令：

`find {{/home/}} -type {{l}} -exec {{ls -l {} }} \;`

- 使用 grep 风格的扩展正则表达式（如不指定 regextype，则为基本正则表达式）；
- 注意：正则表达式必须要匹配完整的文件路径，因此通常以 .* 开头：

`find {{/home/}} -regextype '{{posix-egrep}}' -regex '{{.*(main|foo)\.cpp$}}'`

