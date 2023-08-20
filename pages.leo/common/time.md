# time [modified]

> See how long a command takes.
> More information: <https://manned.org/time>.

- 各时间含义：

```
real    实际运行时间 = 用户时间 + 系统时间 + 等待时间
user    在用户态的时间（用户时间）
sys     在内核态的时间（系统时间）
```

- 统计程序运行时间

`time {{program}}`
