# Liu Chenyu — Academic Homepage

这是一个用于展示本科生学术身份的纯静态个人主页，可部署到 GitHub Pages，并作为 OpenReview 的 Homepage URL / Personal Link 使用。

## 文件

- `index.html`：主页内容
- `style.css`：页面样式
- `README.md`：部署说明

## 发布前检查

页面中的 GitHub 地址已经配置为：

```text
https://github.com/Liuchenyu-Jane
```

同时请检查姓名、学校、专业、邮箱和项目描述是否准确。不要添加不能公开验证的论文、奖项或经历。

## 上传到 GitHub

### 方法一：使用 GitHub 网站

1. 登录 [GitHub](https://github.com/)，点击右上角 `+`，选择 **New repository**。
2. 仓库名建议使用 `Liuchenyu-Jane.github.io`。
3. 将仓库设为 **Public**，然后点击 **Create repository**。
4. 在新仓库页面点击 **uploading an existing file** 或 **Add file → Upload files**。
5. 上传 `index.html`、`style.css` 和 `README.md`，填写提交说明后点击 **Commit changes**。

### 方法二：使用 Git 命令行

先在 GitHub 创建一个空的公开仓库，然后在本项目目录运行：

```bash
git init
git add index.html style.css README.md
git commit -m "Create academic homepage"
git branch -M main
git remote add origin https://github.com/Liuchenyu-Jane/Liuchenyu-Jane.github.io.git
git push -u origin main
```

如果当前目录已经是 Git 仓库，则不要重复执行 `git init`。如果已配置名为 `origin` 的远程仓库，也不要重复执行 `git remote add origin`；请先用 `git remote -v` 检查。

## 开启 GitHub Pages

1. 打开 GitHub 上的主页仓库。
2. 进入 **Settings → Pages**。
3. 在 **Build and deployment** 下，将 **Source** 选择为 **Deploy from a branch**。
4. 在 **Branch** 中选择 `main` 和 `/ (root)`，然后点击 **Save**。
5. 等待几分钟，刷新 Pages 设置页，GitHub 会显示已发布的网址。

如果仓库名是 `Liuchenyu-Jane.github.io`，主页为：

```text
https://Liuchenyu-Jane.github.io/
```

如果使用普通仓库名（例如 `academic-homepage`），网址通常为：

```text
https://Liuchenyu-Jane.github.io/academic-homepage/
```

## 在 OpenReview 中填写哪个 URL

先用浏览器打开 GitHub Pages 地址，确认页面可以公开访问，并且页面上能清楚看到姓名 **Liu Chenyu**、学校和邮箱。然后在 OpenReview 的个人资料中，将这个完整的公开地址填入 **Homepage URL** 或 **Personal Links**：

```text
https://Liuchenyu-Jane.github.io/
```

不要填写 GitHub 仓库编辑页面、仓库的 `Settings` 地址、本地文件路径，或只有你自己能访问的预览地址。

## 本地预览

直接双击 `index.html` 即可在浏览器中预览。也可以在项目目录启动一个本地服务器：

```bash
python -m http.server 8000
```

然后访问 `http://localhost:8000/`。
