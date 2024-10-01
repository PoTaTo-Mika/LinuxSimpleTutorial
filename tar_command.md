在linux当中，我们常常是使用命令行进行一系列操作的，那么最重要的压缩和解压该如何实现呢？

```bash
tar -command output_name.tar/tar.gz file_folder
```

其中```bash -command```参数包括：

```-c```:创建一个新的归档文件

```-x```:解压归档文件(tar.gz)

```-z```:使用gzip解压

```-v```:显示解压过程

```-f```:指定被解压文件的名称

好的，如果我们接下来需要分卷压缩一个巨大的文件，那该怎么做呢？

```bash
tar -cvf source.tar
```

我们先打包一个大的tar

然后用```split```指令

```bash
split -b 大小/per_file 大tar 生成的分卷前缀
```

如果需要合并的话直接使用cat就行了:

```bash
cat file1 file2 file3 ... * > combined_tar
```