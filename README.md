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

## basic git command line

> **echo "file content" >> fileName** : 新增 內容為"file content" 的 fileName 檔案  
> **rm fileName** : 刪除檔案  
> **mkdir folderName** : 建立 folder  
> **rm -d(-r) folderName** : 只能刪除空的 folder(刪除整個資料夾)  
> **git branch master** : 建立新分支(不切換)  
> **git branch (-r, -a)** : 查看所有本地分支 (遠端分支, 全部分支)  
> **git branch (-r) -d branchName** : 刪除(遠端)本地分支  
> **git checkout branchName** : 切換分支  
> **git checkout -b branchName** : 新創分支並切換  
> **git checkout -b branchName origin/branchName** : 從遠端複製分支  
> **git checkout -t origin/branchName** : 從遠端複製分支，並追蹤遠端分支  
> **git switch branchName** : 切換分支  
> **git add .** : 確認所有變更(git add --all 類似) 或 可以選擇特定檔案(git add fileName)  
> **git commit -m 'commit message'** : 寫這次變更的註解  
> **git merge branchName** : 合併分支  
> **git rebase branchName** : 在當前分支同步 branchName 的最後一個 commit 訊息 並接續當前分支的 commit 訊息後合併 branchName  
> **git fetch** : 檢查 遠端分支狀態  
> **git pull** : 同步遠端分支的內容到本地端分支  
> **git push origin branchName** : 推送(同步)到遠端 或 git push 就好  
> **git status (-s)** : 查看分支狀態 (查看已修改的檔案名稱)  
> **git tag (-d) tagName [-a -m 'The tag information']** : 在此 branch 的 commit 加上(刪除)輕量標籤 [ 加上有附註的標籤 ]  
> **git push origin 'tagName'** : 推 tagName 到 remote branch  
> **git push --delete origin tagName/branchName** : 刪除遠端 branch 的 tabName / 刪除遠端的 branch  
> **git reset --sort/--hard commitID** : 撤銷 commitID 之後的 commit 訊息 (撤銷 commit 的變更還在可重新 commit) / 撤銷 commitID 之後的 commit 訊息與變更  
> **git revert commitID** : 回復該 commitID 的變更，並新增該次操作的 commit 訊息(但不影響其他 commit)  
> **git cherry-pick (commit1 commit2...) [-no-commit ]** : 選取分支合併，[ 只是放到暫存區 ]  
> **git log [--pretty=oneline]**: 查看分支 commit 紀錄  
> **git show**: 查看分支 commit 紀錄，更動內容

> **git --help** : 查看指令
