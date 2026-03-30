# 💕 Love-Me 网站复刻

完整复刻 https://www.love-me.xyz/ 的深色主题约会交友落地页

## 📁 项目结构

```
love-me-clone/
├── index.html          # 主页面
├── style.css           # 样式文件（15KB）
├── script.js           # 脚本文件（12KB）
├── README.md           # 说明文档
└── assets/
    ├── images/         # 照片文件夹（可选）
    └── fonts/          # 字体文件夹（可选）
```

## 🎨 复刻内容

### 已实现功能

| 功能 | 状态 | 说明 |
|------|------|------|
| 深色渐变背景 | ✅ | 深紫/黑色主题 |
| 顶部导航栏 | ✅ | Logo + 绿色 CTA 按钮 |
| Hero 区域 | ✅ | 标题 + 副标题 + 特性标签 |
| 筛选按钮组 | ✅ | 年龄/幻想类型/身材（3 组） |
| 照片展示区 | ✅ | 3 张卡片堆叠效果 |
| 照片画廊 | ✅ | 6 张照片网格 |
| 特性介绍 | ✅ | 3 个功能卡片 |
| 底部 CTA | ✅ | 大按钮 + 免责声明 |
| 页脚 | ✅ | 链接 + 法律声明 |
| 飘心动画 | ✅ | 自动漂浮爱心 |
| 响应式设计 | ✅ | 手机/平板/PC 适配 |
| 悬停效果 | ✅ | 卡片/按钮动画 |
| 点击灯箱 | ✅ | 照片放大查看 |

## 🚀 快速开始

### 方式 1: 直接打开
```bash
cd /Users/wangyiming/.openclaw/workspace/love-me-clone
open index.html
```

### 方式 2: 本地服务器（推荐）
```bash
# Python
python3 -m http.server 8888

# Node.js
npx serve .

# 然后访问 http://localhost:8888
```

## 🎯 自定义指南

### 1. 替换照片

**方式 A - 使用本地照片：**
1. 将照片放入 `assets/images/` 文件夹
2. 修改 `index.html` 中的 `src` 路径：
```html
<img src="assets/images/photo1.jpg" alt="Profile">
```

**方式 B - 使用在线图片：**
直接修改 `src` 为图片 URL（当前使用 Unsplash 占位图）

### 2. 修改文字内容

所有文字都在 `index.html` 中：
- **主标题**: `<h1 class="hero-title">`
- **副标题**: `<p class="hero-subtitle">`
- **筛选标签**: `.filter-label span`
- **按钮文字**: `.btn-cta`
- **照片信息**: `.photo-info`, `.gallery-info`
- **特性描述**: `.feature-card p`

### 3. 修改颜色主题

打开 `style.css`，修改 CSS 变量：
```css
:root {
    --primary-pink: #ff477e;      /* 主粉色 */
    --primary-red: #ff2d55;       /* 次要红色 */
    --accent-green: #00ff88;      /* 强调绿色（顶部按钮） */
    --accent-purple: #9d4edd;     /* 紫色点缀 */
    
    --bg-primary: #0a0610;        /* 主背景 */
    --bg-secondary: #120a1f;      /* 次要背景 */
}
```

### 4. 修改筛选选项

在 `index.html` 中修改 `.filter-buttons`：
```html
<button class="filter-btn" data-filter="age" data-value="18-25">18-25 ans</button>
```

### 5. 修改飘心设置

在 `script.js` 中修改 `CONFIG`：
```javascript
const CONFIG = {
    hearts: {
        enabled: true,        // 是否启用
        interval: 400,        // 生成间隔（毫秒）
        minSize: 12,          // 最小尺寸
        maxSize: 28,          // 最大尺寸
        minDuration: 10,      // 最小漂浮时间（秒）
        maxDuration: 18       // 最大漂浮时间（秒）
    }
};
```

## 📱 响应式断点

| 断点 | 宽度 | 布局变化 |
|------|------|----------|
| Desktop | >1024px | 双栏布局 |
| Tablet | 768-1024px | 单栏布局 |
| Mobile | <768px | 紧凑布局 |
| Small Mobile | <480px | 最小布局 |

## 🔧 技术细节

### 使用的技术
- **HTML5** - 语义化标签
- **CSS3** - Grid/Flexbox 布局、渐变、动画
- **Vanilla JavaScript** - 无依赖原生 JS
- **Google Fonts** - Inter 字体

### 性能优化
- ✅ 无外部 JS 库依赖
- ✅ CSS 变量方便主题定制
- ✅ 图片懒加载（可添加）
- ✅ 动画使用 CSS transform（GPU 加速）

### 浏览器兼容性
- ✅ Chrome 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Edge 90+

## 🎨 设计特点

1. **深色主题** - 深紫/黑色渐变背景
2. **粉色主调** - #ff477e 作为强调色
3. **绿色对比** - 顶部按钮使用绿色形成对比
4. **毛玻璃效果** - 卡片使用 backdrop-filter
5. **发光效果** - 按钮和卡片悬停时有粉色光晕
6. **照片堆叠** - Hero 区照片呈卡片堆叠效果

## 📝 注意事项

1. **图片版权** - 当前使用 Unsplash 免费图片，商用需替换
2. **内容合规** - 根据当地法律调整内容
3. **隐私政策** - 页脚链接需指向真实页面
4. **下载链接** - CTA 按钮需配置真实下载链接

## 🔗 部署建议

### GitHub Pages
```bash
git init
git add .
git commit -m "Initial commit"
git push origin main
# Settings → Pages → 选择 main 分支
```

### Vercel
```bash
npm i -g vercel
vercel
```

### Netlify
直接拖拽文件夹到 Netlify Drop

## 💡 扩展建议

- [ ] 添加真实的用户数据 API
- [ ] 集成用户认证系统
- [ ] 添加实时聊天功能
- [ ] 集成支付系统
- [ ] 添加多语言支持
- [ ] SEO 优化
- [ ] PWA 支持

## 📞 问题排查

**照片不显示？**
- 检查图片路径是否正确
- 确认图片格式支持（JPG/PNG/WebP）
- 查看浏览器控制台报错

**动画不流畅？**
- 检查浏览器是否支持 CSS animations
- 减少同时运行的动画数量
- 使用 requestAnimationFrame 优化

**样式错乱？**
- 清除浏览器缓存
- 检查 CSS 文件是否正确加载
- 确认 viewport meta 标签存在

---

**复刻完成时间**: 2026-03-30  
**原始网站**: https://www.love-me.xyz/  
**技术栈**: HTML5 + CSS3 + Vanilla JS
