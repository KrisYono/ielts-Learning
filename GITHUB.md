# 上传到 GitHub

本地已经完成：`git init`、首次提交。

## 你需要做的（二选一）

### 方法一：在网页上创建仓库后推送（推荐）

1. 打开 [GitHub → New repository](https://github.com/new)。
2. **Repository name**：填一个名字，例如 `ielts-learning` 或 `Ielts-Learning`。
3. 选 **Public**，**不要**勾选 "Add a README"（我们本地已有）。
4. 点 **Create repository**。
5. 在项目文件夹里打开终端，执行（把 `你的用户名` 和 `仓库名` 换成你的）：

```powershell
cd "c:\Users\yunu2\Desktop\Ielts Learning"
git remote add origin https://github.com/你的用户名/仓库名.git
git branch -M main
git push -u origin main
```

例如仓库是 `KrisYono/ielts-Learning`，则：

```powershell
git remote add origin https://github.com/KrisYono/ielts-Learning.git
git branch -M main
git push -u origin main
```

（当前项目已用 HTTPS 推送到该仓库；若你未配置 SSH，用 HTTPS 即可。）

### 方法二：用 GitHub CLI 创建并推送

若已安装 [GitHub CLI](https://cli.github.com/) 且已登录：

```powershell
cd "c:\Users\yunu2\Desktop\Ielts Learning"
gh repo create ielts-learning --public --source=. --remote=origin --push
```

（会创建名为 `ielts-learning` 的公开仓库并自动推送。）

---

推送时如要求登录，按提示用浏览器或 Personal Access Token 即可。
