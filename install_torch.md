我们都知道，直接启动

```bash
pip install torch
```

是没法下载支持CUDA的torch的。

所以我们需要在后面加一行:

```bash
pip install torch --index-url https://download.pytorch.org/whl/cu121
```

cu后面的数字就是对应的cuda版本号，不过torch会向下兼容，所以问题不大。