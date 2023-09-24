把本地库的代码上传到github

1 git本地分支改名

```bash
#本地默认分支名是master，但github上是main，这样在push时比较麻烦，因此在初始化仓库同时更改本地分支master为main
git branch -m master main
```

2 初始化仓库并提交文件(代码)

```bash
git add . #git add 文件名
git commit -m "文件描述信息" #如果
```

3 连接远程仓库并同步冲突

```bash
git remote add origin url

#远程仓库创建的新仓库如果新建时有readme，且本地新建init了一个库，直接add commit后push会报错,这是因为造成了冲突
#解决思路：先pull远程仓库，之后再push.这里--rebase是合并冲突的意思
git pull --rebase origin main
```

4 push到远程仓库

```bash
git push -u origin main
```

