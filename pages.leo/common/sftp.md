# sftp [modified]

> Secure File Transfer Program.
> Interactive program to copy files between hosts over SSH.
> For non-interactive file transfers, see `scp` or `rsync`.
> More information: <https://manned.org/sftp>.

- 在普通命令前增加 l 前缀，使得该命令在本地主机执行，常用的命令如下：

```
cd / lcd        : 切换远程/本地目录
ls / lls        : 查看远程/本地目录内的所有目录项
pwd / lpwd      : 查看远程/本地的工作路径
mkdir / lmkdir  : 在远程/本地创建目录
```

- 连接远程主机，-i 指定私钥文件，-P 指定端口号，默认为 22，同时可切换远程主机的指定目录:

`sftp -i {{path/private_key}} -P {{port}} {{remote_user}}@{{remote_host}}{{:/path/to/dir/}}`

- 将文件下载到本地：

`get {{/path/remote_file}} {{/path/local_file}}`

- 将本地文件发送到远程主机：

`put {{/path/local_file}} {{/path/remote_file}}`

- -R 选项用于递归发送目录 (works with `put` too):

`get -R {{/path/remote_directory}}`

- 查看帮助文档，了解支持哪些命令：

`help`
