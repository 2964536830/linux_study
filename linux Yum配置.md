## 配置 yum 源

1. 移除默认的 yum 仓库
   
   > 删除 /etc/yum.repos.d/下所有的.repo 文件
2. 配置 yum 源
   
   > 打开阿里云镜像源网址 https://developer.aliyun.com/mirror
3. 下载 Centos7
   
   > wget -O /etc/yum.repos.d/CentOS-Base.repo http://mirrors.aliyun.com/repo/Centos-7.repo
4. 清空旧的 yum 缓存
   
   > yum clean all
5. 生成新的 yum 仓库缓存(这个缓存来自于阿里云的 yum 仓库，便于加速软件下载)
   
   > yum makecache
6. 配置一个第三方的 额外仓库源(epel 源)
   
   > wget -O /etc/yum.repos.d/epel.repo http://mirrors.aliyun.com/repo/epel-7.repo
7. 使用 yum install xxx 下载所需软件
