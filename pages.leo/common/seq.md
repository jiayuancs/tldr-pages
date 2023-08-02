# seq [modified]

> Output a sequence of numbers to `stdout`.
> More information: <https://www.gnu.org/software/coreutils/seq>.

- 从 1 输出到 10：

`seq 10`

- :从 5 输出到 20，每次增量为 3：

`seq 5 3 20`

- 使用空格作为分隔符：

`seq -s " " 5 3 20`

- 格式化输出，用 0 补齐为 4 位数字：

`seq -f "%04g" 5 3 20`
