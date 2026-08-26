# 汪洋的 Astro 博客

这是 `sophistwy.com` 的 Astro 迁移版本：文章使用 Markdown/MDX 管理，静态构建后部署到 GitHub Pages。

## 本地开发

```bash
npm install
npm run dev
```

## 发布文章

最简单的方式是在 `src/content/posts/` 新建 Markdown 文件：

```md
---
title: 我的新文章
description: 一句话摘要
pubDate: 2026-08-26
category: iOS
tags: [iOS, Swift]
---

正文从这里开始。
```

提交到 `main` 后，GitHub Actions 会自动构建并发布。

项目也预留了 `/admin/` 的 GitHub CMS 配置。将 `public/admin/config.yml` 中的 `repo` 改成实际仓库后，就可以在浏览器中创建文章。

## 迁移说明

- 已导入线上站点公开的 40 篇文章内容；
- 新文章地址为 `/posts/<slug>/`；
- 已为现有文章生成部分旧 `/年/月/日/标题/` 兼容入口；
- `public/CNAME` 保留了 `www.sophistwy.com`。
