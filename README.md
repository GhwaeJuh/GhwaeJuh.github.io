# 个人博客

使用 Jekyll 官方默认主题 [Minima 2.5.1](https://github.com/jekyll/minima/tree/v2.5.1)，保留原版布局和样式。主题以 MIT 许可证发布。本仓库通过 GitHub Actions 自动构建并发布到 GitHub Pages。

## 首次发布

1. 创建 GitHub 仓库。根域博客建议仓库名为 `你的GitHub用户名.github.io`；也支持 `blog` 等普通仓库名。
2. 将本目录内容（包括 `.github`）推送到仓库的 `main` 分支。
3. 进入 **Settings → Pages → Build and deployment → Source**，选择 **GitHub Actions**。
4. 如果首次自动运行失败，在 **Actions → Publish blog to GitHub Pages → Run workflow** 重新运行。
5. 等待部署完成，在 Settings → Pages 查看访问地址。

工作流自动设置域名和子路径，普通项目仓库也能正确加载链接和样式。

## 写文章

在 `_posts` 新建 `YYYY-MM-DD-英文文章名.md`：

```markdown
---
layout: post
title: "文章标题"
date: 2026-10-03 14:00:00 +0800
categories: 学习
---

文章摘要。

## 正文标题

正文内容。
```

提交后自动更新。不要使用晚于当前时间的日期，否则 Jekyll 会将它视为未来文章而暂不发布。

`_drafts/article-template.md` 是草稿模板，默认不会发布。`_posts/2026-10-03-hello-blog.md` 是可删除的示例文章。

## 修改博客信息

- `_config.yml`：博客名称、简介、导航。
- `about.md`：关于页面。
- `archive.html`：文章归档。
- 不设置评论系统、统计或外部个人资料。

## 本地预览

安装 Ruby 和 Bundler，然后执行：

```bash
bundle install
bundle exec jekyll serve
```

访问终端给出的地址。草稿预览使用 `bundle exec jekyll serve --drafts`。
