# git simple cheat sheet

## Init Git Repository

```
echo "# git_demo" >> README.md
git init
git add README.md
git commit -m "commit message..."
git branch -M master
git remote add origin "your repository"
git push -u origin master
```

## Bash Command Line

> **echo "file content" >> fileName** : 新增 內容為"file content" 的 fileName 檔案  
> **man (command)** : 查看指令的說明  
> **touch fileName** : 建立 fileName 檔案  
> **pwd** : 查看當前位置路徑  
> **cd ~path(/~path)(..)(-)** : 移動至相對路徑位置(絕對路徑位置)(回上層)(回上一次操作的位置)  
> **ls (~path)(/~path) (-a) (-l)** : 查看當前路徑(相對路徑或絕對路徑)下的 file 與 directory。 -a 包含隱藏檔。-l 較多資訊  
> **mkdir folderName** : 建立 folder[directory]  
> **rm fileName** : 刪除檔案  
> **rm -d(-r) folderName** : 只能刪除空的 folder(刪除整個資料夾內所有的東西 recursive)  
> **mv fileName ~path/fileName** : 移動檔案至路徑位置  
> **mv fileName newFileName** : 更新檔案名稱  
> **cp fileName ~path/fileName** : 複製檔案到路徑位置  
> **nano fileName** : 進入編輯檔案模式(也可以用 vim)  
> **env** : 列出所有環境變數  
> **alias e="env"** : 可以用自訂義代表該指令

## Basic Git Command Line

> **git branch master** : 建立新分支(不切換)  
> **git branch (-r, -a)** : 查看所有本地分支 (遠端分支, 全部分支)  
> **git branch (-r) -d branchName** : 刪除(遠端)本地分支  
> **git checkout branchName** : 切換分支  
> **git checkout -b branchName** : 新創分支並切換  
> **git checkout -b branchName origin/branchName** : 從遠端複製分支  
> **git checkout -t origin/branchName** : 從遠端複製分支，並追蹤遠端分支  
> **git switch branchName** : 切換分支  
> **git add . (-p)** : 確認所有變更(git add --all 類似) 或 可以選擇特定檔案(git add fileName)。 -p 可以選擇部分變更加到本次 commit 紀錄  
> **git commit -m 'commit message'** : 寫這次變更的註解  
> **git merge branchName** : 合併分支  
> **git rebase branchName** : 在當前分支同步 branchName 的最後一個 commit 訊息 並接續當前分支的 commit 訊息後合併 branchName  
> **git fetch (origin branchName)** : 檢查 遠端全部(origin branchName)分支狀態  
> **git pull** : 同步遠端分支的內容到本地端分支  
> **git push (-u) origin branchName** : 推送分支到遠端(並追蹤分支狀態) (-u 等同於 --set-upstream)  
> **git status (-s)** : 查看分支狀態 (查看已修改的檔案名稱)  
> **git tag (-d) tagName (-a -m 'The tag information')** : 在此 branch 的 commit 加上(刪除)輕量標籤 (加上有附註的標籤)  
> **git push origin 'tagName'** : 推 tagName 到 remote branch  
> **git push --delete origin tagName/branchName** : 刪除遠端 branch 的 tabName / 刪除遠端的 branch  
> **git tag -l `<pattern>`** : 查看(符合 pattern)的本地 tag 列表  
> **git ls-remote --tags `<repository>`** : 查看 remote tag 列表(--tags 也可以是 -t)。  
> **git fetch --all -tags** : 檢查 遠端分支 tag 狀態  
> **git reset --sort/--hard commitID** : 撤銷 commitID 之後的 commit 訊息 (撤銷 commit 的變更還在可重新 commit) / 撤銷 commitID 之後的 commit 訊息與變更  
> **git revert commitID** : 回復該 commitID 的變更，並新增該次操作的 commit 訊息(但不影響其他 commit)  
> **git restore . (~path/filename) (--source=HEAD~1)** : 撤銷工作區所有文件的修改 (路徑的某檔案) (將工作區內容切換到上個 commit 版本)  
> **git cherry-pick [commit1-SHA commit2-SHA...] (-no-commit)** : 選取分支合併，(只是放到暫存區)  
> **git format-patch [-n] [commit1-SHA..commit2-SHA] -o ~path**： 產生最新(n 次) (從 commit1-SHA 之後但不包含 到 commit2-SHA) 的 commit 紀錄的更新檔，到 ~path 的位置  
> **git am ~path**： 使用 ~path 的更新檔  
> **git stash (push/list/pop/apply/drop/clear) stash@{n} [save 'message']**：暫存當前目錄 push 可省略/顯示列表/還原暫存並移除暫存紀錄/還原暫存但暫存紀錄還在/清除最新暫存/清除全部暫存，指定暫存檔案的地 n 筆，預設為第一筆，save 可以寫該暫存紀錄的訊息  
> **git log (--pretty=oneline)**: 查看分支 commit 紀錄  
> **git reflog**: 查看分支歷史紀錄  
> **git show**: 查看分支 commit 紀錄，更動內容

> **git --help** : 查看指令

## Commit Message

- Header: `<type>` `<subject>`
  - `<type>`: 代表此 commit 類型，如：feat, fix, refactor, test, chore, revert 等。
  - `<subject>`: 代表此 commit 簡短描述

> **feat** : 為新增或修改功能時  
> **fix** : 為修  補功能錯誤(bug)時  
> **refactor** : 重構程式碼架構(不是修增或修補功能時)  
> **test** : 增加測試時  
> **chore** : 建構程序或輔助工具時(例如：新增 release 版本紀錄、更新程式執行環境、升級套件版本 )  
> **revert** : 撤銷先前 commit 紀錄時  
> **docs** : 撰寫文件時(例如：新增、移除註解)  
> **style** : 格式改變但不影響程式變動(例如：formatting、white-space)  
> **pref** : 改善效能

- Body:
  - Body 部份是對本次 Commit 的詳細描述
  - 可以分成多行

more information: [AngularJS Git Commit Message Conventions](https://docs.google.com/document/d/1QrDFcIiPjSLDn3EL15IJygNPiHORgU1_OOAqWjiDU5Y/edit#heading=h.uyo6cb12dt6w)
