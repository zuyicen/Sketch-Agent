# Sketch Agent

&gt; 嵌入 Sketch 的 AI 设计智能体。用自然语言就能完成UI设计。

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Sketch Version](https://img.shields.io/badge/Sketch-100+-orange.svg)](https://www.sketch.com)
[![macOS](https://img.shields.io/badge/macOS-13%2B-black.svg)](https://www.apple.com/macos)

Sketch Agent 是一款原生嵌入 Sketch 右侧检查器（Inspector）侧边栏的 AI 对话插件。设计师无需离开画布，通过自然语言即可**从零生成完整 UI 界面**，或**直接修改选中图层**的样式与属性，实现「说话就能做设计」的工作流。

---

## 💡 模型推荐

> **日常操控与编辑修改元素**，强烈建议使用 **DeepSeek-V4-Flash**。经过 作者Pillz 实测，该模型在性价比与性能之间取得了极其优秀的平衡，非常适合常规图层和元素的操控。
>
> **生成精美的完整 UI 页面**，强烈推荐使用 **Kimi-K2.6**。其拥有优秀的审美能力，能够输出视觉精致、风格统一的完整页面设计。

---

## ✨ 核心功能

- **🎨 自然语言生成界面** — 描述需求（如 *"做一个带邮箱、密码框和第三方登录按钮的登录页"*），AI 自动在画板上构建完整图层结构。
- **⚡ 对话式修改设计** — 选中任意图层，输入指令（如 *"把这个按钮改成主题蓝 #1890FF，圆角 8px，加投影"*），画布即时更新。
- **👁️ 智能预览模式** — 简单属性修改即时生效；复杂生成先展示 SVG 预览，确认后再写入画布，避免污染设计稿。
- **🤖 多模型自由切换** — 自带 API Key 即可使用 **OpenAI (GPT-4o)**、**Anthropic (Claude 4 Sonnet)**、**DeepSeek (V3)**、**智谱 AI (GLM-4)**。
- **🧠 画布上下文感知** — 自动采集选中图层属性、画板尺寸、文档颜色变量和文本样式，注入 AI Prompt 保证生成结果贴合当前设计系统。
- **↩️ 原生撤销支持** — 每次 AI 操作前自动快照，可通过 Sketch 原生 `Cmd+Z` 逐步回退。
- **🔒 隐私优先** — API Key 本地 AES 加密存储，设计数据不上传任何第三方服务器。

---

## 📦 安装

### 通过 Release 安装（推荐）

1. 在 [Releases](../../releases) 下载最新版 `.sketchplugin`。
2. 双击安装。
3. 如 Sketch 正在运行，重启即可。


## 🚀 快速开始

1. 打开 Sketch 并进入任意文档。
2. 在右侧 Inspector 侧边栏找到 **Sketch Agent** 面板。
3. 点击 **⚙️ 设置**，选择 AI 提供商并填入 API Key。
4. 开始用说话的方式做设计：
   - **创建：选中空白画布，输入** *"生成一个包含头像、昵称和简介的APP个人中心页设计"*
   - **修改：** 选中一个按钮，输入 *"改成蓝色并添加 阴影"*

------

## ⚙️ 设置项

| 设置项         | 说明                                         |
| :------------- | :------------------------------------------- |
| **提供商**     | OpenAI / Anthropic / DeepSeek / 智谱 AI/KIMI |
| **API Key**    | 个人 API 密钥（本地加密存储）                |
| **Endpoint**   | 可选自定义 API 接口地址                      |
| **模型**       | 如 `gpt-4o`、`claude-4-sonnet` 等            |
| **预览模式**   | 自动判断 / 始终预览 / 始终直接生效           |
| **上下文轮数** | 保留的对话历史轮数（默认 10 轮）             |

------

## 🛠️ 技术栈

- **前端界面：** HTML/CSS/JS，运行于 Sketch 原生 `WKWebView`
- **通信桥接：** `sketch-module-web-view` 实现 WebView ↔ 插件双向通信
- **原生操作：** Sketch JavaScript API + CocoaScript 操控画布图层
- **构建工具：** `skpm`（基于 Webpack 的 Sketch 插件构建链）
- **AI 层：** 标准 Chat Completions API，统一 Adapter 屏蔽厂商差异

------

## 📋 支持的操作类型

### 生成

- 矩形、文本、图片占位、编组、Symbol 实例

### 修改

- 颜色（填充、描边、文字、渐变）
- 尺寸、位置、间距
- 文字排版（字体、字号、行高、字间距、对齐方式）
- 圆角、阴影、不透明度
- 图层层级（置顶、置底、上移、下移）



------

## 📄 开源协议

本项目基于 MIT 协议开源。详见 [LICENSE](https://www.kimi.com/chat/LICENSE)。

------

<p align="center">   为 Sketch 社区用心打造 💙 </p> 

