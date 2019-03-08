
# [Linux][访问权限]分区和文件系统

## 分区

参考:

[Partitioning](https://wiki.archlinux.org/index.php/partitioning)

[Disk partitioning](https://en.wikipedia.org/wiki/Disk_partitioning)

分区(partition)是将磁盘空间划分可独立访问,分离管理的单个或多个空间,比如启动空间,交换空间,生成的分区信息存储在分区表方案中，如MBR或GPT

划分好磁盘空间后,必须格式化为文件系统,才能进行文件读写操作

常用分区工具:fdisk, parted

## 文件系统

参考:

[File systems](https://wiki.archlinux.org/index.php/File_systems)

[Linux](https://en.wikipedia.org/wiki/Linux)

[File system](https://en.wikipedia.org/wiki/File_system)

文件系统控制了文件存储和检索的方式,用于管理信息组及其名称的结构和逻辑规则称为“文件系统”。

## 命令

如何管理分区(当前分区,新建分区,删除分区,修改分区)

如何管理文件系统(如何分片,如何扩容)