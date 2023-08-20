# kill [modified]

> Sends a signal to a process, usually related to stopping the process.
> All signals except for SIGKILL and SIGSTOP can be intercepted by the process to perform a clean exit.
> More information: <https://manned.org/kill>.

- Terminate a program using the default SIGTERM (terminate) signal:

`kill {{process_id}}`

- List available signal names (to be used without the `SIG` prefix):

`kill -l`

- Terminate a background job，详见 jobs 命令:

`kill %{{job_id}}`

- 强制杀死指定进程：

`kill -{{9|KILL}} {{process_id}}`

- 强制杀死指定进程组：

`kill -{{9|KILL}} -{{process_group_id}}`

- 查看常用信号含义：

`tldr signal`

