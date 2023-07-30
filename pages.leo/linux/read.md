# read [modified]

> Shell builtin for retrieving data from `stdin`.
> More information: <https://manned.org/read.1p>.

- 从键盘读取数据存到变量 variable 中，-p 用于指定提示字符串，
- -t 用于指定超时时间，单位为秒：

`read -p '{{input a value: }}' -t {{10}} {{variable}}`

- Store each of the next lines you enter as values of an array:

`read -a {{array}}`

- 指定最多读取几个字符：

`read -n {{character_count}} {{variable}}`

- Use a specific character as a delimiter instead of a new line:

`read -d {{new_delimiter}} {{variable}}`

- Do not let backslash (\\) act as an escape character:

`read -r {{variable}}`

- Do not echo typed characters (silent mode):

`read -s {{variable}}`

- Read `stdin` and perform an action on every line:

`while read line; do echo "$line"; done`
