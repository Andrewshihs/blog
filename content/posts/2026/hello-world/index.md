---
title: "Hello World — 博客搭建记录"
date: "2026-09-21T23:00:00+08:00"
draft: false
tags: ["博客", "Hugo", "EdgeOne"]
categories: ["技术"]
summary: "第一篇博客，记录基于 Hugo + EdgeOne Makers 搭建个人博客的全过程。"
---

## 动机

一直想有一个属于自己的写作空间。试过知乎、微信公众号、Notion，但总感觉少了点「自己的地盘」的味道。

于是，就有了这个博客。

## 技术选型

### Hugo

选 Hugo 的理由很简单：**快**。

一个几百篇文章的站点，Hugo 构建时间以毫秒计。Go 语言写的，单二进制文件，没有运行时依赖。

我用的是 [PaperMod](https://github.com/adityatelange/hugo-PaperMod) 主题——极简、快速、13k GitHub Star，社区足够大，踩坑不愁。

### EdgeOne Makers

之前也考虑过 Vercel、Cloudflare Pages、GitHub Pages。最后选了 EdgeOne Makers：

- **国内访问快**：腾讯云 CDN 节点覆盖好
- **一站式**：托管 + CDN + HTTPS 一个平台搞定
- **免费额度**：个人博客够用
- **边缘函数**：后续可以加评论系统、表单处理等动态功能

### GitHub Actions

写完文章 `git push`，剩下的自动完成：

```
推送代码 → GitHub Actions 触发 → Hugo 构建 → 部署到 EdgeOne Makers
```

真正的「写完就发」。

## 接下来

- [ ] 迁移旧文章
- [ ] 接入评论系统（Giscus）
- [ ] 加入搜索功能
- [ ] 图片 CDN 优化
- [x] ~~把博客搭起来~~ ✅

---

> 种一棵树最好的时间是十年前，其次是现在。