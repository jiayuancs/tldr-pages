# if [modified]

> Performs conditional processing in shell scripts.
> See also: `test`, `[`.
> More information: <https://www.gnu.org/software/bash/manual/bash.html#Conditional-Constructs>.


- 语法格式，其中 elif 和 else 分支可省略：

```
if {{condition_command}} ; then
  {{command_block}}
elif {{condition_command}} ; then
  {{command_block}}
else
  {{command_block}}
fi
```

- 举例：

`if ! [ -d "{{$directory}}" ]; then {{echo "Condition is true"}}; fi`

- List all possible conditions (`test` is an alias to `[`; both are commonly used with `if`):

`man [`

