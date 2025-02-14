---
title: MLVP文档 - 首页
summary: MLVP Index
authors:
    - BlueSpace
date: 2023-11-01
---

{!README.md!}

**注意：本项目所有命令除非特殊说明都在MLVP项目主目录下运行**

**注意：本项目已经集成进[OVIP-UT](https://gitee.com/yaozhicheng/OVIP-UT/blob/master/src/cpp/tb_memory.cpp)**

## Installation and Configuration

详细步骤及common issue请见[安装与配置章节](./prepare.md)，其中本项目安装部分为必做

快速安装：在项目根目录运行

```sh
./scripts/prepare.sh
```

## Quick Start

前提：按照上一节完成环境安装与配置，详细说明见[Quick Start章节](./quickstart.md)

本项目由CMake构建，安装后在`MLVP`目录下执行：

```sh
# build file
./scripts/build.sh

# check raw system verilog file
cat design/NutshellCache/nutshellcache.sv

# run test
./bin/mlvp

# check total result
cat report/cache/total.info

# check coverage of system verilog loc
cat report/cache/cache.sv

# check vcd waveform
gtkwave log/cache/Driver0/cache.vcd
```

在以上步骤中我们完成了编译、验证目标查看、执行、结果查看，成功完成了一个简单的UT验证流程，获取到正确与否的验证结果和代码覆盖率报告。

若对本项目感兴趣并希望深入了解相关架构与设计，请继续阅读。

## Tutorial

教程参考[教程章节](./tutorial.md)

## Developer Guide

若想要参与开发，请查阅[开发者指南](./developer.md)

## API Reference

本项目重要函数都已添加完善注释，若想学习本项目可以试着帮助完善注释，本项目使用doxygen构建基于注释的API查询的文档，请参阅[API文档](./doxygen/html/index.html)
