正常来说，云端租卡都是一个root环境用到死，不过万一遇到了自己的B200服务器需要装多个环境的情况，我们就需要用虚拟环境或者直接docker启动了。

首先要确保conda已经初始化:

```bash
source /path/to/your/miniconda3/bin/activate
```

然后命令行最左边应该是有(base)的信息了，这时候我们就可以用:

```bash
conda activate your_env
```

进行激活。

如果没有conda虚拟环境的话，可以按照如下步骤进行新建:

```bash
conda create -n env_name python=3.11.5
```

如果不知道机器上有几个环境，可以使用:

```bash
conda env list
```

获取更多信息。