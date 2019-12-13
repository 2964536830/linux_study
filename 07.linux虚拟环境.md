## virtualenv

1.  virtualenv 是 <python> 的一个库
    > pip3 install -i https://pypi.tuna.tsinghua.edu.cn/simple virtualenv
2.  调用 virtualenv 命令
    > --no-site-packages 这是构建干净，隔离的模块的参数
    > --python=python3 指定基础物理解释器

```shell
  ~ virtualenv --no-site-packages --python=python3   testenv1
```

3. 此时已生成 testenv1 目录,切换到该目录

- 激活虚拟环境

```shell
  # 调用后前面会出现虚拟环境名
  source testenv1/bin/activate
```

- 检查环境变量

```shell
	echo $PATH 检查环境变量
	which python3
	which pip3  检查虚拟环境是否正常
```

4. 退出虚拟环境

```shell
~ deactivate
```

## 导出 python 环境包

1. 命令

```shell
~ pip3 freeze > requirements.txt
```

2. 上传至服务器后，在服务器下创建 virtualenv，在 venv 中导入项目所需的模块依赖

```shell
pip3 install -r requirements.txt
```

## 虚拟环境管理工具 virtualenvwrapper

1. 安装

```shell
~ pip3 install virtualenvwrapper
```

2. 配置 python 环境变量在最前面

```shell
~ vim /etc/profile
PATH=/opt/python38/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/root/bin:/root/bin
~ source /etc/profile
```

3. 编辑 ~/.bashrc

```shell
export WORKON_HOME=~/Envs   #设置virtualenv的统一管理目录
export VIRTUALENVWRAPPER_VIRTUALENV_ARGS='--no-site-packages'   #添加virtualenvwrapper的参数，生成干净隔绝的环境
export VIRTUALENVWRAPPER_PYTHON=/opt/python347/bin/python3     #指定python解释器
source /opt/python34/bin/virtualenvwrapper.sh #执行virtualenvwrapper安装脚本
```

4. 重新登录

5. 使用 virtualenvwrapper 工具

```shell
~ mkvirtualenv  <虚拟环境名>   #自动下载虚拟环境，且激活虚拟环境

~ workon  <虚拟环境名>   #激活虚拟环境

~ deactivate  # 退出虚拟环境

~ rmvirtualenv	# 删除虚拟环境

~ cdvirtualenv  # 进入当前已激活的虚拟环境所在的目录

~ cdsitepackages # 进入当前激活的虚拟环境的，python包的目录
```
