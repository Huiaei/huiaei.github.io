---
title: Git 命令使用或取消代理
slug: git-commands-use-or-cancel-proxy-1eonzk
url: /post/git-commands-use-or-cancel-proxy-1eonzk.html
date: '2024-03-02 22:11:57+08:00'
lastmod: '2025-05-19 00:28:21+08:00'
tags:
  - 命令
  - 使用技巧
keywords: 命令,使用技巧
toc: true
isCJKLanguage: true
---



# Git 命令使用或取消代理

假设代理到目标 socks5://127.0.0.1:10808

1. 全局代理 git config --global http.proxy socks5://127.0.0.1:10808 git config --global https.proxy socks5://127.0.0.1:10808
2. 部分代理 git config --global http.https://github.com.proxy socks5://127.0.0.1:10808 git config --global https.https://github.com.proxy socks5://127.0.0.1:10808
3. 取消代理 git config --global --unset http.proxy git config --global --unset https.proxy

> 参考自: https://blog.gobyte.cn/post/1a22163b.html https://blog.csdn.net/tanningzhong/article/details/52817399
