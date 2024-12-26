1.工程下带有其他链接使用

```bash
git submodule update --init --recursive
```

2.git format

    git format-patch 123...123 arch/riscv

3.保持文件格式不变 

    git config --add core.filemode false 

    全局：
    git config --global core.filemode false

4.error: RPC failed; curl 56 GnuTLS recv error (-54): Error in the pull function.

问题解决：将下载地址的https改为git.例如：

    把’https://git.openwrt.org/feed/packages.git’改为’git://git.openwrt.org/feed/packages.git’

5.git rebase -i使用

    # p, pick <提交> = 使用提交
    # r, reword <提交> = 使用提交，但修改提交说明
    # e, edit <提交> = 使用提交，进入 shell 以便进行提交修补
    # s, squash <提交> = 使用提交，但融合到前一个提交
    # f, fixup <提交> = 类似于 "squash"，但丢弃提交说明日志
    # x, exec <命令> = 使用 shell 运行命令（此行剩余部分）
    # b, break = 在此处停止（使用 'git rebase --continue' 继续变基）
    # d, drop <提交> = 删除提交
    # l, label <label> = 为当前 HEAD 打上标记
    # t, reset <label> = 重置 HEAD 到该标记
    # m, merge [-C <commit> | -c <commit>] <label> [# <oneline>]
    # .       创建一个合并提交，并使用原始的合并提交说明（如果没有指定
    # .       原始提交，使用注释部分的 oneline 作为提交说明）。使用
    # .       -c <提交> 可以编辑提交说明。

6.github上提交代码

    1.添加ssh key
    2.git remote set-url origin git@github.com:zhuzhizhan/zhuzhizhan.github.io.git
    zhuzhizhan为账户名，zhuzhizhan.github.io为项目名
    git remote set-url origin git@github.com:zhuzhizhan/zhuzhizhan.github.io.git

### 8.github初始仓库创建

### …or create a new repository on the command line

    echo "# simulation-matlab" >> README.md
    git init
    git add README.md
    git commit -m "first commit"
    git branch -M main
    git remote add origin https://github.com/zhuzhizhan/simulation-matlab.git
    git push -u origin main

### …or push an existing repository from the command line

    git remote add origin https://github.com/zhuzhizhan/simulation-matlab.git
    git branch -M main
    git push -u origin main

### 9.git push --set-upstream origin master


