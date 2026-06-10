# 个人官网 - 部署说明

## 📂 文件结构

```
website/
├── index.html          # 中文版首页
├── en/
│   └── index.html    # 英文版首页
├── images/
│   ├── lawn-mower-1.jpg  # 割草机图片
│   ├── lawn-mower-2.jpg
│   ├── lawn-mower-3.jpg
│   └── dyes-1.jpg        # 润彩染料图片
└── README.md          # 本文件
```

---

## 🚀 免费部署方案

### 方案 1：GitHub Pages（推荐）

#### 步骤 1：创建 GitHub 仓库
1. 登录 GitHub
2. 点击右上角 "+" → "New repository"
3. 仓库名：`brianfang.github.io`（必须这样命名）
4. 设置为 Public
5. 点击 "Create repository"

#### 步骤 2：上传文件
**方法 A：网页上传**
1. 进入仓库页面
2. 点击 "Add file" → "Upload files"
3. 上传整个 `website` 文件夹内容（注意：index.html 要在根目录）

**方法 B：Git 命令**
```bash
cd /root/.openclaw/workspace/website
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/brianfang/brianfang.github.io.git
git push -u origin main
```

#### 步骤 3：启用 GitHub Pages
1. 进入仓库设置（Settings）
2. 左侧菜单找到 "Pages"
3. Source 选择 "Deploy from a branch"
4. Branch 选择 "main" 和 "/ (root)"
5. 点击 Save

#### 步骤 4：访问网站
等待 1-2 分钟，访问：`https://brianfang.github.io`

---

### 方案 2：Vercel（更简单）

1. 注册 Vercel（用 GitHub 账号登录）
2. 点击 "Add New" → "Project"
3. 导入你的 GitHub 仓库
4. 点击 "Deploy"
5. 自动生成域名：`https://your-project.vercel.app`

---

## ✏️ 后续修改

### 修改个人简介
编辑 `index.html` 和 `en/index.html` 中的：
- 头像：替换 `<div style="width: 300px...>` 部分
- 个人介绍：修改 `<div class="about-content">` 中的 `<p>` 标签

### 修改产品图片
替换 `images/` 文件夹中的图片，保持文件名一致。

### 修改联系方式
编辑两个 HTML 文件中的：
- 邮箱：`brian715@163.com`
- LinkedIn：`https://www.linkedin.com/in/brianfang`

---

## 🔗 添加自定义域名（可选）

如果想用 `brianfang.com` 这样的域名：

### 1. 购买域名
推荐：
- 阿里云：https://wanwang.aliyun.com
- 腾讯云：https://dnspod.cloud.tencent.com
- 价格：约 ¥100/年

### 2. 配置 DNS
在域名服务商添加 CNAME 记录：
- 主机记录：`www`
- 记录类型：`CNAME`
- 记录值：`brianfang.github.io`（GitHub Pages）

### 3. 在 GitHub 配置自定义域名
1. 仓库 Settings → Pages
2. Custom domain 输入：`www.brianfang.com`
3. 点击 Save

---

## 📧 联系我

- Email: brian715@163.com
- LinkedIn: https://www.linkedin.com/in/brianfang

---

*最后更新：2026-06-08*
