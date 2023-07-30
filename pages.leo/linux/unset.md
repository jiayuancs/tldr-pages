# unset [modified]

> Remove shell variables or functions.
> More information: <https://manned.org/unset>.

- 取消变量 foo，如果变量 foo 不存在，则取消函数 foo:

`unset {{foo}}`

- 取消变量([v]ariable) foo 和 bar:

`unset -v {{foo}} {{bar}}`

- 取消函数([f]unction) my_func:

`unset -f {{my_func}}`
