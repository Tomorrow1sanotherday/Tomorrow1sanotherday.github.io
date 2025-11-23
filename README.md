# 学术主页

一个简洁优雅的学术个人主页模板，适用于 GitHub Pages。

## 功能特点

- ✨ 现代化设计，简洁优雅
- 📱 完全响应式，支持移动端
- 🎨 精美的动画效果
- 🔗 集成 Google Scholar、GitHub 等链接
- 📄 展示研究兴趣、新闻和论文

## 使用方法

### 1. 自定义内容

编辑 `index.html` 文件，修改以下内容：

- **个人信息**：姓名、职位、学校、部门
- **头像**：替换 `src="https://via.placeholder.com/200"` 为你的头像链接，或上传图片到仓库
- **链接**：更新 Google Scholar、GitHub、邮箱链接
- **介绍**：修改个人介绍文本
- **研究兴趣**：更新研究方向和兴趣
- **新闻**：添加或修改新闻条目
- **论文**：更新论文列表

### 2. 部署到 GitHub Pages

#### 方法一：使用命令行（推荐）

1. **初始化 Git 仓库**（如果还没有）
   ```bash
   git init
   git add .
   git commit -m "Initial commit: Academic homepage"
   ```

2. **在 GitHub 上创建新仓库**
   - 访问 https://github.com/new
   - 输入仓库名称（例如：`yourname.github.io` 或 `academic-homepage`）
   - 选择 Public（公开）
   - **不要**勾选 "Initialize this repository with a README"
   - 点击 "Create repository"

3. **连接本地仓库到 GitHub**
   ```bash
   git remote add origin https://github.com/你的用户名/仓库名.git
   git branch -M main
   git push -u origin main
   ```

4. **启用 GitHub Pages**
   - 进入仓库页面，点击 **Settings**（设置）
   - 在左侧菜单找到 **Pages**
   - 在 "Source" 下选择 **Deploy from a branch**
   - 选择分支：`main` 或 `master`
   - 选择文件夹：`/ (root)`
   - 点击 **Save**

5. **访问你的主页**
   - 如果仓库名是 `yourname.github.io`，访问：`https://你的用户名.github.io`
   - 如果仓库名是其他名称，访问：`https://你的用户名.github.io/仓库名`
   - 首次部署可能需要几分钟，请耐心等待

#### 方法二：使用 GitHub 网页界面

1. **创建新仓库**
   - 访问 https://github.com/new
   - 输入仓库名称
   - 选择 Public
   - 点击 "Create repository"

2. **上传文件**
   - 在仓库页面点击 **uploading an existing file**
   - 拖拽或选择所有文件（index.html, style.css, script.js, README.md, .gitignore）
   - 点击 **Commit changes**

3. **启用 GitHub Pages**
   - 进入 **Settings** → **Pages**
   - Source 选择 `main` 分支，文件夹选择 `/ (root)`
   - 点击 **Save**

4. **等待部署完成**
   - 通常 1-2 分钟后即可访问
   - 在仓库的 **Actions** 标签页可以查看部署状态

### 3. 使用自定义域名（可选）

如果你想使用自己的域名（如 `yourname.com`）：

1. **创建 CNAME 文件**
   - 在仓库根目录创建 `CNAME` 文件（无扩展名）
   - 内容只需一行：你的域名（如：`yourname.com` 或 `www.yourname.com`）

2. **配置 DNS 记录**
   - 登录你的域名服务商（如 GoDaddy、Namecheap 等）
   - 添加 DNS 记录：
     - **类型**：CNAME
     - **主机**：@ 或 www
     - **值**：`你的用户名.github.io`
   - 或者使用 A 记录：
     - **类型**：A
     - **主机**：@
     - **值**：`185.199.108.153`、`185.199.109.153`、`185.199.110.153`、`185.199.111.153`

3. **等待 DNS 生效**
   - 通常需要几分钟到几小时
   - 可以使用 `ping yourname.com` 检查是否生效

### 4. 更新内容

每次修改文件后，需要提交并推送：

```bash
git add .
git commit -m "Update homepage content"
git push
```

GitHub Pages 会自动重新部署，通常 1-2 分钟后更新就会生效。

## 文件结构

```
.
├── index.html      # 主页面
├── style.css       # 样式文件
├── script.js       # 交互脚本
└── README.md       # 说明文档
```

## 自定义样式

可以在 `style.css` 中修改 CSS 变量来改变主题颜色：

```css
:root {
    --primary-color: #2563eb;      /* 主色调 */
    --text-primary: #1f2937;      /* 主文本颜色 */
    --text-secondary: #6b7280;    /* 次要文本颜色 */
    /* ... 更多变量 */
}
```

## 浏览器支持

- Chrome (最新版)
- Firefox (最新版)
- Safari (最新版)
- Edge (最新版)

## 许可证

MIT License - 可自由使用和修改

