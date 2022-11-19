# Git学习笔记

## Git配置
```
git config --list   // 查看当前的配置，配置内容存放在文件 ~/.gitconfig 中

git config --global --edit  //打开config文件进行编辑

Or

git config --global user.name "Sky Ao"  // 配置当前单个仓库时把 --global去掉即可
git config --global user.email "aoxiaojian@gmail.com"   //配置当前单个仓库时把 --global去掉即可

git config --global color.ui auto   // 提高命令输出的可读性
```
## Git 基本操作
### git init -- 初始化仓库
```
git init    // 在需要初始化为仓库的目录里执行
```

### git log -- 查看提交日志
```
git log     // 正常显示提交日志
git log --pretty=short      // 只显示提交信息的第一行
git log README.md       // 只显示指定文件或者目录相关的日志
git log -p      // 显示文件的改动

git log --graph     // 以图形的方式输出提交日志，尤其在查看分支操作方面更有用
```

### git diff -- 查看更改前后的差别
```
git diff    // 查看工作树和暂存区的差别，还没有 git add 修改
git diff HEAD    // 查看工作树和最新提交的差别，git add 之后，git commit之前
```

### git branch -- 分支操作
```
git branch      // 查看所以分支，以及当前正在工作的分区
git checkout -b branch-name     // 创建，切换分支
git branch branch-name      // 切换到branch-name分支
git checkout branch-name    // 切换到branch-name分支
git checkout -              // 切换到之前的一个分支

git merge --no-ff branch-name  // 把branch-name分支的更改合并到当前分支上

git branch -d branch-name       // 正常删除已经merge的分支
git branch -D branch-name       // 强制删除分支， 不管是否完成merge
```

### git reset -- 回溯历史版本
```
git reset --hard hash-code      // 把版本回溯到hash-code对应的时间点

git reflog      // 查看当前仓库的操作日志，而git log只能显示当前状态为终点的日志
```

### git commit --amend -- 修改提交的信息
```
git commit --amend      // 把当前的commit合并到上一次的commit里
```
