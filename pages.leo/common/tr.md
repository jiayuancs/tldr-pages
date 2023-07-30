# tr [modified]

> 删除指定的文字，或是对文字进行替换。
> More information: <https://www.gnu.org/software/coreutils/tr>.

- -d 选项用于删除指定字符，例如删除冒号 ':'字符：

`{{cat /etc/passwd}} | tr -d '{{:}}'`

- 将文件中指定字符集替换为另一个字符集：

`tr '{{abcd}}' '{{jkmn}}' < {{path/to/file}}`

- 删除文件中的 a,b,c,d 字符：

`tr -d '{{[a-d]}}' < {{path/to/file}}`

- 使用单个字符代替连续出现的 a,b,c,d 字符：

`tr -s '{{[a-d]}}' < {{path/to/file}}`

- 将所有的小写字符替换为大写字符：

`tr '{{[:lower:]}}' '{{[:upper:]}}' < {{path/to/file}}`

