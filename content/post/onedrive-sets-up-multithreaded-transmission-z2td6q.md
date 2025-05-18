---
title: Onedrive设置多线程传输
slug: onedrive-sets-up-multithreaded-transmission-z2td6q
url: /post/onedrive-sets-up-multithreaded-transmission-z2td6q.html
date: '2024-03-02 22:12:00+08:00'
lastmod: '2025-05-19 00:28:35+08:00'
tags:
  - 使用技巧
  - Onedrive
  - Windows
keywords: 使用技巧,Onedrive,Windows
toc: true
isCJKLanguage: true
---



# Onedrive设置多线程传输

修改文件： "%localappdata%\Microsoft\OneDrive\settings\Personal\global.ini" 向第一行加入： numberOfConcurrentUploads=3

> PS：数值项即为线程数，最小值为1，最大值为3，根据实际需要选择即可

可通过`Windows`+`R`运行，或cmd里运行下面直接打开修改： notepad "%localappdata%\Microsoft\OneDrive\settings\Personal\global.ini"

---

> [https://blog.tcpsoft.app/2020/03/let-onedrive-fly-scientifically/](https://blog.tcpsoft.app/2020/03/let-onedrive-fly-scientifically/)
