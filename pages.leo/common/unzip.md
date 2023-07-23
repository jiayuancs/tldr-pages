# unzip [modified]

> Extract files/directories from ZIP archives.
> See also: `zip`.
> More information: <https://manned.org/unzip>.

- 常用选项

```
-q: 不输出额外的信息
-d: 指定输出目录
-l: 显示压缩包中的文件
```

- 解压多个压缩文件到当前目录：

`unzip -q {{path/to/compressed.zip path/to/compressed.zip ...}}`

- 解压到指定目录下：

`unzip -q {{path/to/compressed.zip}} -d {{path/to/directory}}`

- 显示压缩包中的文件：

`unzip -l {{path/to/compressed.zip}}`

