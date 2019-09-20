
# [Ubuntu 16.04]设置文件、目录权限

Linux针对每个文件和目录针对不同用户、组设置了访问限制

常用命令包括：

1. id：打印指定用户的用户和组信息
2. 

## 查看当前用户和组信息

    $ id -a
    uid=1000(zj) gid=1000(zj) groups=1000(zj),4(adm),24(cdrom),27(sudo),30(dip),46(plugdev),113(lpadmin),128(sambashare)

* uid指用户标识符（user identifier）
* gid指组标识符（group identifier）



用户/组/文件/目录

不同用户 不同组 不同权限

不同文件 不同目录 不同权限

设置用户/组/文件/目录的权限