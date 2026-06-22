# 齐了！凑一桌 🎉

四个人的小博客，基于 Hexo + Fluid 主题搭建。

## 📁 项目结构

```
our-sweet/
├── source/
│   ├── _posts/          # 文章（Markdown格式）
│   ├── about/           # 关于页面
│   ├── admin/           # 可视化后台（Netlify CMS）
│   └── img/             # 图片资源
├── themes/              # 主题（自动安装）
├── _config.yml          # Hexo 主配置
├── _config.fluid.yml    # Fluid 主题配置
├── package.json         # 依赖配置
└── .github/workflows/   # 自动构建配置
```

## 🚀 快速开始

### 1. 初始化仓库

把这些文件推到你的 GitHub 仓库 `aoliao12112/our-sweet` 的 `main` 分支。

### 2. 开启 GitHub Pages

在仓库设置里：
- Settings → Pages
- Source 选择 `Deploy from a branch`
- Branch 选择 `gh-pages` / `/ (root)`
- 保存

### 3. 自动构建

已经配置好了 GitHub Actions，只要往 `main` 分支提交代码，就会自动构建并部署到 `gh-pages` 分支。

## ✍️ 怎么发帖子

### 方式一：GitHub 网页直接编辑（推荐，最简单）

四个人都能用，不用装任何软件：

1. 登录 GitHub，进入仓库
2. 进入 `source/_posts/` 目录
3. 点击 `Add file` → `Create new file`
4. 文件名：`文章标题.md`（比如 `我的第一篇文章.md`）
5. 按下面的格式写：

```markdown
---
title: 文章标题
date: 2026-06-22 15:30:00
categories: 分类名
tags:
  - 标签1
  - 标签2
author: 你的名字
---

这里写正文，用 Markdown 格式。

## 小标题

正文内容...

- 列表项1
- 列表项2
```

6. 拉到最下面点 `Commit changes` 提交
7. 等 1-2 分钟，自动构建完就能在博客上看到了！

**Markdown 很简单，常用的就几个：**
- `# 标题`、`## 二级标题`
- `**粗体**`、`*斜体*`
- `- 列表项`
- `[链接文字](网址)`
- `![图片描述](图片地址)`

---

### 方式二：可视化后台（Netlify CMS）

像发朋友圈一样填表单，但是需要额外配置认证。

**访问地址**：`https://aoliao12112.github.io/our-sweet/admin/`

**⚠️ 注意**：第一次用需要配置 GitHub OAuth 认证，配置方法：

1. 去 GitHub 申请一个 OAuth App：
   - Settings → Developer settings → OAuth Apps → New OAuth App
   - Application name: 随便填（比如"我们的博客"）
   - Homepage URL: `https://aoliao12112.github.io/our-sweet/`
   - Authorization callback URL: `https://aoliao12112.github.io/our-sweet/admin/`
   - 注册后会得到 Client ID 和 Client Secret

2. 部署一个 OAuth 认证服务（推荐用 Vercel 一键部署），或者用 Netlify 的 Git Gateway。

3. 配置好后就能用 GitHub 账号登录后台发帖了。

**如果觉得配置麻烦，直接用方式一就好，也很简单！**

## 🎨 本地预览（可选）

想在本地看效果的话：

```bash
# 安装依赖
npm install

# 启动本地服务器
npm run server

# 构建静态文件
npm run build
```

然后访问 `http://localhost:4000/our-sweet/` 就能看到效果。

## 📝 小贴士

- 文章开头的 `---` 之间的内容叫 Front Matter，是文章的元信息，不要删
- `date` 是发布时间，格式是 `YYYY-MM-DD HH:mm:ss`
- `categories` 是分类，一篇文章一个分类
- `tags` 是标签，可以有多个
- `author` 是作者名字，写上你是谁~

有问题就找管理员！🎉
