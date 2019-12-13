



## 用户操作

### 添加用户

```powershell
~ useradd  用户名
```

### 更改密码

```powershell
# 修改某个用户的密码
~ passwd 用户名
# 修改自己的密码
~ passwd
```

### 切换用户

```powershell
# 切换到某个用户
~ su 用户名
```

### 删除用户

```powershell
# -r 删除家目录 -f强制删除
~ userdel 用户名
~ userdel -fr 用户名
```

## 用户组

### 添加用户组

```powershell
~ grounpadd 组名
```

### 更改用户所在组

```powershell
# usermod 更改用户身份信息
# -g 更改组
~ usermod -g 想移入的组 想移入的人
```



## 使用sudo命令

1.  修改/etc/suduers文件,添加sudo命令

### 文件权限管理

 ll查看文件详细信息

-rw-r--r-- 1 root root  386 Dec  9 14:18 index.html

> -rwx
>
> 第一个- 代表文件类型 - 是常规类型 d是文件夹类型
>
> -r 可读   													层级数字4
>
> -w 可写				 									层级数字2
>
> -x 可执行 比如查看详细信息 cd 等等    层级数字1

```shell
# 给某个文件权限
~ chmod u+wx xxx.py
~ chmod u-w  xxx.py
~ chmod g-w  xxx.py
~ chmod o-w  xxx.py
# 给某个用户权限
~ chmod u+x 用户名
# 使用层级数字	
~ chmod 743  xxx.py
```

更改所属组(成员)

```powershell
~ chown 用户 文件
~ chgrp 用户 文件
```

