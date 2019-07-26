# Gitbook

作法參考來源：[安裝 Gitbook - Chengwei's Blog](http://www.chengweiyang.cn/gitbook/installation/README.html)

- - -

## 安裝
使用 npm

    $ npm install gitbook -g

- - -

## 使用
初始化書籍目錄，僅支援兩級目錄

    $ gitbook init

編輯和預覽書籍

    $ gitbook serve
    
編譯書籍

    $ gitbook build

- - -

## 指令：gitbook init

首先，創建二個必須的文件
- **SUMMARY.md** 是書籍的目錄結構
- **README.md** 是書籍的簡單介紹

創建這兩個文件後，使用 `gitbook init`创建 **SUMMARY.md** 中的目錄結構。

- - -

## 指令：gitbook serve
書籍目錄結構創建完成以後，使用 `gitbook serve` 來編譯和預覽書籍。

`gitbook serve` 命令實際上會首先調用 `gitbook build` 命令編譯書籍，完成以後會打開一個 web 服務器，監聽在本地的 4000 端口。

在文件修改過程中，每一次保存文件，gitbook serve 會自動重新編譯，所以可以持續通過瀏覽器來查看最新的書籍修改！

- - -

## 指令：gitbook build
編譯書籍至 *_book* 目錄下