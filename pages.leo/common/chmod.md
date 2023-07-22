# chmod [modified]

> Change the access permissions of a file or directory.
> More information: <https://www.gnu.org/software/coreutils/chmod>.

- 常用格式（u 表示其拥有者，g 表示其所属组，o表示其他用户，a 同时表示这三类）：

`chmod [ugoa][+-=][rwx] {{path/to/file}}`

- 使用数字指定权限；第一个数字用于指定 SGID 权限（见下文），可省略；
- 其余三个数字分别对应 u,g,o 三类用户权限：

`chmod 2740 {{path/to/file}}`

- 递归：

`chmod -R u+x,g+w {{path/to/file}}`

- SUID，SGID，SBIT 权限：

```
SUID: 4, u+s, 针对二进制程序有效，执行者将具有拥有者的权限
SGID: 2, g+s, 针对二进制程序和目录有效
SBIT: 1, o+t, 针对目录有效，在该目录下创建的文件仅有自己和 root 可以删除
```

- 为一个二进制程序添加 SUID 权限：

`chmod u+s {{path/to/binary}}`

