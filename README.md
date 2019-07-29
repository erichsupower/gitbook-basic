# Markdown Syntax

[線上 Markdown 資源文件](https://markdown.tw/)

This is an H1
=============

This is an H2
-------------

# This is an H1
## This is an H2
### This is an H3
#### This is an H4
##### This is an H5
###### This is an H6

## 區塊引言

> 區塊引言
> 區塊引言
> > 區塊引言

> 區塊引言區塊引言區塊引言區塊引言區塊引言區塊引言區塊引言區塊引言區塊引言區塊引言區塊引言區塊引言區塊引言區塊引言區塊引言區塊引言區塊引言區塊引言區塊引言

> 區塊引言區塊引言區塊引言區塊引言區塊引言區塊引言區塊引言區塊引言區塊引言區塊引言區塊引言區塊引言區塊引言區塊引言區塊引言區塊引言區塊引言區塊引言區塊引言

## 清單

*   無序清單使用星號、加號或是減號作為清單標記
*   無序清單使用星號、加號或是減號作為清單標記
*   無序清單使用星號、加號或是減號作為清單標記

+   無序清單使用星號、加號或是減號作為清單標記
+   無序清單使用星號、加號或是減號作為清單標記
+   無序清單使用星號、加號或是減號作為清單標記

-   無序清單使用星號、加號或是減號作為清單標記
-   無序清單使用星號、加號或是減號作為清單標記
-   無序清單使用星號、加號或是減號作為清單標記

1.  有序清單則使用數字接著一個英文句點
2.  有序清單則使用數字接著一個英文句點
3.  有序清單則使用數字接著一個英文句點

## 分隔線

* * *
***
*****
- - -
---
---------------------------------------

## 程式碼區塊

    This is a code block.
    This is a code block.
    This is a code block.
    
```
This is a code block.
This is a code block.
This is a code block.
```
    
## 程式碼

Use the `printf()` function.

``There is a literal backtick (`) here.``

`&#8212;` is the decimal-encoded equivalent of `&mdash;`.

## 連結

###### Markdown 支援兩種形式的連結語法：行內和參考兩種形式。
This is [an example](http://example.com/ "Title") inline link.
[This link](http://example.net/) has no title attribute.

###### 如果你是要連結到同樣主機的資源，你可以使用相對路徑：
See my [About](/about/) page for details.  

###### 參考形式的連結使用另外一個方括號接在連結文字的括號後面，而在第二個方括號裡面要填入用以辨識連結的標籤：
This is [an example] [id] reference-style link.

[id]: http://example.com/  "Optional Title Here"

下面這三種連結的定義都是相同：
[foo]: http://example.com/  "Optional Title Here"
[foo]: http://example.com/  'Optional Title Here'
[foo]: http://example.com/  (Optional Title Here)

###### 簡短的自動連結形式來處理網址和電子郵件信箱：
<http://example.com/>
<address@example.com>

## 強調

*single asterisks*
_single underscores_
**double asterisks**
__double underscores__

## 圖片

![Alt text](./images/208x128.png)

![Alt text](https://markdown.tw/images/208x128.png "Optional title")

![Alt text][idImage]

[idImage]:images/208x128.png

## 跳脫字元

###### 利用反斜線來插入一些在語法中有其他意義的符號
\*literal asterisks\*

## 表格
[Markdown Tables generator](https://www.tablesgenerator.com/markdown_tables)

| A | B | C | D | E |
|---|---|---|---|---|
| 1 | 2 | 3 | 4 | 5 |
| 1 | 2 | 3 | 4 | 5 |
| 1 | 2 | 3 | 4 | 5 |