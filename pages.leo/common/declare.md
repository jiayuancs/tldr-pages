# declare [modified]

> Declare variables and give them attributes.
> More information: <https://www.gnu.org/software/bash/manual/bash.html#Bash-Builtins>.

- 常用选项

```
-p: 查看变量的值和属性
```

- 常用属性，在属性字符前使用 - 表示设置属性，使用 + 表示取消设置属性：

```
a: array，数组
A: associative array，关联数组（键值对）
i: integer，整数
r: readonly，只读
x: export，导出为环境变量
```

- Declare a string variable with the specified value:

`declare {{variable}}="{{value}}"`

- Declare an integer variable with the specified value:

`declare -i {{variable}}="{{value}}"`

- Declare an array variable with the specified value:

`declare -a {{variable}}=({{item_a item_b item_c}})`

- Declare an associative array variable with the specified value:

`declare -A {{variable}}=({{[key_a]=item_a [key_b]=item_b [key_c]=item_c}})`

- Declare a readonly string variable with the specified value:

`declare -r {{variable}}="{{value}}"`

- Declare a global variable within a function with the specified value:

`declare -g {{variable}}="{{value}}"`
