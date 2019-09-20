
# [Ubuntu 16.04]Network service discovery disabled

经常会遇到一个问题：在开机或者切换网络过程中，右上角弹出一个提示框，显示

```
Network service discovery disabled
```

参考[Network service discovery disabled: What does this mean for me?](https://askubuntu.com/questions/339702/network-service-discovery-disabled-what-does-this-mean-for-me)

进入目录`/etc/default/`，修改文件`avahi-daemon`如下：

```
# 1 = Try to detect unicast dns servers that serve .local and disable avahi in
# that case, 0 = Don't try to detect .local unicast dns servers, can cause
# troubles on misconfigured networks
# AVAHI_DAEMON_DETECT_LOCAL=1
AVAHI_DAEMON_DETECT_LOCAL=0
```

重启即可