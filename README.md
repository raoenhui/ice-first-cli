# 创建脚手架 cli 入门教程

## 第一步 创建仓库

创建一个git仓库，可以在GitHub创建个git仓库，如[https://github.com/raoenhui/ice-first-cli](https://github.com/raoenhui/ice-first-cli)

## 第二步 编辑package

npm init 或直接创建package.json,将git仓库地址加入

``` json
{
  "name": "ice-first-cli",
  "version": "1.0.8",
  "scripts": {
    "test": "npm -v"
  },
  "bin": {
    "ice-first-cli": "./bin/commit.js"
  },
  "repository": {
    "type": "git",
    "url": "git+https://github.com/raoenhui/ice-first-cli.git"
  },
  "keywords": [
    "cli"
  ],
  "devDependencies": {
    "shelljs": "^0.8.1"
  }
}
```

## 第三步 创建bin文件

创建bin文件夹，在bin中再创建commit.js文件。
```
#! /usr/bin/env node
var shell = require("shelljs");
shell.exec("echo shell.exec works1");
console.log('my first cli');     
```

## 第四步 测试cli

控制台输入
```
sudo npm link
ice-first-cli
npm publish
```
![cli.png](http://upload-images.jianshu.io/upload_images/9902136-732fa32306001121.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

## 第五步 完成

可从npm官网中找到，[https://www.npmjs.com/package/ice-first-cli](https://www.npmjs.com/package/ice-first-cli) .

