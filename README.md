# 个人主页

一个基于 Flask 的现代化个人主页应用，可展示您的 GitHub 个人信息、项目和技术栈，并支持多种部署方式。

<img width="1280" height="700" alt="image" src="https://github.com/user-attachments/assets/7d394bbd-c4ed-4398-a551-104237f90c4e" />

## 🚀 功能特点

- ✨ **美观界面设计**：采用二次元+科技+渐变风格，支持自适应深色/浅色模式切换
- 📱 **完全响应式**：完美适配从手机到桌面的各种屏幕尺寸
- 🎨 **精美动画效果**：平滑的过渡和交互动画，提升用户体验
- 🔧 **快速详细配置**：通过简洁的 JSON 配置文件自定义个人信息和网页设置
- 📊 **GitHub 信息集成**：自动展示头像、名称、仓库数量、Stars 数量
- 📈 **活动数据可视化**：直观展示 GitHub 活动轨迹和趋势
- 📝 **技术栈展示**：自动分析并展示您常用的编程语言和技术
- 🔄 **最近项目展示**：自动获取并展示您最近有更新的 GitHub 项目
- 📜 **个性化介绍**：灵活的个人介绍内容配置方式
- 🌐 **在线项目展示**：展示您的在线项目和部署的应用

## 🛠️ 技术栈

- **后端**：Python 3.6+, Flask
- **前端**：HTML5, Tailwind CSS, JavaScript
- **数据可视化**：Chart.js
- **第三方集成**：GitHub API
- **部署选项**：GitHub Pages, Vercel, Netlify, PythonAnywhere, Heroku 等

## 📋 前提条件

- Python 3.6 或更高版本
- Git 版本控制系统
- GitHub 账号（可选，用于展示 GitHub 信息）
- 推荐使用虚拟环境进行开发

## 🚀 快速开始

### 1. 克隆仓库

```bash
# 克隆仓库到本地
git clone https://github.com/WUHINS/Home_Page.git
cd Home_Page
```

### 2. 安装依赖

```bash
# 使用 pip 安装所需依赖
pip install -r requirements.txt

# 或使用提供的部署脚本
bash deploy.sh install
```

### 3. 配置个人信息

编辑 `config.json` 文件，根据您的需求修改以下配置：

```json
{
  "github_url": "https://github.com/your-username",
  "dark_mode": "auto",
  "name": "Your Name",
  "bio": "Your Bio",
  "introduction_file": "Introduction.md",
  "theme": {
    "primary_color": "#6a11cb",
    "secondary_color": "#2575fc",
    "dark_primary_color": "#a855f7",
    "dark_secondary_color": "#60a5fa"
  },
  "background": {
    "image": "background.jpg",
    "blur": 4,
    "overlay_opacity": 0.6,
    "overlay_color": "#f3f4f6",
    "dark_overlay_color": "#121212"
  },
  "contact": {
    "qq": "https://qm.qq.com/q/c7DY18rEju",
    "wechat": "",
    "bilibili": "https://space.bilibili.com/1969160969",
    "douyin": "https://www.douyin.com/user/MS4wLjABAAAATzdjtBBrLLCn69TtPMeseuEUzztbNZzw-9f13adrfiM?relation=0&vid=7143257533807873316",
    "xiaohongshu": "https://www.xiaohongshu.com/user/profile/6427cf87000000002901166e?xsec_token=YBcPhyaU45_o0XD1fWkS2AJAoXOxWm09mZUN0iNRSVK3E%3D&xsec_source=app_share&xhsshare=CopyLink&shareRedId=ODo0N0ZLPEA2NzUyOTgwNjg8OTg1OzxO&apptime=1760733353&share_id=f252abf542b54551b1c018c51f4a64c8&share_channel=copy_link"
  },
  "online_projects": [
    {
      "name": "在线商城系统",
      "description": "基于Flask开发的全功能电商网站，支持商品管理、订单处理和支付集成",
      "url": "https://demo-store.example.com",
      "github_repo": "username/ecommerce-store",
      "icon": "fa-solid fa-shopping-cart"
    },
    {
      "name": "个人博客平台", 
      "description": "响应式个人博客系统，支持Markdown编辑和多用户管理",
      "url": "https://myblog.example.com",
      "github_repo": "username/personal-blog",
      "icon": "https://example.com/blog-icon.png"
    },
    {
      "name": "数据分析仪表板",
      "description": "实时数据可视化仪表板，支持多种图表类型和数据源接入",
      "url": "https://dashboard.example.com",
      "github_repo": "username/data-dashboard",
      "icon": "fa-solid fa-chart-line"
    }
  ]
}
```

### 4. 本地运行

```bash
# 直接运行
python app.py

# 或使用部署脚本
bash deploy.sh run
```

然后访问 http://localhost:5000 查看效果。

## 🎨 自定义个人介绍

有三种灵活的方式可以自定义个人介绍内容：

1. **GitHub README（推荐）**：在您的 GitHub 账号下创建一个与用户名同名的仓库，并在其中添加 README.md 文件
2. **本地 Introduction.md**：直接修改项目根目录下的 Introduction.md 文件
3. **配置文件指定**：在 config.json 中修改 `introduction_file` 字段，指向您自定义的 Markdown 文件

## 🌐 在线服务展示

通过 `online_projects` 配置，您可以展示您的在线服务：

- **服务名称**：清晰展示服务标题
- **服务描述**：简要介绍服务功能和特色
- **在线链接**：提供服务访问入口
- **GitHub仓库**：链接到服务源码
- **图标配置**：支持 Font Awesome 图标类名、自定义图片URL或自动获取服务图标（使用 `http-icon` 值）

## 🚢 部署指南

### 方法一：使用 Vercel/Netlify 部署

1. 将代码推送到 GitHub 仓库
2. 注册 Vercel 或 Netlify 账号
3. 连接您的 GitHub 仓库
4. 按照平台指引完成部署配置

### 方法二：生成静态文件部署

```bash
# 直接运行构建脚本生成静态文件（HTML将直接生成在项目根目录）
python build_static.py

# 添加生成的文件并提交
git add index.html background.jpg

git commit -m 'Update static website'

# 将文件推送到 GitHub Pages 的 gh-pages 分支
git push origin master:gh-pages
```

### 方法三：使用支持 Flask 的平台

您也可以选择支持 Flask 的平台进行部署：
- PythonAnywhere
- Heroku
- Railway
- DigitalOcean App Platform

## 💻 命令行工具

项目提供了便捷的命令行工具 `deploy.sh` 来管理项目：

```bash
# 安装项目依赖
bash deploy.sh install

# 运行开发服务器
bash deploy.sh run

# 构建静态文件
# 注意：build_static.py 已更新，静态HTML直接生成在项目根目录
bash deploy.sh build

# 查看部署指南
bash deploy.sh deploy

# 查看帮助信息
bash deploy.sh help
```

## 🤖 自动编译配置

项目支持配置 GitHub Actions 自动编译功能，主要特点：

- 每天 UTC 时间 0 点（北京时间 8 点）自动运行编译脚本
- 自动将生成的静态文件提交到当前分支
- 支持在 GitHub 仓库的 Actions 页面手动触发运行

GitHub Actions 配置文件可参考[个人项目主页](https://github.com/SRInternet/SRInternet.github.io/blob/master/.github/workflows/build-deploy.yml)

## ⚙️ 配置详解

### config.json 字段说明

- `github_url`：您的 GitHub 个人主页 URL，用于获取您的公开信息
- `dark_mode`：深色模式设置（可选值：`auto` 跟随系统、`dark` 强制深色、`light` 强制浅色）
- `name`：您的名称（GitHub API 调用失败时的备选显示）
- `bio`：您的简介（GitHub API 调用失败时的备选显示）
- `introduction_file`：本地介绍文件路径
- `theme`：主题配色方案配置
  - `primary_color`：主色调（用于按钮、重点内容等）
  - `secondary_color`：辅助色调（用于渐变、次要强调等）
  - `dark_primary_color`：深色模式主色调
  - `dark_secondary_color`：深色模式辅助色调
- `background`：背景图片和视觉效果配置
  - `landscape_image`：横屏设备背景图片文件名
  - `portrait_image`：竖屏设备背景图片文件名
  - `blur`：背景模糊程度
  - `overlay_opacity`：覆盖层透明度
  - `overlay_color`：浅色模式覆盖层颜色
  - `dark_overlay_color`：深色模式覆盖层颜色
  - **新增功能**：系统会根据设备方向自动选择合适的背景图片，横屏设备使用 landscape_image，竖屏设备使用 portrait_image
- `contact`：联系方式配置，支持多种社交平台
- `online_projects`：在线项目列表，展示您的部署项目

## 📞 联系方式

通过配置文件中的联系信息，您可以方便地展示各种社交平台链接：
- QQ
- 微信
- Bilibili
- 抖音
- 小红书

## 🔧 开发指南

- **修改页面样式**：编辑 `templates/index.html` 文件中的 Tailwind CSS 配置
- **添加新功能**：修改 `app.py` 文件中的 Flask 路由和逻辑
- **调整前端交互**：编辑 `templates/index.html` 中的 JavaScript 代码或 `index.js` 文件
- **自定义主题**：在 `config.json` 中调整主题颜色配置

## 📝 License

[MIT](LICENSE)

## 🤝 贡献

欢迎提交 Issue 和 Pull Request 来改进这个项目！
