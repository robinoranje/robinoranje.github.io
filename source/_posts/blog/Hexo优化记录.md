---
title: Hexo优化记录
date: 2018-11-30 10:42:03
categories: note
tags:
---

## Next主题

### 首页字数显示限制

* 将`/themes/next/_config.yml`的`auto_excerpt`设为true，并调整`length`值控制字数
*但对内含代码片段的文章，暴力截断并不合适*

* 手工打标记截断
在文章中加入`<!-- more --> `标识，首页即可展示“阅读全文”入口

<!-- more -->

### 切换版式

在`/themes/next/_config.yml`切换Schemes完成

### 修改超链接的展示样式

主题源码中找到自定义样式配置文件`themes\next\source\css\_custom\custom.styl`，添加语句

```
.post-body p a {
    color: #0593d3;
    border-bottom: none;
    &:hover {
        color: #0477ab;
        text-decoration: underline;
    }
}
```

## 参考

[Hexo搭建的GitHub博客之优化大全](https://zhuanlan.zhihu.com/p/33616481)
[Hexo-Next-主题优化(二)](https://www.jianshu.com/p/428244cd2caa)
[Hexo博客设置进阶](http://blog.junyu.io/posts/0010-hexo-learn-from-Never-yu.html)
[Hexo主题设置和优化](http://www.vitah.net/posts/20f300cc/)