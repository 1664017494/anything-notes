
# 初始化仓库本地分支是 master 远程是 main 时如何处理

```sh
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin url
git push -u origin main
```