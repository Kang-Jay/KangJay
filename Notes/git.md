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

本地分支

（星号为当前分支）

```bash
$git branch 
```

远程分支

```bash
$git branch -r
```

查看本地分支与远程分支的关系

```bash
$git branch -vv
```

###### 创建分支

```bash
$git branch new
```

新创建的分支没有与远程分支相连接，需要

###### 切换分支

```bash
$git checkout new
```

###### 创建并切换分支

```bash
$git checkout -b new
```

###### 推送到新的远程分支

（将当前分支new推送到远程，本地分支的名称与之相同）

```bash
$git push origin -u new
```

###### 跟踪远程分支

```bash
$git branch --set-upstream-to=origin/main new
$git branch -u origin/main new
```

###### 创建，切换并跟踪远程分支

```bash
$git checkout -b new origin/main
```

###### 合并分支

（一般先切换到主分支后再合并）

```bash
$git merge new
```

###### 删除分支

本地分支：

```bash
$git branch -d <old_name>
```

（强制删除）

```bash
$git branch -D <old_name>
```

远程分支：

```bash
$git push -d origin <old_name>
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

##### 七、重命名

###### 重命名本地分支

切换--重命名--删除--默认远程仓库为上游（方便使用pull push）

*注意，如果删除的分支是默认分支，要把github中的默认分支改为其他分支后才能删除

```bash
$git checkout <old_name>
$git branch -m <new_name>
$git branch -d <old_name> //删除本地分支（清理工作目录）
$git push origin -d <old_name> //删除远程分支
$git push origin -u <new_name> //将当前分支推送到远程,本地分支的名称与之相同
```

