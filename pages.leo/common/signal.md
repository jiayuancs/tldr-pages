# signal [new]

> 记录 Linux(x86/ARM) 信号四要素，
> 从左到右依次为：编号、名称、默认动作、事件描述。
> 更为详细的描述见 `man 7 signal`。

- 信号的默认处理动作：

`Term`：终止进程
`Ign`： 忽略信号 (默认即时对该种信号忽略操作)
`Core`：终止进程，生成 Core 文件。(查验进程死亡原因， 用于 gdb 调试)
`Stop`：停止（暂停）进程
`Cont`：继续运行进程

- 常规信号（1-31），其中 9 号和 19 号不能被忽略，处理和阻塞：

`1)  SIGHUP    Term` 当用户退出 shell 时，由该 shell 启动的所有进程将收到这个信号
`2)  SIGINT    Term` 当用户按下了<Ctrl-C>组合键时，用户终端向正在运行中的由该终端启动的程序发出此信号
`3)  SIGQUIT   Core` 当用户按下<Ctrl-\>组合键时产生该信号，用户终端向正在运行中的由该终端启动的程序发出些信号
`4)  SIGILL    Core` CPU 检测到某进程执行了非法指令
`5)  SIGTRAP   Core` 该信号由断点指令或其他 trap 指令产生
`6)  SIGABRT   Core` 调用 abort 函数时产生该信号
`7)  SIGBUS    Core` 非法访问内存地址，包括内存对齐出错
`8)  SIGFPE    Core` 在发生致命的运算错误时发出。不仅包括浮点运算错误，还包括溢出及除数为 0 等所有的算法错误
`9)  SIGKILL   Term` 无条件终止进程。本信号不能被忽略，处理和阻塞
`10) SIGUSR1   Term` 用户定义的信号
`11) SIGSEGV   Core` 指示进程进行了无效内存访问
`12) SIGUSR2   Term` 用户自定义信号
`13) SIGPIPE   Term` Broken pipe 向一个没有读端的管道写数据
`14) SIGALRM   Term` 定时器超时，超时的时间由系统调用 alarm() 设置
`15) SIGTERM   Term` 程序结束信号，与 SIGKILL 不同的是，该信号可以被阻塞和终止。通常用来使程序正常退出。执行命令 Kill 时，缺省产生这个信号
`16) SIGSTKFLT Term` Linux 早期版本出现的信号，现仍保留向后兼容
`17) SIGCHLD   Ign`  子进程状态发生变化时，父进程会收到这个信号
`18) SIGCONT   Cont` 如果进程已停止，则使其继续运行
`19) SIGSTOP   Stop` 停止进程的执行。信号不能被忽略，处理和阻塞
`20) SIGTSTP   Stop` 停止终端交互进程的运行。按下<Ctrl-z>组合键时发出这个信号
`21) SIGTTIN   Stop` 后台进程读终端控制台
`22) SIGTTOU   Stop` 该信号类似于 SIGTTIN，在后台进程要向终端输出数据时发生
`23) SIGURG    Ign`  套接字上有紧急数据时，向当前正在运行的进程发出些信号，报告有紧急数据到达。如网络带外数据到达
`24) SIGXCPU   Core` 进程执行时间超过了分配给该进程的 CPU 时间 ，系统产生该信号并发送给该进程
`25) SIGXFSZ   Core` 超过文件的最大长度设置
`26) SIGVTALRM Term` 虚拟时钟超时时产生该信号。类似于 SIGALRM，但是该信号只统计该进程的 user time
`27) SGIPROF   Term` 类似于 SIGVTALRM，该信号只统计进程的 user time + sys time
`28) SIGWINCH  Ign`  窗口变化大小时发出
`29) SIGIO     Term`  此信号向进程指示发出了一个异步 IO 事件
`30) SIGPWR    Term` 关机
`31) SIGSYS    Core` 无效的系统调用

- 实时信号（34-64）没有固定的含义（可以由用户自定义）。所有的实时信号的默认动作都为终止进程。

