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
```

### git diff -- 查看更改前后的差别
```
git diff    // 查看工作树和暂存区的差别，还没有 git add 修改
```