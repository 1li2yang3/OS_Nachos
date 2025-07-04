# Nachos 操作系统课程设计

本项目基于 Nachos 教学操作系统平台，作为山东大学《操作系统》课程设计的一部分。通过八个阶段的实验，逐步实现了线程管理、进程调度、同步机制、地址空间管理、文件系统和系统调用等操作系统核心功能。

## 项目简介

- 支持多进程并发执行与系统调用交互
- 实现虚拟地址到物理内存的映射（页表机制）
- 扩展文件系统，支持文件的创建、删除、读写和追加
- 完成 `Exec`、`Exit`、`Join`、`Yield` 等系统调用
- 支持父子进程同步与资源回收

## 目录结构

- `code/threads/` — 基本线程管理模块
- `code/userprog/` — 用户程序加载与执行模块
- `code/filesys/` — 文件系统实现模块
- `code/machine/` — 硬件抽象模块
- `test/` — 用户态测试程序

## 编译与运行方法

1. 编译 Nachos 内核：

    ```bash
    cd code/threads
    make
    cd ../userprog
    make
    cd ../filesys
    make
    ```

2. 编译用户程序：

    ```bash
    cd test
    make
    ```

3. 运行 Nachos 并加载用户程序：

    ```bash
    ./nachos -x ../test/halt.noff
    ```

## 环境要求

- Linux 系统（推荐 Ubuntu）
- GCC 交叉编译工具链（MIPS 架构）
- GDB 调试器
- Nachos 原版源代码

## 实验内容概览

| 实验序号 | 实验主题 |
| :------: | :------ |
| 实验一 | Nachos 环境搭建与初步调试 |
| 实验二 | 项目结构分析与 Makefile 配置 |
| 实验三 | 使用信号量实现生产者-消费者问题 |
| 实验四 | 文件系统基本测试与分析 |
| 实验五 | 文件系统扩展：追加与中间写入 |
| 实验六 | 用户程序加载与地址空间管理 |
| 实验七 | 多进程内存管理机制改进 |
| 实验八 | 系统调用（Exec、Exit、Join、Yield）实现 |

## 项目亮点

- 多进程并发执行能力
- 页表管理与物理内存分配
- 完整的用户程序加载与执行流程
- 文件系统操作扩展
- 系统调用支持与父子进程同步

