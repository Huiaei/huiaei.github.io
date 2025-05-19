---
title: ArchManjaro（pacman）配置国内源
slug: archmanjaro-pacman-configuration-domestic-source-srfse
url: /post/archmanjaro-pacman-configuration-domestic-source-srfse.html
date: '2024-03-02 22:11:50+08:00'
lastmod: '2025-05-19 00:27:28+08:00'
tags:
  - Pacman
  - 使用技巧
keywords: Pacman,使用技巧
toc: true
isCJKLanguage: true
---



# ArchManjaro（pacman）配置国内源

1. 更改源

* 使用`pacman-mirros`更改镜像软件库所在国家 `sudo pacman-mirrors -i -c China -m rank`
* 或者使用nano或vim打开`/etc/pacman.d/mirrorlist` 添加源服务器链接并保存，例如，清华源 `Server = https://mirrors.tuna.tsinghua.edu.cn/archlinux/$repo/os/$arch`

1. 使用命令`pacman -Syy`强制刷新软件库缓存
2. 可选选择 安装`archlinuxcn` 1. 打开`/etc/pacman.conf` 2. 在末尾添加

```
[archlinuxcn]
Server = https://mirrors.tuna.tsinghua.edu.cn/archlinuxcn/$arch
```

服务器可选以下，只需替换`Server =`之后的链接（搜集不全，如有缺失，欢迎补充）

|名字|链接|
| ------| ---------------------------------------------------|
|中科大|https://mirrors.ustc.edu.cn/archlinuxcn/$arch|
|网易|http://mirrors.163.com/archlinux-cn/$arch|
|腾讯云|https://mirrors.cloud.tencent.com/archlinuxcn/$arch|
|----||

推荐参考资料：[archwiki](https://wiki.archlinux.org)
