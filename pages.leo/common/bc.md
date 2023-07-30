# bc [modified]

> An arbitrary precision calculator language.
> See also: `dc`.
> More information: <https://manned.org/man/bc.1>.

- 常用选项：

```
-l: 使用预定于的数学函数
-q: quiet，进入交互式窗口时不输出初始横幅信息
```

- 使用 -l 选项后，可使用如下函数：

```
s(x): sin(x)，x 是弧度
c(x): cos(x)，x 是弧度
a(x): arctan(x)，x 是弧度
l(x): ln(x)，自然对数
e(x): e^x
```

- 交互式计算窗口，输入 quit 退出：

`bc`

- 支持数学函数的交互式计算窗口，输入 quit 退出：

`bc -l`

- 计算数学表达式，支持 +,-,*,/,^,% 等运算：

`echo '{{5 / 3 + 7}}' | bc`

- 计算文件中的数学表达式，一行一个数学表达式：

`bc {{path/to/file}}`

- 使用 scale 指定计算精度（小数点后多少位）：

`echo 'scale = {{10}}; {{5 / 3}}' | bc`

- 计算圆周率，scale 指定精度为小数点后 100 位，4*a(1) 表示计算 4*arctan(1)，即 π:

`echo 'scale = {{100}}; {{4*a(1)}}' | bc -l`

