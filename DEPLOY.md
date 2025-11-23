# GitHub Pages 部署指南

## 方法一：使用命令行（推荐）

### 1. 初始化 Git 仓库

打开终端（PowerShell 或 CMD），进入项目目录，然后运行：

```bash
cd "d:\StudyProject\新建文件夹"
git init
```

### 2. 添加所有文件

```bash
git add .
```

### 3. 提交文件

```bash
git commit -m "Initial commit: Academic homepage"
```

### 4. 在 GitHub 上创建新仓库

1. 访问 https://github.com/new
2. **仓库名称**：
   - 如果想用 `https://你的用户名.github.io` 访问，仓库名必须是：`你的用户名.github.io`
   - 否则可以任意命名，如：`academic-homepage`
3. 选择 **Public**（公开）
4. **不要**勾选 "Add a README file" 或 "Add .gitignore"
5. 点击 **Create repository**

### 5. 连接本地仓库到 GitHub

将 `你的用户名` 和 `仓库名` 替换为实际值：

```bash
git remote add origin https://github.com/你的用户名/仓库名.git
git branch -M main
git push -u origin main
```

如果遇到认证问题，可能需要：
- 使用 GitHub Personal Access Token
- 或配置 SSH 密钥

### 6. 启用 GitHub Pages

1. 进入你的 GitHub 仓库页面
2. 点击 **Settings**（设置）
3. 在左侧菜单找到 **Pages**
4. 在 "Source" 下：
   - 选择 **Deploy from a branch**
   - Branch 选择 **main**
   - Folder 选择 **/ (root)**
5. 点击 **Save**

### 7. 等待部署完成

- 通常 1-2 分钟后即可访问
- 如果仓库名是 `你的用户名.github.io`，访问：`https://你的用户名.github.io`
- 如果仓库名是其他名称，访问：`https://你的用户名.github.io/仓库名`

---

## 方法二：使用 GitHub 网页界面（更简单）

### 1. 创建新仓库

访问 https://github.com/new，创建一个新仓库。

### 2. 上传文件

1. 在仓库页面，点击 **"uploading an existing file"** 或 **"Add file" → "Upload files"**
2. 将以下文件拖拽到页面：
   - `index.html`
   - `style.css`
   - `script.js`
   - `profilepic.jpg`
   - `README.md`
   - `.gitignore`（如果有）
3. 点击 **Commit changes**

### 3. 启用 GitHub Pages

1. 进入 **Settings** → **Pages**
2. Source 选择 `main` 分支，Folder 选择 `/ (root)`
3. 点击 **Save**

### 4. 访问你的主页

等待几分钟后访问你的主页地址。

---

## 更新内容

以后如果需要更新内容：

### 方法一：命令行

```bash
git add .
git commit -m "Update content"
git push
```

### 方法二：网页界面

1. 在 GitHub 仓库页面点击文件
2. 点击编辑图标（铅笔图标）
3. 修改内容后点击 **Commit changes**

---

## 常见问题

### 1. 头像不显示？

- 确保 `profilepic.jpg` 已经上传到仓库
- 检查 HTML 中的图片路径是否正确

### 2. CSS 样式没生效？

- 强制刷新浏览器：按 `Ctrl + F5`
- 检查浏览器控制台是否有错误

### 3. 部署后访问 404？

- 等待几分钟（首次部署需要时间）
- 检查仓库 Settings → Pages 中的设置是否正确
- 确认 `index.html` 在仓库根目录

### 4. 如何自定义域名？

1. 在仓库根目录创建 `CNAME` 文件
2. 内容只有一行：你的域名（如：`yourname.com`）
3. 在域名服务商配置 DNS 记录

---

## 快速命令参考

```bash
# 初始化仓库
git init

# 添加文件
git add .

# 提交
git commit -m "Initial commit"

# 连接远程仓库
git remote add origin https://github.com/用户名/仓库名.git

# 推送到 GitHub
git branch -M main
git push -u origin main

# 更新内容
git add .
git commit -m "Update"
git push
```

---

**需要帮助？** 可以查看 GitHub 官方文档：https://docs.github.com/en/pages

