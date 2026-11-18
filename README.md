# 武明信个人主页 · 发布指南

## 文件说明

| 文件 | 用途 |
|---|---|
| `index.html` | **桌面版**（230 KB）。手机访问会自动跳转到 `m.html`。海洋蓝主题，含波浪背景。 |
| `m.html` | **手机专用版**（234 KB）。底部固定导航、竞赛折叠、触控优化。 |
| `photo.jpg` | 证件照（已内嵌进两个 HTML，此文件备用）。 |
| `logo.jpg` | BRMI Lab 标识（已内嵌，此文件备用）。 |

两个 HTML 都是**单文件、无外部依赖**，所有图片均已 base64 内嵌，上传时只需传 HTML 文件即可。

---

## 方案 A：GitHub Pages（推荐，免费、永久、学术圈最常用）

**第 1 步**：打开 [github.com/new](https://github.com/new)，新建一个公开仓库，名称建议 `mingxinwu.github.io`（这样网址就是 `https://mingxinwu.github.io`）。

**第 2 步**：进入仓库 → 点击 **Add file → Upload files**，把本目录下的 `index.html` 和 `m.html` 拖进去，点 **Commit changes**。

**第 3 步**：进入 **Settings → Pages → Source**，选择 **Deploy from a branch → main / root**，点 Save。等 1–2 分钟。

**完成**：访问 `https://mingxinwu.github.io` 即可。手机打开会自动进入手机版，电脑打开就是桌面版。

> 如果以后更新：直接在本机修改 `生成主页.py` → 重新运行 → 把新生成的 `index.html` 和 `m.html` 覆盖上传到 GitHub，1 分钟后自动刷新。

---

## 方案 B：Vercel（最快，拖拽即部署）

1. 打开 [vercel.com](https://vercel.com)，用 GitHub 账号登录。
2. 点击 **Add New… → Project**，导入刚才的 GitHub 仓库，点 Deploy。
3. 自动获得 `https://xxx.vercel.app` 链接，国内访问可能需要 CDN 加速。

---

## 方案 C：Netlify（同样拖拽）

1. 打开 [netlify.com](https://netlify.com)，登录。
2. 把本文件夹直接拖进 Netlify 首页的虚线框，立即生成链接。

---

## 手机版与桌面版的切换

- 手机访问 `index.html` 会自动跳转到 `m.html`。
- 如果想在手机上看桌面版，在地址栏末尾加 `?desktop=1` 即可阻止跳转。
- `m.html` 底部有 5 个固定导航按钮（首页 / 论文 / 项目 / 概况 / 联系），方便快速跳转。

---

## 更新后重新生成

```bash
cd "D:/workbudy/个人学术档案库/个人主页"
python 生成主页.py
```

运行后会同时更新 `index.html`（桌面版）和 `m.html`（手机版），然后重新上传即可。

---

*生成时间：2026 年 11 月 18 日*
