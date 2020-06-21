
# [wget]文件下载

`wget`是最常用的`Linux`下载工具了。实践过程中发现有一些参数很有用，记录一下

## 参数

* 断点续传

```
-c,  --continue                  断点续传下载文件
```

* 不需要验证服务器证书

```
--no-check-certificate       不要验证服务器的证书。
```

* 取出URL查询内容，保存相应的文件名

```
--content-disposition
```

还有一个很有用的小技巧，就是用单引号把`URL`括起来，这样`wget`就能解析整个地址了

## 示例

以下载`Win10 ISO`为例，其下载链接如下

```
https://software-download.microsoft.com/sg/Win10_2004_English_x64.iso?t=b71d6df1-e4fa-4a15-96e0-a0227b70d96c&e=1592790767&h=e27462a825a47057d8a5fedac94f2126
```

使用`wget`进行下载，添加断点续传和URL解析功能

```
$ wget -c --content-disposition 'https://software-download.microsoft.com/sg/Win10_2004_English_x64.iso?t=b71d6df1-e4fa-4a15-96e0-a0227b70d96c&e=1592790767&h=e27462a825a47057d8a5fedac94f2126'
--2020-06-21 09:53:08--  https://software-download.microsoft.com/sg/Win10_2004_English_x64.iso?t=b71d6df1-e4fa-4a15-96e0-a0227b70d96c&e=1592790767&h=e27462a825a47057d8a5fedac94f2126
正在解析主机 software-download.microsoft.com (software-download.microsoft.com)... 117.18.232.200
正在连接 software-download.microsoft.com (software-download.microsoft.com)|117.18.232.200|:443... 已连接。
已发出 HTTP 请求，正在等待回应... 200 OK
长度： 5268953088 (4.9G) [application/octet-stream]
--2020-06-21 09:53:09--  https://software-download.microsoft.com/sg/Win10_2004_English_x64.iso?t=b71d6df1-e4fa-4a15-96e0-a0227b70d96c&e=1592790767&h=e27462a825a47057d8a5fedac94f2126
再次使用存在的到 software-download.microsoft.com:443 的连接。
已发出 HTTP 请求，正在等待回应... 200 OK
长度： 5268953088 (4.9G) [application/octet-stream]
正在保存至: “Win10_2004_English_x64.iso”

Win10_2004_English_x64.iso                          1%[>                                                                                                          ]  93.08M  12.8MB/s    剩余 6m 57s^
```

## 问题

快下载完`Win10 ISO`的是否出现了错误

```
段错误（核心已转储）
```

### 解决一

我又在官网上重新下载了一次，速度非常快，平均`10MB/s`，就没有上面这个问题了 ???

### 解决二

参考[“段错误 (核心已转储) ”一种可能原因及其解决方法](https://blog.csdn.net/dahailantian1/articl)，扩大系统的堆栈空间

```
$ ulimit -a
core file size          (blocks, -c) 0
data seg size           (kbytes, -d) unlimited
scheduling priority             (-e) 0
file size               (blocks, -f) unlimited
pending signals                 (-i) 62941
max locked memory       (kbytes, -l) 16384
max memory size         (kbytes, -m) unlimited
open files                      (-n) 1024
pipe size            (512 bytes, -p) 8
POSIX message queues     (bytes, -q) 819200
real-time priority              (-r) 0
stack size              (kbytes, -s) 8192                     # 这里
cpu time               (seconds, -t) unlimited
max user processes              (-u) 62941
virtual memory          (kbytes, -v) unlimited
file locks                      (-x) unlimited
```

从`8192`扩大为`102400`

```
$ ulimit -s  102400
```