## i 进入编辑模式

## esc 进入命令模式

## :wq :x :q :wq! 退出

## :set nu 显示行号

## :数字 跳转到某行

### 查找括号引用

```shell scripts
{ xxx:xxx }
~ shift + %
```

### 复制行

```shell scripts
~ yy + p
~ yy+数字 + p # 复制多少行
~ 数字+yy + p # 复制下面的多少行
```

### 删除行

```shell scripts
~ dd
~ 数字+dd # 从光标开始删除多少行
~ dG # 从光标开始删除下面全部
```

### 撤销 (u)

### 单个删除 (x)
