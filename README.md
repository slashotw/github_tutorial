# github_tutorial
通用版github教學 for喵ㄉgithub課

## 前言
### 何乃github?
線上軟體原始碼代管服務平台，aka：工程師的臉書、開源軟體聚集地、~~炫耀程式平台~~。
### 跟gitㄉ關係
github透過 Git 進行版本控制


## *tasks*
1. 創立github帳號
2. 建立你的第一個repository！(用本名開repo)
3. ~~star這篇文章~~


## 小功能
* Watch（關注）
* Star（給星星） 
* Fork（複製一份到你的帳號）

## Repo
全名為repository
* Code
    * 就是你這個branch下的code，可以透過左上切換各種Branches
* Issue
    * 對這個Repo有任何問題都可以在issue提出，未解決的則是Open
    * 在問問題前先看一下close有沒有解
* Pull Requests(PR)
    * 讓作者知道你fork了一個並做了一些修改 看要不要合併(merge)
* Actions
    * Actions 讓你可以在存放程式碼的地方自動化程式碼部署的工作流程，Actions可以理解為單獨的流程，Workflow則為多個Action部屬的合集
* Projects
    * 規劃專案、排序任務、追蹤任務狀態、分享狀態等等
* Wiki
    * 類似託管文檔的功能
* Security
    * 可以傳遞你Security方面訊息，或者回報漏洞的地方
* Insights
    * 分析數據
#### 特殊的Repo
假設你的名稱叫kevin123
* kevin123
    * 個人首頁
    * [範例](https://github.com/KvN1027/KvN1027) 
* kevin123.github.io 
    * 靜態網頁，可以把自己的靜態網站託管在那邊
    * [範例](https://github.com/KvN1027/KvN1027.github.io)

## 把code丟上去
### way1: add files
upload 或者 creat new files
### way2: git command
[Git安裝](https://git-scm.com/downloads)

先新增一個資料夾 作為專案的根目錄，之後開始尻下面的GIT Command

創立一個README.md檔案
```
echo "# 隨便寫點東西" >> README.md
```
將該資料夾做初始化，創建一個.git資料夾(看不到：檔案總管上方檢視>右邊隱藏的項目打勾)
```
git init
```

add就是把這個檔案加入staging area(索引)，否則的話這個檔案就不會被commit，若是要一次把所有檔案都加入的話則為`git add .`
```
git add README.md
```
把已經建立索引的檔案提交至本地資料庫(Local Repository)，"first commit"那邊則是填寫關於這個commit的相關訊息 打啥都行
```
git commit -m "first commit"
```
建立一個分支，這個打一次就行 不用每次commit都打一次
```
git branch -M main
```
添加遠端的資料庫，意思就是跟你這個github repo連線
```
git remote add origin https://github.com/KvN1027/sad.git
```
上傳指定分支(main)到github目錄
```
git push -u origin main
```
#### 初始完了方丈，那我下次更改檔案後該如何丟上去呢方丈
可以先用`git status`，確認一下有沒有新增的檔案沒add到(檔名會標紅字在untracked files那邊)
確認ok的話就
```
git commit -m "first commit"
```
再來就
```
git push -u origin main
```
完成(ﾉ>ω<)ﾉ
