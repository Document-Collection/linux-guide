
# [Ubuntu 16.04]清理应用

参考：[ubuntu安装和查看已安装软件](https://blog.csdn.net/coolcooljob/article/details/80547527)

查询当前已安装应用

    apt list --installed
    # 或者
    dpkg -l

卸载安装的应用

    sudo apt-get remove --purge app-name
    sudo apt-get autoremove
    # 或者
    $ sudo dpkg -r xxx

比如删除亚马逊应用

    sudo apt-get remove --purge unity-webapps-common
    sudo apt-get autoremove

