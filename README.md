# 橙子课表 (OrangeOrganize) 官网

纯静态官网，使用 HTML/CSS/JS 构建，无后端、无构建工具依赖，可直接部署到任意静态托管服务。

## 📁 项目结构

```
橙子课表官网/
├── index.html          # 主页面（含内联 CSS 和 JS）
├── DESIGN.md           # 设计说明文档
├── README.md           # 项目说明（本文件）
├── assets/
│   └── logo.svg        # 品牌 Logo（已用于导航、Hero、页脚、favicon）
└── .gitignore          # Git 忽略规则（可选）
```

## 🚀 快速开始

### 本地预览

直接在浏览器中打开 `index.html` 即可预览：

```bash
# Windows
start index.html

# macOS
open index.html

# Linux
xdg-open index.html
```

或使用本地服务器：

```bash
# 使用 Python
python -m http.server 8000

# 使用 Node.js (需安装 http-server)
npx http-server -p 8000
```

## 📱 部署到静态托管

### GitHub Pages

1. 将项目推送到 GitHub 仓库
2. 进入仓库 Settings > Pages
3. 选择部署分支和文件夹（如 `main` 分支的根目录）
4. 等待部署完成，访问提供的域名

### Vercel / Netlify

1. 将代码推送到 GitHub/GitLab
2. 在 Vercel/Netlify 中导入仓库
3. 选择框架：其他（Other）
4. 构建命令留空
5. 构建输出目录：`/`
6. 部署！

### 其他托管服务

- **Cloudflare Pages**: 直接连接仓库即可
- **Firebase Hosting**: 使用 `firebase deploy`
- **AWS S3 + CloudFront**: 上传文件到 S3，配置 CloudFront

## 🎨 设计令牌

全站使用以下 CSS 变量定义的品牌色：

| 用途 | 颜色值 | 变量名 |
|------|--------|--------|
| 品牌主色（深橙） | `#9A4800` | `--color-primary` |
| 明亮强调橙 | `#E8590C` | `--color-accent` |
| 强调橙悬停 | `#FF6B00` | `--color-accent-hover` |
| 主容器浅橙底 | `#FFDBC6` | `--color-primary-container` |
| 页面背景（米白） | `#FFF8F5` | `--color-bg` |
| 卡片背景 | `#FFFFFF` | `--color-surface` |
| 正文文字 | `#221A14` | `--color-text` |
| 次要文字 | `#52443B` | `--color-text-secondary` |

详细设计令牌请查看 `DESIGN.md`。

## 🖼️ 图片占位说明

页面中使用以下占位，请替换为真实图片：

### 1. 下载二维码

在 `index.html` 中找到下载区（约第 420 行）：

```html
<!-- 注意：请替换为真实的二维码图片 -->
<!-- 示例：<img src="/assets/qrcode.png" alt="下载二维码" style="width:160px;height:160px;border-radius:12px;"> -->
<div class="qr-placeholder"></div>
```

替换方式：

```html
<div class="download-qr">
    <img src="assets/qrcode.png" alt="下载二维码" width="160" height="160">
</div>
```

### 2. 下载链接

在 `index.html` 中找到下载区按钮，`href` 目前为占位符 `[下载APK链接]`：

```html
<a href="[下载APK链接]" class="btn btn-primary download-button" ...>
```

替换 `[下载APK链接]` 为真实的 APK 文件路径，例如：

```html
<a href="downloads/orange-organize-v1.0.0.apk" class="btn btn-primary download-button" ...>
```

### 3. 联系方式

在页面底部和 FAQ 中，将 `[联系邮箱]` 替换为真实的联系邮箱地址。

## ⚙️ 自定义配置

### 修改版本号/大小/日期

在 `index.html` 中搜索以下关键字：

- `v1.0.0` - 版本号
- `约 7MB` - 安装包大小
- `2026-09-05` - 更新日期

### 修改版权年份

在页面底部搜索 `© 2026`，替换为实际年份。

### 调整颜色

在 `index.html` 的 `:root` 中修改 CSS 变量值（约第 10 行）：

```css
:root {
    --color-primary: #9A4800;  /* 修改这里 */
    --color-accent: #E8590C;   /* 修改这里 */
    /* ... */
}
```

## 📱 移动端适配

- 所有按钮最小点击区域 `44px`
- 汉堡菜单在屏幕宽度 `<992px` 时显示
- 特性卡片响应式布局：
  - 移动端：1 列
  - 平板：2 列
  - 桌面：4 列

## ✨ 功能清单

- ✅ 固定吸顶导航栏（滚动时阴影效果）
- ✅ 汉堡菜单（移动端）
- ✅ 平滑滚动锚点
- ✅ 活动导航项高亮
- ✅ 特性卡片悬停效果
- ✅ 淡入动画（滚动触发）
- ✅ FAQ 手风琴（折叠/展开）
- ✅ 尊重系统「减少动效」偏好
- ✅ 响应式设计
- ✅ 无外部依赖

## 🔒 隐私与安全

- 无任何第三方追踪代码
- 无外部字体/图标依赖
- 所有资源可本地托管
- 无 Cookie 收集

## 📄 许可证

本项目为纯静态展示页面，供「橙子课表」用户使用。

## 📞 联系方式

如有问题，请联系：[联系邮箱]

---

**橙子课表 OrangeOrganize** — 轻量简洁的课表软件
