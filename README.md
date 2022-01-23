# bind_git_manage

## 本文是说明如何将空项目绑定到git的存储库

```
git init   # 把项目初始化,相当于在项目的跟目录生成一个 .git 目录
git add .    # 把项目的所有文件加入暂存区
git commit -am '项目初始化'     # 把项目提交到本地仓库，引号里面的是这次提交的注释，方便以后查看。
git remote rm origin  # 先删除远程 Git 仓库
git remote add origin https://github.com/BobinYang/   #为本地的仓库创建一个远程仓库. 例如：git remote add origin https://github.com/BobinYang/HtmlAgilityPackSample.git
git pull --rebase origin master  # 把远端仓库中的代码 拉到本地进得合并一下。
强制push本地仓库到远程 (这种情况不会进行merge, 强制push后远程文件可能会丢失 不建议使用此方法)
$ git push -u origin master -f

注意： 不能单纯地使用 git pull，也不能用 git push,这样作为报错的
rebase操作不会生成新的节点，是将两个分支融合成一个线性的提交。https://www.cnblogs.com/chenyablog/p/10308058.html)
执行后可以看到本地代码中多了README.md文件

git push origin master  # 将本地缓存仓库的文件推送到远程。master这个是分支名
```
