# Gitbook 發佈到 GitHub Pages

作法參考來源：[發布到 GitHub Pages - Chengwei's Blog](http://www.chengweiyang.cn/gitbook/github-pages/README.html)

- - -

GitHub Pages 簡單說就是一個可以託管靜態網站的 Git 項目，支持使用 markdown 語法以及 Jekyll 來構建，或者直接使用已經生成好的靜態站點。

構建好的書籍可直接放到 GitHub Pages 中託管後，再通過如下地址訪問書籍：
**<user_name>.github.io/<project_name>**

詳細可以參考 [GitHub Pages](https://pages.github.com/) 主頁。

- - -

## 建構書籍

使用 `gitbook build` 將書籍內容輸出到默認目錄 *_book* 底下。

    $ gitbook build

- - -

## 創建 gh-pages 分支

執行以下命令來創建分支，並且刪除不需要的文件：

```
$ git checkout --orphan gh-pages
$ git rm --cached -r .
$ git clean -df
$ rm -rf *~
```

現在，目錄下應該只剩下 *_book* 目錄，再來，忽略一些文件：

```
$ echo "*~" > .gitignore
$ echo "_book" >> .gitignore
$ git add .gitignore
$ git commit -m "Ignore some files"
```

然後，加入 *_book* 下的內容到分支中：

```
$ cp -r _book/* .
$ git add .
$ git commit -m "Publish book"
```

- - -

## 上傳書籍內容到 GitHub

將編譯好的書籍上傳到 GitHub 中 pepository 項目內的 gh-pages 分支，雖然這裡還沒有創建分支，上傳和創建會一步完成！

    $ git push -u origin gh-pages