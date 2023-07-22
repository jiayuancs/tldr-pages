# mv [modified]

> Move or rename files and directories.
> More information: <https://www.gnu.org/software/coreutils/mv>.

- 重命名/移动文件，当移动文件时，可以有多个源文件：

`mv {{path/to/source}} {{path/to/target}}`

- 覆盖已存在的文件前不进行提示：

`mv -f {{path/to/source}} {{path/to/target}}`

- 在覆盖现有文件之前提示确认，无论文件权限如何：

`mv -i {{path/to/source}} {{path/to/target}}`

- 不覆盖目标上的现有文件：

`mv -n {{path/to/source}} {{path/to/target}}`

- 显示移动后的文件：

`mv -v {{path/to/source}} {{path/to/target}}`
