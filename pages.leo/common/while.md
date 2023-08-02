# while [modified]

> Simple shell loop.
> More information: <https://manned.org/while>.

- 语法格式，当条件成立时执行循环：

```
while {{condition_command}}; do
  {{command_block}}
done
```

- Read `stdin` and perform an action on every line:

`while read line; do echo "$line"; done`

- Execute a command forever once every second:

`while :; do {{command}}; sleep 1; done`
