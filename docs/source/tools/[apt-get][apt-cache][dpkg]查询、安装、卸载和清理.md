
# [apt-get][apt-cache][dpkg]查询、安装、卸载和清理

参考：[apt-get](https://baike.baidu.com/item/apt-get/2360755)

## 查询

参考：[linux apt-cache使用方法](https://www.cnblogs.com/zzg-home/p/8032807.html)

查询已安装应用

```
apt list --installed
# 或者
dpkg -l
```

查询应用依赖

```
apt-cache depends package_name
```

搜索软件包

```
apt-cache search package_name
```

查看指定软件信息

```
apt-cache show package_name
```

## 安装

```
apt-get install package_name
```

* 参数`-y`表示跳过系统提示，直接安装
* 参数`--fix-missing`表示修复缺失的包

```
# 更新软件源中的所有软件列表
apt-get update
# 更新软件
apt-get upgrade
# 将系统升级到新版本
apt-get dist-upgrade
```

```
#安装本地deb包
dpkg -i *.deb
```

## 卸载

```
# 卸载一个已安装的软件包（保留配置文档）
apt-get remove package_name
# 卸载一个已安装的软件包（删除配置文档）
apt-get remove --purge packagename
# 删除包及其依赖的软件包
apt-get autoremove packagename
# 删除包及其依赖的软件包+配置文件
apt-get autoremove --purge packagname
```

```
dpkg -r *.deb
```

## 清理

```
# 清除已卸载软件备份
apt-get autoclean
# 同时清除已安装软件备份
apt-get clean
```