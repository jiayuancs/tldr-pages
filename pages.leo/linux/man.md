# man [modified]

> Format and display manual pages.
> More information: <https://manned.org/man>.

- man 手册有如下章节：

```
- 1. 用户命令(User commands)
- 2. 系统调用(System calls)
- 3. 库调用(Library calls)
- 4. 特殊文件,设备(Special files)
- 5. 文件格式和配置文件(File formats and configuration files)
- 6. 游戏(Games)
- 7. 杂项(Overview, conventions, and miscellaneous)
- 8. 系统管理命令(System management commands)
```

- Display the man page for a command:

`man {{command}}`

- Display the man page for a command from section 7:

`man {{7}} {{command}}`

- 查找，等同于 whatis 命令：

`man -f {{command}}`

- 模糊查找，等同于 apropos 命令：

`man -k apropos`
