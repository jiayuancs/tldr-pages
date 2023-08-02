# shift [modified]

> Shell built-in command that shifts the arguments passed to the calling function or script by a specified number of places.
> shift 命令通常用于 shell 脚本中，用于移动参数位置，以便于处理参数列表。
> More information: <https://www.gnu.org/software/bash/manual/bash.html#index-shift>.

- 丢弃第一个参数，将第二个参数移至第一个参数的位置，以此类推：

`shift`

- 丢弃前 N 个参数，将第 N+1 个参数移至第一个参数的位置，以此类推：

`shift {{N}}`
