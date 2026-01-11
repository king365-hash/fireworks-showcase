# 📖 GitHub Pages 发布完整指南

## 🎯 准备工作

### 第一步：注册 GitHub 账号

1. 访问 [https://github.com](https://github.com)
2. 点击右上角 **"Sign up"**
3. 填写信息：
   - **Email**: 你的邮箱
   - **Password**: 设置密码
   - **Username**: 用户名（将作为网站地址的一部分）
4. 验证邮箱

---

## 📤 上传文件到 GitHub

### 方法一：网页上传（推荐新手）

#### 1. 创建新仓库

1. 登录 GitHub 后，点击右上角 **"+"** → **"New repository"**
2. 填写仓库信息：
   ```
   Repository name: fireworks-showcase
   Description: 🎆 精美的烟花屏网站
   Public ☑️
   Add a README file: 取消勾选（我们已经有了）
   ```
3. 点击 **"Create repository"**

#### 2. 上传文件

1. 在新创建的仓库页面，点击 **"Add file"** → **"Upload files"**
2. 将以下文件拖拽到上传区域：
   - `index.html`
   - `README.md`
   - `.gitignore`
3. 在 **"Commit changes"** 输入框填写：
   ```
   Initial commit: Add firework screen website
   ```
4. 点击 **"Commit changes"** 按钮

### 方法二：使用 Git 命令行（适合开发者）

```bash
# 1. 克隆仓库到本地
git clone https://github.com/你的用户名/fireworks-showcase.git
cd fireworks-showcase

# 2. 复制文件到仓库目录
cp /path/to/github-pages-package/* .

# 3. 添加文件到 Git
git add .

# 4. 提交更改
git commit -m "Add firework screen website"

# 5. 推送到 GitHub
git push origin main
```

---

## ⚙️ 启用 GitHub Pages

### 1. 进入仓库设置

1. 在仓库页面，点击顶部 **"Settings"** 标签
2. 在左侧边栏找到 **"Pages"**（在 "Code and automation" 部分）

### 2. 配置 Pages

在 **"Source"** 部分：
- **Branch**: 选择 `main` 或 `master`
- **Folder**: 选择 `/ (root)`
- 点击 **"Save"** 保存

### 3. 等待部署

- 部署通常需要 **1-2 分钟**
- 页面会显示部署状态（🔴 正在部署 → 🟢 部署成功）

---

## 🌐 访问你的网站

部署成功后，你的网站地址为：

```
https://你的用户名.github.io/fireworks-showcase/
```

### 示例

如果用户名是 `zhangsan`，地址就是：
```
https://zhangsan.github.io/fireworks-showcase/
```

---

## 🔄 更新网站

### 方法一：网页编辑

1. 进入仓库页面
2. 点击 **"index.html"** 文件
3. 点击右上角 **铅笔图标** ✏️ 编辑
4. 修改内容后，在页面底部填写提交信息
5. 点击 **"Commit changes"**

### 方法二：重新上传

1. 删除旧文件：在文件列表中点击文件 → **Delete this file**
2. 上传新文件：**Add file** → **Upload files**
3. 提交更改

### 方法三：Git 命令行

```bash
# 1. 修改本地文件
# 使用编辑器修改 index.html

# 2. 提交更改
git add .
git commit -m "Update firework effect"

# 3. 推送到 GitHub
git push origin main
```

---

## 🎨 自定义域名（可选）

### 使用自己的域名

1. **购买域名**（可选）
   - 阿里云、腾讯云、GoDaddy 等

2. **配置 DNS**
   - 在域名提供商处添加 CNAME 记录：
   ```
   类型: CNAME
   主机记录: @
   记录值: 你的用户名.github.io
   ```

3. **在 GitHub 设置自定义域名**
   - 仓库 → Settings → Pages
   - 在 **"Custom domain"** 输入你的域名
   - 点击 **"Save"**

4. **等待 DNS 生效**（通常 10 分钟 - 48 小时）

---

## 📊 查看访问统计

GitHub Pages 提供基础统计：

1. 仓库 → **Insights** → **Traffic**
2. 可以查看访问量、访问者等数据

---

## 🔧 常见问题

### Q: 网站显示 404 错误

**A:** 检查以下几点：
1. 文件是否正确命名为 `index.html`
2. 是否选择了正确的分支
3. 等待几分钟让部署完成

### Q: 网站无法正常访问

**A:** 尝试以下方法：
1. 清除浏览器缓存后重试
2. 检查仓库是否为 Public（公开）
3. 等待更长时间让 DNS 生效

### Q: 如何修改网站内容

**A:** 有三种方法：
1. 直接在 GitHub 网页上编辑
2. 删除旧文件重新上传
3. 使用 Git 命令行更新

### Q: 能否绑定自己的域名

**A:** 可以！参考上面的"自定义域名"部分

---

## 📝 文件说明

### index.html
- 网站主文件
- 包含完整的烟花动画代码
- 使用 Canvas 绘制和 Web Audio API 音效

### README.md
- 项目说明文档
- 在仓库首页显示
- 包含功能介绍、使用方法等

### .gitignore
- Git 忽略文件配置
- 避免提交不必要的文件

---

## 🎉 完成！

现在你已经成功发布了烟花屏网站！

**分享给朋友的链接格式：**
```
🎆 烟花屏网站：https://你的用户名.github.io/fireworks-showcase/

点击屏幕发射烟花，输入文字显示祝福！
```

---

## 💡 进阶技巧

### 添加favicon图标

在 `index.html` 的 `<head>` 中添加：
```html
<link rel="icon" type="image/png" href="favicon.png">
```

### 添加百度统计

1. 注册百度统计：https://tongji.baidu.com/
2. 在 `</head>` 前添加统计代码

### 优化 SEO

在 `<head>` 中添加：
```html
<meta name="description" content="精美的烟花屏网站，为节日庆典增添欢乐气氛">
<meta name="keywords" content="烟花, firework, 节日, 庆祝">
```

---

**祝使用愉快！🎆🎉**

如有问题，欢迎提 Issue！
