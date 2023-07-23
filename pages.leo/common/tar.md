# tar [modified]

> Archiving utility.
> Often combined with a compression method, such as gzip or bzip2.
> More information: <https://www.gnu.org/software/tar>.

- 常用选项：

```
-c: 打包
-x: 解包
-v: 输出压缩文件信息
-f: 指定压缩包的名称
-C: 指定解压输出路径
-t: 查看压缩包里的文件名

-a: 根据给出的后缀来确定使用何种压缩程序
-z: 使用 gzip 压缩，后缀格式为 .tar.gz，等同于 .tgz
-j: 使用 bzip2 压缩，后缀格式为 .tar.bz2
-J: 使用 xz 压缩，后缀格式为 .tar.xz
```

- 打包压缩为指定后缀的文件，根据给出的后缀来确定使用何种压缩程序：

`tar -caf {{path/to/target.tar[.gz|.bz2|.xz]}} {{path/to/file1 path/to/file2 ...}}`

- 解压文件到指定目录，如省略 -C 选项，则默认解压到当前目录：

`tar -xf {{path/to/source.tar[.gz|.bz2|.xz]}} -C {{path/to/directory}}`

- 查看压缩包中包含的文件：

`tar -tf {{path/to/source.tar[.gz|.bz2|.xz]}}`

- 查看一个压缩文件使用何种压缩程序：

`file {{path/to/file}}`

