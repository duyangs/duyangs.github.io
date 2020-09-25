---
title: Git常用命令
date: 2020-09-25 10:22:15
categories: 
 Git
tags: 
 Git
---



> 特别提醒：文中命令所使用`[]`皆为强调,实际命令时需去除



---



## `branch`

### 新建分支
```git
//新建分支并切换到新分支
git checkout -b [分支名]

//新建分支，然后再切换到新的分支
git branch [分支名]
git checkout [分支名]
```

### 本地分支同步到远程仓库
```git
//同步到远程仓库
git push origin [本地分支名]

//同步到远程仓库并定义远程仓库名
git push origin [本地分支名]:[远程仓库分支名]
```

### 修改分支名
```git
修改本地
git branch -m [原分支名] [新分支名]

如需同步修改远程，则执行如下命令：
1、删除远程分支
git push --delete origin [原分支名]
2、上传新命名的本地分支
git push origin [新分支名]
3、建立关联
git branch --set-upstream-to origin/[新分支名]
```

### 同步远程仓库
1. 查看远程仓库
```git
git remote -v
```
2. 获取远程仓库代码
```git
git fetch origin [远程分支名]
```
3. 合并
```git
git merge origin/[远程分支名]
```


---



## `tag`

### 新建标签 
```git
git tag -a [标签名] -m '[标签说明]'
```

### 本地标签同步到远程仓库
```git
上传所有标签
git push origin --tags

上传指定标签
git push origin [标签名]
```