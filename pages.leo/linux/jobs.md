# jobs [modified]

> Shell builtin for viewing information about processes spawned by the current shell.
> Options other than `-l` and `-p` are exclusive to `bash`.
> More information: <https://manned.org/jobs>.

- 常用选项：

```
-l: 同时列出 PID
-r: 只列出正在运行的进程
-s: 只列出已停止的进程
```

- View jobs spawned by the current shell:

`jobs`

- 将后台任务拿到前台处理：

`fg %{{job_id}}`

- 让后台任务继续运行：

`bg %{{job_id}}`

- 终止后台任务：

`kill %{{job_id}}`
