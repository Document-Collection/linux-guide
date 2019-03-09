
# [Ubuntu 18.04][ssh]Too many authentication failures

昨天不小心删除了`ubuntu`用户，导致系统无法登录

今天重装了系统，使用公共镜像`Ubuntu 18.04`，重装完成后进行登录发现如下错误

    $ ssh ubuntu@132.232.142.219
    Received disconnect from 132.232.142.219 port 22:2: Too many authentication failures
    Connection to 132.232.142.219 closed by remote host.
    Connection to 132.232.142.219 closed.

先到控制台的云服务器页面，选择左侧的`SSH`密钥选项，删除之前设置的密钥

然后关闭实例，重新设置密钥，输入本地的公钥内容，再次启动实例后就能够登录了