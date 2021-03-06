# linux-0.12 源码学习

*参考《Linux内核完全剖析 --基于0.12内核》*

linux-0.12目录为修改过的源代码，其中加入了**中文注释**，修改部分代码使其能在现在的环境下**编译**，并且支持**GDB调试**。(无任何修改的源代码 -> [linux-0.12.tar.gz](src/code/linux-0.12.tar.gz))

| 文件夹        | 说明                  |
| ------------ | -------------------- |
| `linux-0.12` | linux-0.12源代码      |
| `oslab`      | 实验目录              |
| `src`       | 一些资源和笔记         |

## 一、实验篇

1. ubuntu(>=14.04)的用户可以使用`src/setup`目录下的一键搭建脚本[setup.sh](src/setup/setup.sh)；

2. 其他系统(包括ubuntu)的用户可以拉取已创建好的docker镜像作为实验环境，```docker pull ultraji/ubuntu-xfce-novnc:os_learn```；

具体内容请查看 [实验环境搭建及说明](src/note/实验相关/实验环境搭建及说明.md)。

<div align=center>
<img src="src/note/实验相关/.pic/docker.png" width = 70% height = 70% /> 
</div>

## 二、踩坑篇

如有错误、疏漏之处，感谢指出。

### 实验相关

1. [实验环境搭建及说明](src/note/实验相关/实验环境搭建及说明.md)
2. [常见编译问题总结](src/note/实验相关/编译源码的问题记录.md)
3. [0.12内核代码bug修复](src/note/实验相关/0.12内核代码bug修复.md)
4. [Bochs调试技巧](src/note/实验相关/Bochs调试技巧.md)
5. [GDB调试技巧](src/note/实验相关/GDB调试技巧.md)

### 知识积累

1. [C代码阅读提示](src/note/知识积累/C代码阅读提示.md)
2. [汇编中各寄存器的作用](src/note/知识积累/汇编中各寄存器的作用.md)
3. [内核源码文件目录说明](src/note/知识积累/内核源码文件目录说明.md)

### 系统总览

1. [内核导言](src/note/系统总览/内核导言.md)

### 建造工具 tools/

1. [建造工具build的说明](https://ultraji.github.io/post/linux0.12-build.html) 相关文件：`tools/build.c`

### 系统引导 boot/

1. [Linux0.12的启动过程](src/note/系统引导/Linux0.12的启动过程.md) 相关文件：`bootsect.S、setup.S`

### 文件系统 fs/

1. [总览](https://ultraji.github.io/post/linux0.12-filesystem.html)
2. [高速缓冲区的实现](https://ultraji.github.io/post/linux0.12-filesystem-buffer.html) 相关文件：`buffer.c`
3. [write和read的实现](https://ultraji.github.io/post/linux0.12-filesystem-rw.html) 相关文件：`block_dev.c、file_dev.c、char_dev.c、pipe.c、read_write.c`

### 内存管理 mm/
