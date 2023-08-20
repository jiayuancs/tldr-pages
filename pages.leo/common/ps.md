# ps [modified]

> Information about running processes.
> More information: <https://manned.org/ps>.

- 常用选项：

```
-j: 使用 jobs 格式输出（包含 PGID 和 SID 等字段）
-l: 采用详细的格式来显示程序状况
-e: 显示所有进程
-f: 显示所有进程的完整格式，包括命令行、UID、PPID、CPU使用率、STIME等
-F: 包含 -f，同时增加了一些格外的字段
-L: 显示线程
```

- 查看所有运行的进程：

`ps aux / ps -ef`

- 仅查看自己 bash 相关进程的详细信息：

`ps -l`

- 查看某个进程中的线程：

`ps -Lf {{PID}}`

