# test [modified]

> Check file types and compare values.
> Returns 0 if the condition evaluates to true, 1 if it evaluates to false.
> More information: <https://www.gnu.org/software/coreutils/test>.

- 常用文件类型判断选项：

`test option {{path/to/file_or_directory}}`

```
option:
-e: 判断文件名是否存在
-f: 判断文件名是否存在且为普通文件
-d: 判断文件名是否存在且为目录
```

- 常用整数比较选项：

`test {{n1}} option {{n2}}`

```
option:
-eq: 等于
-ne: 不等于
-gt: 大于
-ge: 大于等于
-lt: 小于
-le: 小于等于
```

- 多重条件逻辑运算选项：

```
-a: 与
-o: 或
! : 非
```

- 字符串比较：

```
test -z string: 判断字符串是否为空
test -n string: 判断字符串是否非空，可省略 -n
test string1 == string2: 判断字符串是否相等
test string1 != string2: 判断字符串是否不相等
```

- 判断指定目录是否不存在：

`test ! -d "{{path/to/directory}}"`

- 使用变量时，一定要用双引号括起来，否则会报错：

`test "{{$variable}}" == "{{string}}"`

- If A is true, then do B, or C in the case of an error (notice that C may run even if A fails):

`test {{condition}} && {{echo "true"}} || {{echo "false"}}`

