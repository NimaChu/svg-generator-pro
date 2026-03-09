# SVG Generator

> 🎨 生成可定制的 SVG 背景和图形（支持科技、极简、几何、抽象4种风格，以及5种预设配色方案）

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

## ✨ 项目简介

**SVG Generator** 是一个 [OpenClaw](https://github.com/openclaw/openclaw) Skill，帮助你快速生成精美、可定制的 SVG 背景和图形，用于网站、演示文稿、社交媒体或 UI 装饰元素。

### 🎯 核心特性

- **多种风格** - 4种预设风格：科技、极简、几何、抽象
- **灵活配色** - 5种预设配色方案 + 自定义颜色支持
- **完全本地** - 无需 API 调用，零成本，离线可用
- **Web 友好** - 响应式设计，优化用于网页展示
- **多格式输出** - 支持 SVG、PNG、JPEG、WebP 等格式

### 📐 输出规格

| 规格 | 说明 |
|------|------|
| 尺寸 | 可自定义（默认 1920 × 1080 px） |
| 格式 | SVG（矢量，无损缩放） |
| 兼容性 | 网页、PowerPoint、设计软件 |

---

## 🚀 快速开始

### 前置要求

- 安装 [OpenClaw](https://github.com/openclaw/openclaw)
- 将本项目放置于 OpenClaw 的 skills 目录

### 使用流程

```
┌─────────────────────────────────────────────────────────────────┐
│                        SVG 生成流程                           │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│  ⚡ 快捷方式  /svg-gen-quick --style=风格 --colors=配色           │
│              ↓ 一键完成生成，无需交互                           │
│              ↓ 适合已明确需求的用户                             │
│                                                                 │
│  ─────────────────── 或分步执行 ───────────────────            │
│                                                                 │
│  步骤 1️⃣  /svg-gen-styles                                      │
│           ↓ 查看可用风格和配色方案                              │
│           ↓ 获取详细说明和示例                                  │
│                                                                 │
│  步骤 2️⃣  /svg-gen-custom                                    │
│           ↓ 创建自定义配置                                      │
│           ↓ 退出编辑模式时自动生成                              │
│                                                                 │
│  步骤 3️⃣  /svg-gen-preview @svg文件                            │
│           ↓ 预览生成效果                                        │
│                                                                 │
│  步骤 4️⃣  /svg-gen-convert @svg文件                            │
│           ↓ 转换为 PNG/JPEG/WebP 等格式                         │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

---

## 🔧 可用命令

### `/svg-gen-quick` - ⚡ 一键生成（推荐）

一键生成 SVG 图形，使用预设风格或自定义参数。

**语法**：
```bash
/svg-gen-quick --style <风格> --colors <配色> [--output <文件路径>]
```

**参数**：

| 参数 | 必需 | 默认值 | 说明 |
|------|------|--------|------|
| `--style` | ✅ | - | 风格名称（tech/minimal/geometric/abstract） |
| `--colors` | ✅ | - | 配色方案或自定义颜色 |
| `--output` | ❌ | `./output.svg` | 输出文件路径 |

**可用风格**：`tech`、`minimal`、`geometric`、`abstract`

**预设配色方案**：`blue-purple`、`gray-blue`、`teal-cyan`、`green-blue`、`custom`

**示例**：

```bash
# 使用预设风格和配色
/svg-gen-quick --style tech --colors blue-purple --output hero-bg.svg

# 使用自定义颜色
/svg-gen-quick --style minimal --colors "#FF6B6B-#4ECDC4" --output custom-bg.svg

# 自然语言方式
帮我生成一个科技风格的背景，颜色用科技蓝到紫色
```

---

### `/svg-gen-styles` - 📚 风格和配色参考

查看所有可用风格和配色方案的详细说明。

**语法**：
```bash
/svg-gen-styles
```

**示例**：
```bash
# 查看风格参考
/svg-gen-styles

# 自然语言方式
科技风格适合什么场景？
有哪些配色方案？
```

---

### `/svg-gen-custom` - 🎨 自定义配置

通过交互式方式创建自定义 SVG 配置。

**语法**：
```bash
/svg-gen-custom
```

**交互流程**：
1. 选择风格
2. 设置配色（使用预设或自定义颜色）
3. 设置尺寸（可选）
4. 选择输出格式
5. 确认生成

---

### `/svg-gen-preview` - 👀 预览生成效果

预览 SVG 文件的视觉效果。

**语法**：
```bash
/svg-gen-preview @svg文件
```

---

### `/svg-gen-convert` - 🔄 格式转换

将 SVG 转换为 PNG、JPEG、WebP 等位图格式。

**语法**：
```bash
/svg-gen-convert @svg文件 [--width <像素>] [--height <像素>] [--format <格式>]
```

**支持格式**：`png`、`jpeg`、`webp`

---

## 🎨 风格详解

### Tech 风格（科技风格）
- **特点**：抽象科技元素（数据流、节点、电路）、动态几何图形、未来感设计
- **适用场景**：科技网站、SaaS 产品首页、技术博客

### Minimal 风格（极简风格）
- **特点**：简洁的渐变和几何形状、大量留白、专业简约感
- **适用场景**：专业网站、个人作品集、简洁商务演示

### Geometric 风格（几何风格）
- **特点**：精确的数学图案、规则的几何形状、现代设计感
- **适用场景**：仪表盘、管理后台、数据报告

### Abstract 风格（抽象风格）
- **特点**：艺术性抽象组合、创意构图、个性化表达
- **适用场景**：创意项目、社交媒体、艺术展示

---

## 🎨 配色方案详解

| 方案 | 颜色值 | 适用场景 |
|------|--------|----------|
| `blue-purple` | 蓝 → 紫 | 科技产品、SaaS | 
| `gray-blue` | 灰 → 蓝 | 企业、商务 | 
| `teal-cyan` | 青 → cyan | 现代设计、清新感 | 
| `green-blue` | 绿 → 蓝 | 生态、健康品牌 | 

---

## 📁 项目结构

```
svg-generator-pro/
├── SKILL.md              # Skill 配置文件
├── README.md             # 项目说明（本文件）
├── commands/             # 命令定义
│   ├── quick.md          # /svg-gen-quick 一键生成
│   ├── styles.md         # /svg-gen-styles 风格参考
│   ├── custom.md         # /svg-gen-custom 自定义配置
│   ├── preview.md        # /svg-gen-preview 预览效果
│   └── convert.md        # /svg-gen-convert 格式转换
├── scripts/              # 生成脚本
│   ├── generate-svg.js   # SVG 生成主脚本
│   ├── convert-svg.js    # 格式转换脚本
│   └── customize-svg.js  # 自定义配置脚本
├── assets/               # 示例资源
│   ├── examples/         # 各种风格的示例 SVG 文件
│   └── templates/        # 可复用的 SVG 模板
└── references/           # 参考文档
    ├── best-practices.md # SVG 最佳实践
    ├── ppt-integration.md # PPT 导入指南
    └── color-theory.md   # 配色理论
```

---

## 📖 详细文档

- [一键生成命令](commands/quick.md)
- [风格和配色参考](commands/styles.md)
- [自定义配置命令](commands/custom.md)
- [预览效果命令](commands/preview.md)
- [格式转换命令](commands/convert.md)
- [SVG 最佳实践](references/best-practices.md)
- [PPT 导入指南](references/ppt-integration.md)
- [配色理论](references/color-theory.md)

---

## 📄 许可证

本项目采用 [MIT 许可证](LICENSE) 开源。

---

## 🤝 贡献

欢迎提交 Issue 和 Pull Request！

如果这个项目对你有帮助，请给个 ⭐ Star 支持一下！