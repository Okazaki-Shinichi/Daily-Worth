# Daily Worth - 每日价值追踪器

> 📊 一款简洁美观的物品日均成本追踪应用，帮助您了解每件物品的真实价值

![Daily Worth](https://img.shields.io/badge/Daily%20Worth-v1.0-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![HTML](https://img.shields.io/badge/HTML5-E34F26?logo=html5)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript)

## ✨ 功能特性

### 🎯 核心功能
- **物品管理**：轻松添加、编辑、删除物品
- **自动计算**：自动计算物品的日均使用成本
- **智能统计**：实时显示总花费、日均总成本等关键指标
- **数据持久化**：使用本地存储，数据永不丢失

### 📊 数据可视化
- **日均成本图表**：直观展示所有物品的日均成本对比
- **多种排序方式**：按成本高低、名称等多种方式排序
- **颜色编码**：根据成本区间自动着色（绿/蓝/橙/红）
- **交互式体验**：悬停显示详细信息，点击筛选

### 🎨 用户体验
- **Emoji图标**：为物品选择精美的emoji图标（6大分类）
- **响应式设计**：完美适配桌面和移动设备
- **优雅动画**：流畅的过渡和交互效果
- **数据导入导出**：支持JSON格式，方便备份和迁移

## 🚀 快速开始

### 方法一：直接使用（推荐）

1. 下载 `index.html` 文件
2. 双击打开，即可使用

无需安装任何依赖，无需服务器，即开即用！

### 方法二：本地服务器（开发）

```bash
# 使用Python
python -m http.server 8000

# 使用Node.js
npx serve

# 然后访问 http://localhost:8000
```

## 📖 使用说明

### 添加物品
1. 点击"添加新物品"区域
2. 选择emoji图标（可选）
3. 填写物品名称、价格
4. 选择购买日期
5. （可选）填写预计使用天数
6. 点击"添加物品"

### 查看统计
- **物品总数**：所有已添加的物品数量
- **总花费**：所有物品的购买价格总和
- **日均总成本**：所有物品日均成本的总和

### 使用图表
- 选择排序方式（成本高→低 / 低→高 / 名称）
- 悬停查看详细信息
- 不同颜色代表不同成本区间：
  - 🟢 绿色：< ¥1/天
  - 🔵 蓝色：¥1-5/天
  - 🟠 橙色：¥5-10/天
  - 🔴 红色：> ¥10/天

### 数据管理
- **导出**：点击"导出"按钮，保存为JSON文件
- **导入**：点击"导入"按钮，选择之前的JSON文件
- **编辑**：点击物品卡片的"编辑"按钮
- **删除**：点击物品卡片的"删除"按钮

## 🎯 技术栈

- **HTML5**：语义化标签，结构清晰
- **CSS3**：现代CSS特性，响应式设计
- **Vanilla JavaScript**：原生JavaScript，无框架依赖
- **Chart.js**：数据可视化库（CDN引入）
- **LocalStorage**：浏览器本地存储

## 📁 文件结构

```
daily-worth-single/
├── index.html          # 单文件应用（包含所有功能）
└── README.md          # 项目说明文档
```

## 🌟 核心算法

### 日均成本计算

```javascript
日均成本 = 购买价格 ÷ 使用天数

使用天数 = 预计天数（如果有）
         或 购买日期至今的天数
```

### 示例

| 物品 | 价格 | 使用天数 | 日均成本 |
|------|------|----------|----------|
| iPhone 14 | ¥6999 | 365 | ¥19.18 |
| 笔记本电脑 | ¥8000 | 730 | ¥10.96 |
| 机械键盘 | ¥500 | 90 | ¥5.56 |

## 🎨 功能截图

### 主界面
- 统计面板：一目了然的关键数据
- 添加表单：简洁直观的输入界面
- 日均成本图表：可视化数据分析

### 物品列表
- 卡片式布局：信息清晰
- Emoji图标：快速识别
- 操作按钮：编辑/删除

## 🔧 自定义配置

### 修改颜色主题

在 `<style>` 标签中修改 CSS 变量：

```css
:root {
    --primary-color: #3b82f6;      /* 主色调 */
    --success-color: #10b981;      /* 成功色 */
    --danger-color: #ef4444;       /* 危险色 */
    /* ... 更多变量 */
}
```

### 修改Emoji分类

在 JavaScript 中的 `EMOJI_CATEGORIES` 对象添加：

```javascript
const EMOJI_CATEGORIES = {
    // 添加新分类
    yourCategory: ['😀', '😃', '😄'],
};
```

## 📊 数据格式

### 导出的JSON格式

```json
[
  {
    "id": "1a2b3c4d",
    "name": "iPhone 14",
    "price": 6999,
    "purchaseDate": "2023-01-01",
    "estimatedDays": null,
    "emoji": "📱",
    "usageDays": 365,
    "dailyCost": 19.178082191780822,
    "createdAt": "2024-03-18T12:00:00.000Z"
  }
]
```

## 🔄 版本历史

### v1.0.0 (2024-03-18)
- ✨ 初始版本发布
- ✨ 物品管理功能
- ✨ 日均成本计算
- ✨ 数据可视化图表
- ✨ Emoji图标支持
- ✨ 响应式设计

## 🤝 贡献指南

欢迎提交 Issue 和 Pull Request！

1. Fork 本仓库
2. 创建您的特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 开启 Pull Request

## 📝 许可证

本项目采用 MIT 许可证 - 详见 [LICENSE](LICENSE) 文件

## 🙏 致谢

- [Chart.js](https://www.chartjs.org/) - 数据可视化库
- [MDN Web Docs](https://developer.mozilla.org/) - Web技术文档

## 📧 联系方式

如有问题或建议，欢迎：
- 提交 [Issue](../../issues)
- 发送邮件

## ⭐ Star History

如果这个项目对您有帮助，请给它一个 Star ⭐

---

<div align="center">
  <b>用 Daily Worth，掌控每一分价值！</b>
</div>
