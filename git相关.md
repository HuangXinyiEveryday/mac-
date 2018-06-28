#### 1.mac下git忽略所有的.DS_Store上传仓库

```
vi ~/.gitignore_global
```

```
输入i，复制以下内容
# OS generated files #
######################
.DS_Store
.DS_Store?
.Spotlight-V100
.Trashes
ehthumbs.db
Thumbs.db
```

```
按esc键，输入
:wq!
执行命令
git config --global core.excludesfile ~/.gitignore_global
```

#### 2.删除仓库存在的DS_Store

```
1.find . -name .DS_Store -print0 | xargs -0 git rm -f --ignore-unmatch
将 .DS_Store 加入到 .gitignore
2.echo .DS_Store >> ~/.gitignore
```

