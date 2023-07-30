# tee [modified]

> 从 stdin 读数据，同时输出到指定文件和 stdout.
> More information: <https://www.gnu.org/software/coreutils/tee>.

- Copy standard input to each file, and also to standard output:

`echo "example" | tee {{path/to/file}}`

- 以追加([a]ppend)的方式将数据输出到文件：

`echo "example" | tee -a {{path/to/file}}`

- Print standard input to the terminal, and also pipe it into another program for further processing:

`echo "example" | tee {{/dev/tty}} | {{xargs printf "[%s]"}}`

- Create a directory called "example", count the number of characters in "example" and write "example" to the terminal:

`echo "example" | tee >(xargs mkdir) >(wc -c)`
