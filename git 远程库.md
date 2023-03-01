# 远程仓库
## git 远程库
+ 添加git源
```
	git remote add origin <url>
```
+ 推送master分支所有内容
```
	(第一次推送:git push -u origin master )
	git push origin master
```
+ 查看远程库信息
```
	git remote -v
```
+ 与远程库断开链接
```
	git remote rm <源name>
```
## 从远程库克隆
```
	git clone <url>
```


# 分支管理
+ 创建并切换到该分支
```
git branch -b <branch>
```
等同于
```
git branch <branch>
git checkout <branch>
```
+ 切换分支
```
git checkout <branch>
```
+ 查看当前分支
```
git branch
```
带*的就是当前分支
+ 合并分支
```
git merge <branch> 
```
将指定分支合并到当前分支
+ 删除分支
```
git branch -d <branch>
```
*不能在当前分支删除当前分支*
删除未合并的分支：
```
git branch -D <branch>
```
+ 分支管理策略
合并分支时默认采用fast-forward模式，没有记录
使用普通模式--no-ff合并，会创建新的commit，合并后会有记录
```
git merge <branch> --no-ff -m <message>
```
## bug分支
+ 保留现场
```
git stash 
```
+ 列出保留的现场
```
git stash list
```
+ 恢复并删除现场
```
git stash pop 
```
等同于：
```
git stash apply
git stash drop
```
恢复某个现场：
```
git stash apply <stashid>
```
+ commit复用
将修复bug后的commit应用到当前分支：
```
git cherry-pick <commitid>
```
+ 本地分支与远程分支链接起来如：本地dev分支链接远程分支
```
git branch --set-upstream-to=origin/dev dev
```
