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

> **echo "# git_demo" >> README.md** : 新增 內容為'# git_demo' 的 README.md 檔案   
> **git branch -M master** : 建立新分支   
> **git branch (-r, -a)** : 查看所有本地分支 (遠端分支, 全部分支)   
> **git branch (-r) -d branchName** : 刪除(遠端)本地分支     
> **git checkout branchName** : 切換分支(沒有就新創分支)  
> **git switch branchName** : 切換分支  
> **git add .** : 確認所有變更(git add --all 類似) 或 可以選擇特定檔案(git add fileName)  
> **git commit -m 'commit message'** : 寫這次變更的註解  
> **git merge branchName** : 合併分支   
> **git pull** : 同步遠端分支的內容到本地端分支   
> **git push origin branchName** : 推送(同步)到遠端   
> **git status** : 查看分支狀態  
> **git checkout -b branchName origin/branchName** : 從遠端複製分支  
加上 origin 代表遠端