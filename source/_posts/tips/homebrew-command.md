---
title: Homebrew 常用指令
date: 2020-11-10 10:02:46
categories:
- Tips
tags:
- Homebrew
---



### 更新

- 更新Homebrew自己

```
brew update
```

- 查看需要更新的包

```
brew outdated
```

- 更新包

```
brew upgrade //更新所有包
brew upgrade $FORMULA //更新指定包
```

- 清理旧版本

```
brew cleanup //清理所有包的旧版本
brew cleanup $FORMULA //清理指定包的旧版本
brew cleanup -n //查看可清理的旧版本包，不执行实际操作
```



### 锁定包（不想更新）

```
brew pin $FORMULA //锁定某个包
brew uppin $FORMULA //取消锁定
```



### 查看

- 包信息

```
brew info $FORMULA //显示某包的信息
brew info //显示安装了包数量，文件数量，和总占用空间
brew deps --installed --tree //查看已安装的包的依赖，树形显示
```

- 列出已安装的包

```
brew list
```



### 删除

```
brew rm $FORMULA //删除某个包
brew uninstall --force $FORMULA //删除所有版本
```

