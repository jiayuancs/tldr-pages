# function [new] 

> function 用于在 shell 脚本中定义函数。函数定义需要在调用之前。


- 函数语法格式：

```
function {{function_name}}() {
    {{function_body}}
}
```

- 定义一个函数，函数内部可以使用 `$1`、`$2` 等变量来获取传递给函数的参数：

```
function hello() {
  echo "Hello ${$1}"
}
```

- 使用函数，就像使用命令一样，直接在函数名后传递参数：

`hello "world"`

