# tmux [modified]

> Terminal multiplexer. It allows multiple sessions with windows, panes, and more.
> See also `zellij` and `screen`.
> More information: <https://github.com/tmux/tmux>.

- Start a new session:

`tmux`

- 创建一个会话，并指定会话名称：

`tmux new -s {{name}}`

- 离开当前会话，让其后台运行：

`tmux detach   /  Ctrl-B d`

- 查看会话列表：

`tmux ls`

- 进入指定的会话：

`tmux attach -t {{name}}`

- 关闭指定会话：

`tmux kill-session -t {{name}}`
