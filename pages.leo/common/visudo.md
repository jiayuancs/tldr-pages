# visudo [modified]

> Safely edit the sudoers file.
> More information: <https://www.sudo.ws/docs/man/visudo.man>.

- Edit the sudoers file:

`sudo visudo`

- 检查 /etc/sudoers 文件是否存在语法错误：

`sudo visudo -c`

- 使用指定的编辑器编辑 /etc/sudoers 文件：

`sudo EDITOR={{vim}} visudo`
