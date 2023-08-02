# bash [modified]

> Bourne-Again SHell, an `sh`-compatible command-line interpreter.
> See also: `zsh`, `histexpand` (history expansion).
> More information: <https://gnu.org/software/bash/>.

- 新开一个 shell 回话：

`bash`

- 新开一个 shell 回话，但不加载配置文件（~/.bashrc）：

`bash --norc`

- 执行指定命令：

`bash -c "{{echo 'bash is executed'}}"`

- 执行指定脚本：

`bash {{path/to/script.sh}}`

- 检查脚本是否存在语法问题：

`bash -n {{path/to/script.sh}}`

- 输出脚本的执行过程：

`bash -x {{path/to/script.sh}}`

