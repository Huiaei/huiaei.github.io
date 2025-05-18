---
title: Docker容器中无法运行二进制文件并出现：xxx not found
slug: >-
  the-binary-file-cannot-be-run-in-the-docker-container-and-appears-xxx-not-found-zoxfh6
url: >-
  /post/the-binary-file-cannot-be-run-in-the-docker-container-and-appears-xxx-not-found-zoxfh6.html
date: '2024-03-02 22:11:52+08:00'
lastmod: '2025-05-19 00:29:00+08:00'
tags:
  - 使用技巧
  - Docker
keywords: 使用技巧,Docker
toc: true
isCJKLanguage: true
---



# Docker容器中无法运行二进制文件并出现：xxx not found

## 问题

在Docker容器中，运行二进制文件出现 `/bin/sh: xxx not found` ，使用 Chmod 赋予执行权限依旧出现此问题。

## 解决

容器内执行 `mkdir /lib64 && ln -s /lib/libc.musl-x86_64.so.1 /lib64/ld-linux-x86-64.so.2`

## 原因

镜像可能使用的是以alpine镜像为基础的项目，可能出现动态链接库位置错误问题。

一般二进制文件在linux系统下编译，动态链接库是到/lib64目录下的，而在alpine镜像内无/lib64目录([参考](https://github.com/gliderlabs/docker-alpine/issues/11))。

alpine镜像使用的是musl libc而不是gun libc，因而动态链接库的位置不一致。

## 参考

https://stackoverflow.com/questions/34729748/installed-go-binary-not-found-in-path-on-alpine-linux-docker

https://github.com/docker-library/openjdk/issues/77

https://github.com/gliderlabs/docker-alpine/issues/11

https://github.com/sgerrand/alpine-pkg-glibc/releases

---

引用自：[alpine镜像启动的容器内运行二进制文件出现：/bin/sh: xxx not found](https://blog.51cto.com/welcomeweb/2652026)
