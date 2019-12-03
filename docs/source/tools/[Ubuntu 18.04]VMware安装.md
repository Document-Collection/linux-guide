
# [Ubuntu 18.04]VMware安装

参考：[在ubuntu18.04上安装vmware](https://blog.csdn.net/qq_43658650/article/details/86663326)

在Ubuntu 18.04上安装VMware，之前虽然在16.04上安装过，但是这次操作发现还有一些需要调整的地方

[[Ubuntu 16.04]VMware安装](https://zj-linux-guide.readthedocs.io/zh_CN/latest/tools/[Ubuntu%2016.04]VMware%E5%AE%89%E8%A3%85.html)

## 下载

一定要去官网下载最新版本：[Try VMware Workstation Pro](https://www.vmware.com/products/workstation-pro/workstation-pro-evaluation.html)

当前使用：

```
$ vmware-installer -l
Product Name         Product Version     
==================== ====================
vmware-workstation   15.5.1.15018445     
```

## 必备条件

安装以下应用：

```
$ sudo apt install gcc g++ libcanberra-gtk-module build-essential
```

## 安装

首先赋予执行权限

```
$ sudo chmod a+x VMware-Workstation-Full-15.5.1-15018445.x86_64.bundle
```

然后进行安装

```
$ sudo ./VMware-Workstation-Full-15.5.1-15018445.x86_64.bundle
Extracting VMware Installer...done.
Installing VMware Installer 3.0.0
...
...
Installing VMware Workstation 15.5.1
Copying files...
Configuring...
Installation was successful.
```

安装完成后启动`VMware`，进入图形界面进行配置即可

## 卸载

参考：[有关于ubuntu16.04 卸载vmware](https://blog.csdn.net/smile_5me/article/details/80799328)

```
$ sudo vmware-installer --uninstall-product vmware-workstation
```