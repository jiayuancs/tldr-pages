# rm [modified]

> Remove files or directories.
> See also: `rmdir`.
> More information: <https://www.gnu.org/software/coreutils/rm>.

- Remove specific files:

`rm {{path/to/file1 path/to/file2 ...}}`

- r 表示递归；f 表示强制，不输出警告信息：

`rm -rf {{path/to/file1 path/to/file2 ...}}`

- v 表示输出被删除的文件名：

`rm -rfv {{path/to/file1 path/to/file2 ...}}`

- i 表示对每个文件都询问是否删除；I 则仅在删除三个以上文件之前，
- 或使用递归选项（r）时询问一次

`-i / -I`

