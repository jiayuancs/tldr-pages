# sftp [modified]

> Secure File Transfer Program.
> Interactive program to copy files between hosts over SSH.
> For non-interactive file transfers, see `scp` or `rsync`.
> More information: <https://manned.org/sftp>.

- 连接远程主机，-i 指定私钥文件，-P 指定端口号，默认为 22:

`sftp -i {{path/private_key}} -P {{port}} {{remote_user}}@{{remote_host}}`

- 将文件下载到本地：

`get {{/path/remote_file}} {{/path/local_file}}`

- 将本地文件发送到远程主机：

`put {{/path/local_file}} {{/path/remote_file}}`

- -R 选项用于递归发送目录 (works with `put` too):

`get -R {{/path/remote_directory}}`

- Get list of files on local machine:

`lls`

- Get list of files on remote machine:

`ls`
