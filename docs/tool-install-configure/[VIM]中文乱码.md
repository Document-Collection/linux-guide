
# [VIM]中文乱码

参考：[解决配置vim中文乱码的问题](https://blog.csdn.net/weixin_36250487/article/details/79888103)

`vim`配置文件为`vimrc`

    $ cd /etc/vim
    $ cat vimrc
    ...
    ...
    " Source a global configuration file if available
    if filereadable("/etc/vim/vimrc.local")
    source /etc/vim/vimrc.local
    endif

新建文件`vimrc.local`，添加如下语句

    set fileencodings=utf-8,ucs-bom,gb18030,gbk,gb2312,cp936
    set termencoding=utf-8
    set encoding=utf-8