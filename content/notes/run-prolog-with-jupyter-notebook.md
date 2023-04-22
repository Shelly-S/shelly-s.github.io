---
title: "Run Prolog With Jupyter Notebook"
date: 2023-03-15T20:06:22+08:00
categories: 
  - "Programming"
tags: 
  - "Prolog"
draft: false
---

在 Jupyter Notebook 中运行 Prolog 需要安装相应的 kernel，使用的是 [这个实现](https://github.com/hhu-stups/prolog-jupyter-kernel)，环境为 WSL2 (Ubuntu22.04.2 LTS) on Win11。

- 安装稳定版本 Prolog，参见 [这个链接](https://www.swi-prolog.org/build/PPA.html)；

```bash
sudo apt-get install software-properties-common
sudo apt-add-repository ppa:swi-prolog/stable
sudo apt-get update
sudo apt-get install swi-prolog
```

- 安装 Python3 和 Python3-pip (注：使用 conda 则忽略此步)；

- 安装 `requests` 库和 `notebook` 库；

```bash
python3 -m pip install requests
python3 -m pip install notebook
```

- 安装 kernel；

```bash
python3 -m pip install prolog_kernel
python3 -m prolog_kernel.install
```

- 最后新建文件时内核选择 Prolog 即可。

