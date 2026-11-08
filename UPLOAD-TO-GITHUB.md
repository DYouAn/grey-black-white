# 上传到 GitHub

这个目录已经整理成可上传的 GitHub 仓库内容。我无法直接登录你的 GitHub 账号，所以下面两步需要你完成。

## 方式 A：网页上传（最简单）

1. 打开 https://github.com/new
2. Repository name 填：`grey-black-white`
3. 选择 **Public** 或 **Private**（要使用 GitHub Pages 当隐私政策 URL，需 Public，或使用其它公开网页托管）
4. 创建仓库。
5. 在仓库页面点击 **Add file → Upload files**，把本目录里的所有内容拖进去（注意不要上传 `.git` 目录）。
6. 提交，Commit message 可填 `Initial release v2.3.0`。
7. 打开 **Releases → Draft a new release**，Tag 填 `v2.3.0`，把 `dist/Grey-Black-White-v2.3.0.zip` 作为 release asset 上传。

## 方式 B：Git 命令

先设置你的 GitHub 用户名和邮箱（只在本仓库生效即可）：

```bash
git init -b main
git config user.name "你的名字"
git config user.email "你的GitHub邮箱"
git add .
git commit -m "Initial release v2.3.0"
git remote add origin https://github.com/你的用户名/grey-black-white.git
git push -u origin main
```

第一次 push 时 Git Credential Manager 会弹出浏览器登录 GitHub；登录后即可上传。

## 可选：启用 GitHub Pages（用于隐私政策 URL）

仓库 Settings → Pages：

- Source: **Deploy from a branch**
- Branch: `main`
- Folder: `/ (root)`
- 保存后等待部署，隐私政策 URL 为：
  `https://你的用户名.github.io/grey-black-white/privacy-policy.html`

把该 URL 填入 Edge Partner Center 的 Privacy policy URL 即可。

## 发布 Release

Tag `v2.3.0`，Release 标题 `Grey Black White v2.3.0`，上传：

- `dist/Grey-Black-White-v2.3.0.zip`

这样用户可以直接下载 zip，在 `edge://extensions/` 里加载。
