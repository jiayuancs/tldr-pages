# su [modified]

> Switch shell to another user.
> More information: <https://manned.org/su>.

- Switch to superuser (不推荐，很多环境变量未变更):

`su`

- Switch to a given user (不推荐，很多环境变量未变更):

`su {{username}}`

- Switch to a given user and simulate a full login shell (推荐):

`su - {{username}}`

- Execute a command as another user:

`su - {{username}} -c '{{command}}'`
