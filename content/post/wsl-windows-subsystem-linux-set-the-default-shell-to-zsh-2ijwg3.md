---
title: WSL（Windows子系统Linux）设置默认 Shell 为 Zsh
slug: wsl-windows-subsystem-linux-set-the-default-shell-to-zsh-2ijwg3
url: /post/wsl-windows-subsystem-linux-set-the-default-shell-to-zsh-2ijwg3.html
date: '2024-03-02 22:11:53+08:00'
lastmod: '2025-05-19 00:27:38+08:00'
tags:
  - 使用技巧
  - Windows
  - WSL
keywords: 使用技巧,Windows,WSL
toc: true
isCJKLanguage: true
---



# WSL（Windows子系统Linux）设置默认 Shell 为 Zsh

1. 安装 Zsh ，nano或者vim（选择你会使用的文本编辑器）
2. 使用 Linux 设置默认 Shell 为 Zsh 命令

```
    chsh -s /bin/zsh
```

1. 使用上述指令后，重新使用CMD或者PowerShell进入WSL时，会发现依旧为默认的Bash，此时需要编辑文件生效。使用你熟悉的文本编辑工具，vim或者nano，打开`~/bashrc`，向里面添加：

```
    [[ $- == *i* ]] && $(command -v zsh) || echo "ZSH is not installed"
```

之后保存即可。

---

> 参考自：[WSL 中设置 zsh 为默认 SHELL](https://limxw.com/posts/wsl-use-zsh/)
