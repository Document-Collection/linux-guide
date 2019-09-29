
# [Linux][usermod][passwd]用户权限调整

## usermod

参考：[Linux usermod命令](https://www.runoob.com/linux/linux-comm-usermod.html)

使用`usermod`修改用户的各种设置

修改用户登入目录

```
$ usermod -d DIR USER
```

修改用户初始组

```
$ usermod -g GROUP USER
```

修改用户附属组

```
# 以逗号分隔
$ usermod -G GROUPS USER
```

修改用户`ID`

```
$ usermod -u ID USER
```

修改用户帐号名

```
$ usermod -l NAME USER
```

## passwd

语法如下：

```
$ passwd USER
```

* 在`root`用户中不需要输入原先密码
* 在普通用户中需要输入原先密码

修改密码会加密保存在`/etc/shadow`中