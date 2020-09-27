# git_demo

## init git repository

```
echo "# git_demo" >> README.md
git init
git add README.md
git commit -m "commit message..."
git branch -M master
git remote add origin "your repository"
git push -u origin master
```

> git branch -M master 建立新分支在遠端？？
> git checkout feature/test  建立新分支
> git add . 確認所有變更
> git commit -m 'commit message' 寫這次變更的註解
> git push origin <branch> 推送(同步)到遠端
