
# linux-guide

[![Documentation Status](https://readthedocs.org/projects/zj-linux-guide/badge/?version=latest)](https://zj-linux-guide.readthedocs.io/zh_CN/latest/?badge=latest) [![standard-readme compliant](https://img.shields.io/badge/standard--readme-OK-green.svg?style=flat-square)](https://github.com/RichardLitt/standard-readme) [![Conventional Commits](https://img.shields.io/badge/Conventional%20Commits-1.0.0-yellow.svg)](https://conventionalcommits.org) [![Commitizen friendly](https://img.shields.io/badge/commitizen-friendly-brightgreen.svg)](http://commitizen.github.io/cz-cli/)

> Linux使用指南

学习并使用`Linux`工具、相关配置以及对应基础知识。当前分为以下几部分：

1. 工具安装及使用
2. 工具及系统配置
3. 用户权限配置
4. `SSH`配置
5. `SHELL`脚本编程
6. 云服务器配置

当前操作系统：`Ubuntu 18.04`

`Ubuntu 16.04`相关文档保存在版本[v0.1.0](https://github.com/zjZSTU/linux-guide/releases/tag/v0.1.0)中

## 内容列表

- [背景](#背景)
- [安装](#安装)
- [用法](#用法)
- [主要维护人员](#主要维护人员)
- [参与贡献方式](#参与贡献方式)
- [许可证](#许可证)

## 背景

`Linux`系统使用应该说是程序员必备的基础知识，不过这里面涉及了很大的范围。在使用过程中陆陆续续会碰到不懂的概念或工具，记录下来，以备后续查询

# 安装

需要预先安装以下工具：

```
$ pip install -U Sphinx
$ sudo apt-get install make
```

## 用法

有两种使用方式

1. 在线浏览文档：[linux指南](https://zj-linux-guide.readthedocs.io/zh_CN/latest/?badge=latest)

2. 本地生成文档，实现如下：

    ```
    $ git clone https://github.com/zjZSTU/linux-guide.git
    $ cd linux-guide/docs
    $ make html
    ```
    编译完成后进入`docs/build/html`目录，打开`index.html`文件

## 主要维护人员

* zhujian - *Initial work* - [zjZSTU](https://github.com/zjZSTU)

## 参与贡献方式

欢迎任何人的参与！打开[issue](https://github.com/zjZSTU/linux-guide/issues)或提交合并请求

注意:

* `GIT`提交，请遵守[Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0-beta.4/)规范
* 语义版本化，请遵守[Semantic Versioning 2.0.0](https://semver.org)规范
* `README`编写，请遵守[standard-readme](https://github.com/RichardLitt/standard-readme)规范

## 许可证

[Apache License 2.0](LICENSE) © 2019 zjZSTU
