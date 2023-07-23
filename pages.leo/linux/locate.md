# locate [modified]

> Find filenames quickly.
> More information: <https://manned.org/locate>.

- 常用选项

```
-c: 统计匹配到的条目数量
-i: 忽略大小写
-n: 最多显示多少行
-r: 标准正则表达式
--regex 扩展正则表达式
```

- Ubuntu 安装该程序：

`sudo apt install mlocate`

- 更新索引数据库：

`sudo updatedb`

- 在数据库中搜索，如果没有使用通配符(globbing characters)，则默认匹配 `*pattern*`：

`locate {{pattern}}`

- 使用扩展正则表达式，搜索 foo.cpp 和 main.cpp 文件

`locate --regex '{{(foo|main)\.cpp$}}'`

