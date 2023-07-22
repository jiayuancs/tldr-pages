# umask [modified]

> Manage the read/write/execute permissions that are masked out (i.e. restricted) for newly created files by the user.
> More information: <https://manned.org/umask>.

- 用户创建的文件默认具有如下权限（掩码前）；
- （下面的权限还需去除 umask 中定义的权限，从而得到最终的权限）：

```
文件：-rw-rw-rw-
目录：drwxrwxrwx
```

- 显示当前的权限掩码：

`umask`

- 以字符的形式显示当前的权限掩码，显示的是 rwxrwxrwx - mask 的结果，即最多具有哪些权限：

`umask -S`

- 移除用户组合其他用户的所有权限：

`umask {{077}}`

- 为所有用户开放读权限（即从掩码中移除了所有用户的r权限）：

`umask {{a+r}}`

