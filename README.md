# ConvenientCommand
便捷实用命令

## 使用循环批量创建文件夹
如果你想批量创建命名规则相同的一系列文件夹（如 folder1、folder2 等），可以使用 for 循环命令。

```cmd
for /l %i in (1,1,10) do mkdir folder%i
这将创建 folder1 到 folder10 的 10 个文件夹。
```
`for /l %i in (1,1,10)`：表示循环从 1 到 10，每次递增 1。
`mkdir folder%i`：在每次循环中创建文件夹，如 folder1, folder2 等。

从 .txt 文件读取文件夹名称并批量创建
如果你有一个包含文件夹名称的 .txt 文件，也可以从文件中读取这些名称并批量创建文件夹。

创建一个包含文件夹名称的 .txt 文件，如 folders.txt，内容示例：

```
folder1
folder2
folder3
folder4
```
使用以下命令读取 .txt 文件并批量创建文件夹：

```cmd
复制代码
for /f %i in (folders.txt) do mkdir %i
这将根据 folders.txt 文件中的名称创建相应的文件夹。
```
