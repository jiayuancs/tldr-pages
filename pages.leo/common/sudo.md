# sudo [modified]

> Executes a single command as the superuser or another user.
> More information: <https://www.sudo.ws/sudo.html>.

- Run a command as the superuser:

`sudo {{command}}`

- 使用默认编辑器编辑文件，编辑器由环境变量 SUDO_EDITOR, VISUAL, EDITOR 依次指出：

`sudo --edit {{/etc/fstab}}`

- -E 选项保留当前用户已存在的环境变量：

`sudo -E {{visudo}}`

- 使用 `sudo` 重复执行上条命令 (only in `bash`, `zsh`, etc.):

`sudo !!`

