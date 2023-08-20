# valgrind [modified]

> Wrapper for a set of expert tools for profiling, optimizing and debugging programs.
> Commonly used tools include `memcheck`, `cachegrind`, `callgrind`, `massif`, `helgrind`, and `drd`.
> More information: <http://www.valgrind.org>.

- 安装：

`sudo apt install valgrind`

- 使用默认的内存检查工具 Memcheck 来显示 `program` 的内存使用情况：

`valgrind {{program}}`

- Use Memcheck to report all possible memory leaks of `program` in full detail:

`valgrind --leak-check=full --show-leak-kinds=all {{program}}`

- Use the Cachegrind tool to profile and log CPU cache operations of `program`:

`valgrind --tool=cachegrind {{program}}`

- Use the Massif tool to profile and log heap memory and stack usage of `program`:

`valgrind --tool=massif --stacks=yes {{program}}`
