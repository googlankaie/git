## git标签

- 给当前分支最新的commit打上标签：

```
git tag v1.1
```

- 给历史的commit打上标签：

```shell
git tag v1.0 <commit_id>
```

- 删除标签：

```
git tag -d <tag name>
```

- 展示标签信息：

```
git show <tag>
```

- 展示所有标签：

```
git tag
```

- 指定标签信息：

```
git tag -a <tag name> -m <message>
```

- 推送标签到远程：

```
git push origin <tag name>
```

- 推送本地未推送的标签到远端：

```shell
git push origin --tags
```

- 删除远程库中的标签：

```
git tag -d <tag name> --先在本地删除
git push origin :refs/tags/<tag name>
```

## 忽略特殊文件

创建·`.gitignore`文件,将需要忽略的文件名写入，如

```
# Windows:
Thumbs.db
ehthumbs.db
Desktop.ini

# Python:
*.py[cod]
*.so
*.egg
*.egg-info
dist
build

# My configurations:
db.ini
deploy_key_rsa
```

- 执行git add时使文件不被忽略

```
git add -f <file name>
```

- 使文件不被忽略,gitignore文件中添加：

```
!<file name>
```

- 检查对某个文件的忽略规则：

```
git check-ignore -v <file name>
```