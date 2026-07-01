---
title: Hello World
date: 2025-04-10 22:51:14
tags:
  - 测试
---

欢迎来到我的博客！这是一篇由 Hexo 驱动的示例文章。

站点已迁移到 GitHub Actions 自动构建流程：

1. 在 `hexo` 分支的 `source/_posts/` 下写 Markdown
2. push 后 Actions 自动运行 `hexo generate`
3. 生成结果自动推送到 `main` 分支，GitHub Pages 随即更新

## 写新文章

在 `source/_posts/` 下新建 `你的标题.md`，文件头使用 Front Matter：

```yaml
---
title: 文章标题
date: 2025-07-01 10:00:00
tags:
  - 标签1
  - 标签2
---
```

正文用 Markdown 编写即可。
