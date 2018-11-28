---
title: Hexo新手记录
date: 2018-11-28 15:54:45
categories: note
tags:
---

## 初始化

```
npm install hexo-cli -g
hexo init blog
cd blog
npm install
hexo server
```

## 本地运行

```
hexo server
```
自定义端口
```
hexo server -p 5000
```

## 创建新文章

```
 hexo new "My New Post"
```

## 部署(git)

```
npm install --save hexo-deployer-git
```

`_config.yml `文件中修改对应配置

```
hexo deploy
```

[部署 | Hexo](https://hexo.io/zh-cn/docs/deployment)

## 备份源文件
可使用`hexo-git-backup`插件

备份前，应建好相应备份分支，并将其设为默认分支

如果报错
```
fatal: 'github' does not appear to be a git repository
fatal: Could not read from remote repository.
```
可以在blog目录中执行`git remote add`操作

备份命令
```
hexo backup
```

## 更换主题(Next为例)

### 基本配置

项目目录下执行

```
git clone https://github.com/theme-next/hexo-theme-next themes/next
```
在`_config.yml`站点配置文件中，配置
```
theme:next
language: zh-CN
```

### 支持标签

```
hexo new page tags 
```

md中tag写法

```
tags: [tag1,tag2]
```

`tags/index.md`中添加`type: "tags"`配置

### 支持分类

```
 hexo new page categories
```

md中tag写法
```
categories: cate1
```

`categories/index.md`中添加`type: "categories"`配置


## 简写命令

```
hexo g
hexo d
hexo b
```

## 参考

[我的个人博客之旅：从jekyll到hexo - WordZzzz - CSDN博客](https://blog.csdn.net/u011475210/article/details/79023429)
[Hexo](https://hexo.io/zh-cn/)
[GitHub - coneycode/hexo-git-backup: you can use it to backup your blog into git.](https://github.com/coneycode/hexo-git-backup)
[does not appear to be a git repository · Issue #26 · coneycode/hexo-git-backup · GitHub](https://github.com/coneycode/hexo-git-backup/issues/26)
[Next主题](http://theme-next.iissnan.com/getting-started.html)
[Next配置](https://www.jianshu.com/p/21c94eb7bcd1)