# nohup [modified]

> Allows for a process to live when the terminal gets killed.
> More information: <https://www.gnu.org/software/coreutils/nohup>.

- 在后台运行任务，即使关闭终端，任务仍继续执行：

`nohup {{command}} &`

- 指定输出文件：

`nohup {{command}} > {{path/to/output_file}} 2>&1 &`

