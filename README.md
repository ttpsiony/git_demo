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

## bash command line

> **echo "file content" >> fileName** : 新增 內容為"file content" 的 fileName 檔案  
> **touch fileName** : 建立 fileName 檔案  
> **pwd** : 查看當前位置路徑  
> **cd ~path(/~path)(..)(-)** : 移動至相對路徑位置(絕對路徑位置)(回上層)(回上一次操作的位置)。  
> **ls** : 查看當前路徑下的 file 與 directory  
> **mkdir folderName** : 建立 folder[directory]  
> **rm fileName** : 刪除檔案  
> **rm -d(-r) folderName** : 只能刪除空的 folder(刪除整個資料夾內所有的東西 recursive)  
> **mv fileName ~path/fileName** : 移動檔案至路徑位置  
> **mv fileName newFileName** : 更新檔案名稱  
> **cp fileName ~path/fileName** : 複製檔案到路徑位置  
> **nano fileName** : 進入編輯檔案模式(也可以用 vim)  
> **env** :  列出所有環境變數  
> **alias e="env"** : 可以用自訂義代表該指令

## basic git command line

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
> **git fetch (origin branchName)** : 檢查 遠端(全部/branchName)分支狀態  
> **git pull** : 同步遠端分支的內容到本地端分支  
> **git push (-u) origin branchName** : 推送分支到遠端(並追蹤分支狀態) (-u 等同於 --set-upstream)  
> **git status (-s)** : 查看分支狀態 (查看已修改的檔案名稱)  
> **git tag (-d) tagName [-a -m 'The tag information']** : 在此 branch 的 commit 加上(刪除)輕量標籤 [ 加上有附註的標籤 ]  
> **git push origin 'tagName'** : 推 tagName 到 remote branch  
> **git push --delete origin tagName/branchName** : 刪除遠端 branch 的 tabName / 刪除遠端的 branch  
> **git tag -l <pattern>** : 查看(符合 pattern)的本地 tag 列表  
> **git ls-remote --tags <repository> (--ref)** : 查看 remote tag 列表(--tags 也可以是 -t)。 --ref 只回傳指向 tag object 的 ref，不會回傳取消 tag object ref 的最後一個 non-tag object  
> **git fetch --all -tags** : 檢查 遠端分支 tag 狀態  
> **git reset --sort/--hard commitID** : 撤銷 commitID 之後的 commit 訊息 (撤銷 commit 的變更還在可重新 commit) / 撤銷 commitID 之後的 commit 訊息與變更  
> **git revert commitID** : 回復該 commitID 的變更，並新增該次操作的 commit 訊息(但不影響其他 commit)  
> **git cherry-pick (commit1 commit2...) [-no-commit ]** : 選取分支合併，[ 只是放到暫存區 ]  
> **git log [--pretty=oneline]**: 查看分支 commit 紀錄  
> **git show**: 查看分支 commit 紀錄，更動內容

> **git --help** : 查看指令
