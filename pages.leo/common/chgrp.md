# chgrp [modified]

> Change group ownership of files and directories.
> More information: <https://www.gnu.org/software/coreutils/chgrp>.

- 改变文件所属组（chgrp 只能更改组，而 chown 既可更改所属用户又可更改组）：

`chgrp {{group}} {{path/to/file_or_directory}}`

- 递归改变文件所属组：

`chgrp -R {{group}} {{path/to/directory}}`

- h 选项改变符号链接文件本身的所属组（不更改其指向的文件所属组）：

`chgrp -h {{group}} {{path/to/symlink}}`

- Change the owner group of a file/directory to match a reference file:

`chgrp --reference={{path/to/reference_file}} {{path/to/file_or_directory}}`

