---
title: "Hexo bug: Error: Spawn failed at ChildProcess.<anonymous>"
date: 2020-08-31 23:40:41
categories: 
 Hexo
tags: 
 Bug
---

- 错误信息

```
fatal: in unpopulated submodule '.deploy_git'
FATAL {
  err: Error: Spawn failed
      at ChildProcess.<anonymous> (/Users/ryandu/duyangs.github.io/node_modules/hexo-deployer-git/node_modules/hexo-util/lib/spawn.js:51:21)
      at ChildProcess.emit (events.js:314:20)
      at Process.ChildProcess._handle.onexit (internal/child_process.js:276:12) {
    code: 128
  }
} Something's wrong. Maybe you can find the solution here: %s https://hexo.io/docs/troubleshooting.html
```



- 解决方案

1. 检查`_config.yml`中的`deploy`是否正确

```yaml
#示例
deploy:
  type: git
  repo: git@github.com:duyangs/duyangs.github.io.git
  branch: master
```



2. 检查是否配置了SSH
3. 删除本地`.deploy_git`文件夹

```
rm -rf .deploy_git
```

4. 重新执行`deploy`

