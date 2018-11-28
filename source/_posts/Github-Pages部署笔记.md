---
title: Github Pages部署笔记
date: 2018-11-28 12:14:16
tags: [git]
---

## SSH Keys
### 生成与添加Key
```
cd ~/.ssh
ssh-keygen -t rsa -C “test@info.net”
```

将id_rsa.pub文件中的内容添加到Github-Setting-SSH Keys

### 测试是否配置成功
```
ssh -T git@github.com
```

如果返回`Hi username! You've successfully authenticated, but GitHub does not provide shell access.`说明成功

如果不成功，可用`ssh -T -v git@github.com`查看报错详情

## 创建仓库
按照提示初始化，关键命令：
```
echo "# blog" >> README.md 
git add README.md 
git commit -m 'first commit' 
git remote add origin git@github.com:xxxxxxx/xxxx.git
```

仓库名需为 username.github.io
如果需要修改origin，可用
```
git remote set-url origin https://github.com/xxxxxx/xxxx.git 
```
命令

## 创建Pages
仓库对应的Setting中`GitHub Pages`编辑项，可修改主题等


## 参考
[使用GitHub.io当作自己的博客网站 - 看山 看水 看世界 - CSDN博客](https://blog.csdn.net/tyyytcj/article/details/80880018)