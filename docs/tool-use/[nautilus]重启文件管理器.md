
# [nautilus]重启文件管理器

今天遇到一个问题是文件夹突然打不开了，参考[ubuntu文件管理器假死的解决办法](https://blog.csdn.net/php_225869/article/details/73204533?utm_source=blogxgwz6)方法，查询文件管理器的`pid`并重启

    # 查找系统中的每个进程并搜索文件管理器nautilus
    $ ps -ef | grep nautilus
    zj        6938  1300  0 00:40 ?        00:00:01 /usr/bin/nautilus --gapplication-service
    zj        7822  7696  0 00:48 pts/2    00:00:00 grep --color=auto nautilus

然后杀死进程，重新点击文件夹启动

    kill 6938 & kill 7822


