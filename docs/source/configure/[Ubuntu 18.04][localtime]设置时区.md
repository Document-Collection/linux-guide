
# [Ubuntu 18.04][localtime]设置时区

## 查询当前时间

使用命令`date`可查询当前时间

```
$ date
2019年 10月 05日 星期六 09:50:58 CST
```

## 查询当前时区

### localtime

文件`/etc/localtime`链接了当前所使用的时区

```
$ file /etc/localtime 
/etc/localtime: symbolic link to /usr/share/zoneinfo/Asia/Shanghai
```

### timezone

文件`/etc/timezone`保存了当前所使用时区

```
$ cat /etc/timezone 
Asia/Shanghai
```

## 时区设置

使用命令`dpkg-reconfigure`进行时区设置

```
$ sudo dpkg-reconfigure tzdata
...
...
Current default time zone: 'Asia/Shanghai'
Local time is now:      2019年 10月 05日 星期六 09:56:43 CST.
Universal Time is now:  Sat Oct  5 01:56:43 UTC 2019.
```