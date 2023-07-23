# zip [modified]

> Package and compress (archive) files into zip file.
> See also: `unzip`.
> More information: <https://manned.org/zip>.

- Ubuntu 安装 zip 和 unzip：

`sudo apt install zip unzip`

- 常用选项

```
-r: 递归压缩子目录中的文件（压缩目录时必备）
-q: 不输出额外的信息
-sf: 即 --show-files，显示压缩包中的文件
--encrypy: 加密
```

- 压缩文件或目录，不输出额外的信息：

`zip -rq {{path/to/compressed.zip}} {{path/to/file1 path/to/file2 ...}}`

- 查看压缩包中包含的文件：

`zip -sf {{path/to/compressed.zip}}`

- 创建一个加密压缩文件：

`zip -rq --encrypt {{path/to/compressed.zip}} {{path/to/file1 path/to/file2 ...}}`

