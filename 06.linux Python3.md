## 安装 python3

1. 打开 python 官方网站找到安装包并下载
   > https://www.python.org/downloads/source/
   > wget https://www.python.org/ftp/python/3.8/Python-3.8.tgz
2. 下载环境依赖,避免 BUG

```shell
~ yum install gcc patch libffi-devel python-devel  zlib-devel bzip2-devel openssl-devel ncurses-devel sqlite-devel readline-devel tk-devel gdbm-devel db4-devel libpcap-devel xz-devel -y
```

3. 解压缩源码包

```shell
~ tar -xvf  Python-3.6.2.tgz
```

4. 切换到相应目录然后进行编译

```shell
~ ./configure --prefix=/opt/python36/
  --prefix  指定软件的安装路径

~  make # 生成安装文件
~  make install  # 安装
```

5. 配置环境变量

```shell
~ echo $PATH # 获取到原环境变量
PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/root/bin
~ vim /etc/profile # 写入
PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/root/bin:/opt/python36/bin
~ source /etc/profile # 使配置生效

```
