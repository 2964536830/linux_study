## 对文件夹的增删改查

### 查看当前所在目录

```shell script
~ pwd
```

### 查看列表下的文件或者文件夹

```shell script
~ ls
~ ls /root
~ ls -l /root  # 显示root文件夹下详细信息
~ ls -la # 显示所有的隐藏文件和文件夹
.  代表当前目录
.. 代表上一级
```

### 创建文件夹

```shell script
~ mkdir xxx # 创建一个名为xxx的文件夹
```

### 更改目录

```shell script
cd xxx
cd /xxx/xxx
```

### 增加文件

```shell script
~ touch xxx.txt
```

### 删除文件

```shell script
~ rm xx.txt
~ rm -i xx.txt
~ rm -i xx* # 删除以xx开头的【文件】
```

### 删除文件夹

```shell script
# 只能删除空文件夹
~ rmdir xx
~ rm -r xx # 递归删除
~ rm -rf # 强制删除
~ rm -rf / or * # 删库到跑路
```

### 更改文件/文件夹名

```shell script
~ mv xxx xxx2
~ mv xxx xxx2/ # 移动文件到xxx2下
```

### 编辑文件

```shell script
# 按 i 进入编辑模式
# 按 esc 进入命令模式

~ vi xxx.py

# 命令模式
~ :wq 保存并推出
~ :q! 强制退出

```

### 查看文件

```shell script
~ cat xxx.py
```

## 其他命令

### 退出

```shell script
~ logout
~ ctrl + d
```

### 登录

```shell script
~ ssh xx@192.xx.xx.xx
~ ctrl + shift + d
```

### 更改密码

```shell script
~ passwd root
```

### 帮助手册

```shell script
~ man rm #查看rm的帮助手册
```

### 查看连接数量

```shell script
~ w
```

### 查看我是谁

```shell script
~ whoami
```

### 查看终端信息

```shell script
~ tty
```

### 更改主机名

```shell script
hostnamectl set-hostname xxxx
```
