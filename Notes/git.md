### git

##### 一、确认身份

```bash
git config --global user.name
git config --global user.email
```

##### 二、链接远程仓库

###### git clone

```bash
$git clone https://github.com/Kang-Jay/KangJay.git
```

###### git remote add

```bash
$git init
$git remote add https://github.com/Kang-Jay/KangJay.git
$git pull origin master
```

在 pull 失败的时候尝试 -u (--set-upstream)参数。原因可能是远程仓库没有该分支。

```bash
$git pull -u origin master
```



##### 三、工作流

```bash
$git pull

$git add .
$git commit -m "update"
$git push
```

##### 四、分支

###### 查看分支

（星号为当前分支）

```bash
$git branch 
```

###### 创建分支

```bash
$git branch new
```

###### 切换分支

```bash
$git checkout new
```

###### 创建并切换分支

```bash
$git checkout -b b
```

###### 合并分支

（一般先切换到主分支后再合并）

```bash
$git merge new
```

###### 删除分支

```bash
$git branch -d
```

（强制删除）

```bash
$git branch -D
```

##### 五、标签

###### 打标签

```bash
$git tag v1.0
```

###### 切换到某标签的状态

```bash
$git checkout v1.0
```

##### 六、SSH密钥

###### 秘钥存放位置

```tex
C:\Users\21147\.ssh
```

密钥：id_rsa    公钥：id_rsa.pub

###### 创建密钥

```bash
$git ssh-keygen -t rsa
```

###### 验证是否连接成功

```bash
$git ssh -T git@github.com
```

