
# [Linux][访问控制]用户,组和其他

参考：

[Directories and the Set-User-ID and Set-Group-ID Bits](https://www.gnu.org/software/coreutils/manual/html_node/Directory-Setuid-and-Setgid.html)

[Permissions](https://wiki.debian.org/Permissions)

在Linux系统中每次登录均以用户的身份进行操作

每个用户属于一个或多个组，同一组内的用户共享组权限，比如一个文件设置为组可修改，那么属于同一组内的其他用户也可修改该文件

## 命令

常用命令：

1. stat：显示文件或文件系统状态
2. ls：列出目录内容
3. umask：设置文件模式创建掩码

如何创建用户/组/其他

如何修改用户/组/其他

如何删除用户/组/其他

如何查看用户/组/其他

参考:

[Users and groups](https://wiki.archlinux.org/index.php/users_and_groups)

[https://www.linode.com/docs/tools-reference/linux-users-and-groups/](https://www.linode.com/docs/tools-reference/linux-users-and-groups/)

