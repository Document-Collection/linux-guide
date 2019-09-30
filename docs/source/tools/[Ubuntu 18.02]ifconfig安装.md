
## [Ubuntu 18.02]ifconfig安装

参考：[Why isn't ifconfig available in Ubuntu Docker container?](https://serverfault.com/questions/613528/why-isnt-ifconfig-available-in-ubuntu-docker-container)

`Docker`官方`Ubuntu`镜像不包含`ifconfig`，必须手动安装

```
# apt-get install net-tools
```