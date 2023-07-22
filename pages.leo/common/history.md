# history [modified]

> Command-line history.
> More information: <https://www.gnu.org/software/bash/manual/html_node/Bash-History-Builtins.html>.

- 显示当前 shell 所有历史命令：

`history`

- 只显示最近的 20 条历史命令 (in `zsh` it displays all commands starting from the 20th):

`history {{20}}`

- Clear the commands history list (only for current `bash` shell):

`history -c`

- 执行历史记录中的第 42 条命令：

`!42`
