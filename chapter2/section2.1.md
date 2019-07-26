# npm 指令
Node Package Manager
Node 模組套件管理器

[npm 常用命令指南傳送門](https://www.eebreakdown.com/2016/09/npm.html)

## 版本號碼 `-v`

###### 印出版本資訊
    npm -v 

## 專案初始化 `init`

###### 安裝自定資訊
    npm init

###### 安裝預設資訊
    npm init -y

* name: 專案名稱，預設是專案目錄名
* description: 專案描述
* entry point: 專案切入點
* test command: 專案測試指令
* git repository: 原始碼版本控管位置
* keywoard: 專案關鍵字
* author: 專案作者，以 author-name <author@email.com> 寫之
* license: 專案版權

## package.json exsample

```
{
  "name": "gulp_sass",
  "version": "1.0.0",
  "description": "description content",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [],
  "repository": {
    "type": "git",
    "url": "https://github.com"
  },
  "author": "Eric Hsu",
  "license": "ISC",
  "devDependencies": {}
}
```

## 安裝套件 install


###### 依 package.json 內的配置檔紀錄自動安裝 
    npm install

###### 同上，但不安裝 “devDependencies” 的模組
    npm install --production

###### 若已安裝 devDependencies，可事後移除
    npm prune --production

###### 安裝全域中的套件
    npm install {package name} -g

###### 安裝專案中的套件
    npm install {package name}
    npm i {package name}

###### 安裝套件並自動寫入 package.json 的 “dependencies”
    npm install {package name} --save
    npm install {package name} -S

###### 安裝套件並自動寫入 package.json 的 “devDependencies"
    npm install {package name} --save-dev
    npm install {package name} -D

###### 安裝套件的最後版本，可搭配 -S 或 -D
    npm install {package name}@lastest

###### 安裝套件的特定版本，可搭配 -S 或 -D
    npm install {package name}@1.2.2

###### 安裝套件的特定版本，可搭配 -S 或 -D
    npm install {package name}@">=1.2.2"

###### 安裝 tagged 套件，可搭配 -S 或 -D
    npm install {package name}@stable

###### 安裝套件至自定目錄，預設為目錄 ./node_modules
    npm install {package name} --prefix./path/to/here 

###### 安裝套件，並在寫入 package.json 時，鎖定版本號。這樣在執行 npm update 時，該套件的版本就不會被升級
    npm install {package name} --save --save-exact
    npm install {package name} --save-dev --save-exact
    npm install {package name}@1.2.2 --save --save-exact


## 移除套件 uninstall

###### 移除全域中的套件
    npm uninstall {package name} -g

###### 移除專案中的套件
    npm uninstall {package name} 


## 移除不需要套件 prune

###### 加 —production，會移除 "devDependencies" 中的所有套件
    npm prune [--production] 

## 搜尋套件 search
    npm search {package name}

## 列出套件 ls

###### 列出全域中的套件
    npm ls -g
    
    
###### 列出專案中的使用套件
    npm ls
    
###### 列出專案中的使用套件
    npm list

## 檢查模組是否非最新版本 outdated
###### 檢查專案所使用的模組是否有過期者(非最新版本)
    npm outdated

## 更新套件 update

###### 更新全域中的套件
    npm update -g 
    
######  更新專案中套件
    npm update

######  只更新某個套件(package)
    npm update {package name} 

## 新增 npm 帳號 adduser
    npm adduser

## 登入 npm 帳號 login
    npm login

## 重新建置專案 rebuild
    npm rebuild

## 打包專案 pack
    npm pack