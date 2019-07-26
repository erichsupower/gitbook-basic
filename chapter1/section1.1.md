# Terminal及常用指令介紹
[Linux 常用 Terminal 命令與快捷鍵參考](https://www.evernote.com/l/AA5Dq3IjunxHkrRMRr0-CuMtc5IEDfRsYtw)

> 終端機（Terminal），其實是一個來自上一個世代的名詞。
> 
> 在那個時代的電腦很貴，不像現在幾乎每個人都有電腦可以用。公司內部通常會有一台大型的電腦主機，其它人要使用這部電腦就是自己拿螢幕跟鍵盤去接，然後在上面做事情，這些末端的操作設備便統稱之「終端機」。
> 
> 終端機本身通常不是一部電腦，它沒有運算能力，僅用來顯示資料及輸入資料，所有的計算都是在主機上處理的。

---

## 常用終端機命令列指令

| MacOS / Linux | 說明               |
| ------------- | ------------------ |
| cd            | 切換目錄           |
| pwd           | 取得目前所在的位置 |
| ls            | 列出目前的檔案列表 |
| mkdir         | 建立新的目錄       |
| touch         | 建立檔案           |
| cp            | 複製檔案           |
| mv            | 移動檔案           |
| rm            | 刪除檔案           |
| clear         | 清除畫面上的內容   |

---

## 目錄切換及顯示

##### 切換到 /tmp 目錄（絕對路徑）
    $ cd /tmp
    
##### 切換到 my_project 目錄（相對路徑）
    $ cd my_project
    
##### 往上一層目錄移動
    $ cd ..
    
##### 切換到使用者的 home 目錄中的 project 裡的 namecards 目錄，這個 ``~`` 符號表示 home 目錄
    $ cd ~/project/namecards/
    
##### 顯示目前所在目錄
    $ pwd
    /tmp

---

## 檔案列表

`ls` 指令可列出在目前目錄所有的檔案及目錄，後面可接的 `-al` 參數，
參數 `a` 是連**小數點開頭的檔案**也會顯示（例如.gitignore）
參數 `l` 則是完整檔案的權限、擁有者以及建立、修改時間

    $ ls -al

---

## 建立檔案、目錄

如果 index.html 這個檔案不存在，`touch` 指令會建立一個名為 index.html 的空白檔案；
如果本來就已經存在，則只會改變這個檔案的最後修改時間，不會變更原本這個檔案的內容。

`mkdir` 指令會在目前所在目錄，建立一個名為 demo 的目錄：

    $ mkdir demo
    
---

## 複製、更名、刪除

把檔案 index.html 複製一份成 about.html：

    $ cp index.html about.html

把檔案 index.html 更名成 info.html：

    $ mv index.html info.html

刪除檔案 index.html：

    $ rm index.html

刪除在這個目錄裡所有的 html 檔：

    $ rm *.html

---

## 字串輸出

`echo` 用來將字串輸出到終端上。它通常在shell指令碼和批次處理中使用，以將狀態資訊輸出到**螢幕**或**檔案**中。

以**覆蓋**的方式，將文字 "This is a test." 輸出到 "test.txt" 檔案中：

    $ echo "This is a test." > ./test.txt
    
以**加入**的方式，將文字 "This is a test." 輸出到 "test.txt" 檔案中：：

    $ echo "This is a test." > ./test.txt