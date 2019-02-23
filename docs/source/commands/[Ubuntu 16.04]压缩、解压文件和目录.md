
# [Ubuntu 16.04]压缩、解压文件和目录

在文件复制、移动、传输过程中，对文件、目录进行压缩能够极大提高效率和安全性

常用压缩命令包括

1. `zip`：打包和压缩（存档）文件
2. `tar`：`tar`存档实用程序的`GNU`版本

常用压缩格式包括

1. `.zip`
2. `.tar.gz`

## 参数解析

`tar`常用参数

1. `-z`：通过`gzip`压缩成档案文件
2. `-c`：创建一个新档案文件
3. `-v`：详细地列出处理的文件
4. `-f`：使用档案文件或`ARCHIVE`设备
5. `-x`：从档案文件中解压出文件

`unzip`常用参数

1. `-d`：解压到指定目录

## 压缩文件

    $ tar -zcvf file.tar.gz file1 file2 ...
    # 或
    $ zip file.zip file1 file2 ...

## 压缩目录

    # 包括文件夹
    $ tar -zcvf test.tar.gz test
    # 或
    $ zip -r test.zip test
    
    # 不包括文件夹
    $ tar -zcvf test2.tar.gz test/*

## 解压

    # 解压到当前文件夹
    $ tar -zxvf file.tar.gz
    # 或
    $ unzip file.zip

    # 解压到指定文件夹
    $ tar -zxvf file.tar.gz des
    # 或
    $ unzip file.zip -d des
