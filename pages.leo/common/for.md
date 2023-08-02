# for [modified]

> Perform a command several times.
> More information: <https://www.gnu.org/software/bash/manual/bash.html#Looping-Constructs>.

- 第一种语法格式：

```
for {{variable}} in {{item1 item2 ...}}; do
  {{command_block}}
done
```

- 第二种语法格式，类 C 语言：

```
for ((初始值; 限制条件; 赋值运算 )); do
  {{command_block}}
done
```

- 计算 1 到 100 之间奇数的和，`{1..100..2}` 可用 `$(seq 1 2 100)` 代替

```
sum=0
for i in {1..100..2}; do
  sum=$((${sum} + ${i}))
done
```

- 计算 1 到 100 之间奇数的和：

```
sum=0
for ((i=1; i<=100; i+=2)); do
  sum=$((${sum} + ${i}))
done
```
