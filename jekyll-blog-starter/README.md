# Jekyll 博客最小骨架（3 分区 + Disqus 游客评论）

> 直接把整个目录上传到你的 GitHub 仓库：`YOUR_GITHUB_USERNAME.github.io`

## 使用步骤

### 1) 替换两个占位符
- 打开 `_config.yml`，将 `url:` 改为：`https://YOUR_GITHUB_USERNAME.github.io`
- 打开 `_includes/disqus.html`，将 `YOUR_SHORTNAME` 改为你在 Disqus 中创建站点得到的 shortname

### 2) 推送到 GitHub
- 仓库名必须为：`YOUR_GITHUB_USERNAME.github.io`
- 推送到 `main` 分支

### 3) 开启 GitHub Pages
- 仓库 → Settings → Pages → Build and deployment
  - Source: Deploy from a branch
  - Branch: main
  - Folder: /(root)

几分钟后访问：`https://YOUR_GITHUB_USERNAME.github.io`

### 4) 在 Disqus 开启“游客可评论”
- 登录 Disqus → Settings → Moderation → 打开 **Guest Commenting**

### 5) 写新文章
在 `_posts/` 下新建：`YYYY-MM-DD-title.md`，示例 front matter：
```yaml
---
layout: post
title: "文章标题"
date: 2025-11-02
categories: [随笔]   # 或 [技术] / [公告]
comments: true
---
正文...
```

## 可选
- 自定义域名：在仓库根目录新建 `CNAME` 文件（内容为你的域名），并在 GitHub Pages 设置里绑定。
- 本地预览：
  ```bash
  bundle install
  bundle exec jekyll serve
  ```
  打开 http://127.0.0.1:4000 预览。
