# tashan-12.github.io

基于 Hexo + GitHub Actions 的个人博客，源码在 `hexo` 分支，部署在 `main` 分支。

## 工作机制

| 分支 | 内容 | 维护方式 |
|---|---|---|
| `hexo` | Hexo 源码、文章 Markdown、Actions 配置 | 手动 push |
| `main` | 构建产物（静态站点） | Actions 自动推送 |

push 到 `hexo` 分支后，`.github/workflows/deploy.yml` 自动执行 `hexo generate`，并把 `public/` 强推到 `main` 分支，GitHub Pages 随即更新。

## 写新文章

1. 在 `source/_posts/` 下新建 `标题.md`
2. Front Matter 模板：

```yaml
---
title: 文章标题
date: 2025-07-01 10:00:00
tags:
  - 标签
---
```

3. `git push origin hexo`，等 Actions 跑完即可访问 https://tashan-12.github.io/

## 本地预览

```bash
npm install
npx hexo server   # http://localhost:4000
```

## 从本地笔记导入

把 `notes-export/` 等目录下的 Markdown 复制到 `source/_posts/`，补上 Front Matter 即可。
