# Canvas Copilot

<p align="center">
  <b>基于大模型的 Canvas LMS & EchoVideo 沉浸式课程智能学习助手</b><br>
  <i>集视频字幕提取、AI 结构化笔记、Quiz 测验分步辅导、LaTeX 公式渲染与课程助教于一体的浏览器侧边栏扩展。</i>
</p>

---

## 📖 简介 (Introduction)

**Canvas Copilot** 是一款专为高校大学生、研究者及在线学习者打造的生产力浏览器扩展。深度适配 **Canvas LMS**（如墨尔本大学、悉尼大学、RMIT 等高校部署环境）与 **Echo360 / EchoVideo** 网课播放平台，依托现代大语言模型（LLM），在浏览器原生 **Side Panel（侧边栏）** 中为学生提供一站式、无干扰的听课与复习辅助体验。

---

## ✨ 核心功能矩阵 (Key Features)

### 1. 📝 EchoVideo 视频字幕提取与 AI 智能笔记
* **字幕自动捕获**：智能监听并捕获 Echo360 / EchoVideo 播放器中的视频字幕流（支持 WebVTT 与 JSON 协议，兼容 Canvas 嵌入式播放）。
* **智能断句合并**：内置语句黏连引擎，将碎化的单行字幕智能重构成逻辑连贯的段落。
* **批量字幕提取**：支持一键批量提取整门课程列表的所有录像字幕，告别逐节课手动操作。
* **AI 结构化笔记生成**：一键将课堂讲解内容提炼为排版精美的 Markdown 笔记，涵盖核心考点、定理推导与课堂总结。
* **双语与离线导出**：支持一键导出带时间戳的中英双语 TXT 字幕文件与 Markdown 笔记。

### 2. 🎯 Canvas Quiz 交互式测验解析与辅导
* **全题型智能识别**：自动解析 Canvas Quizzes 作答页与结果页中的单选、多选、判断、填空与简答题。
* **分步深度解析**：支持单题独立解析与一键批量解析全部试题，给出详尽推导过程与考点归纳。
* **LaTeX 公式无损呈现**：内置 `Temml` + `markdown-it-texmath` 渲染引擎，题干、选项与推导中的数学公式完美显示。
* **单题多轮智能追问**：针对不理解的难题支持在卡片内直接发起多轮定向追问，彻底弄懂错题。
* **离线归档导出**：支持一键导出整套试题文本及题图素材，方便期末集中复习。

### 3. 💡 智能课程助教 (AI Tutor)
* **常驻侧边栏对话**：无需切换页面，边看网课/浏览课件边与 AI 助教展开深度学术答疑。
* **动态参考来源联动**：支持一键切换助教知识源（自动检测 / 聚焦当前视频笔记 / 聚焦当前习题）。
* **思考强度实时调节**：支持在急速 (None)、快速 (Low)、均衡 (Medium)、深度 (High) 之间按需调节模型的思考推理深度。

### 4. 🎛️ 多模型支持与 5 大面板独立路由
* **主流大模型直连**：深度集成 **DeepSeek**（含 DeepSeek-R1 深度推理 / V3 模型）、**Google Gemini**、**OpenAI**（GPT-4o 系列）以及**自定义 OpenAI 兼容端点**（如 Ollama、LocalAI、第三方中转）。
* **面板独立配置**：支持为【概览】、【笔记】、【课件】、【助教】、【习题】5 个独立功能面板分别配置专属模型与思考深度（例如：笔记使用 Gemini 高速提炼，习题使用 DeepSeek-R1 深度求解）。
* **BYOK 纯净模式**：用户自备 API Key，无强制订阅门槛，直连官方 API。

### 5. 🎓 全球高校 Canvas 动态授权与全面支持
* **预设即用**：预置支持墨尔本大学 (Unimelb)、悉尼大学 (USYD)、皇家墨尔本理工 (RMIT) 及 EchoVideo 平台。
* **全球高校动态接入**：独创【高校与站点管理】，支持全球任意大学学生在设置中一键添加本校 Canvas 域名（如 `canvas.harvard.edu` 等），遵循最小权限原则动态按需授权。

### 6. 📂 本地工作区联动与绝对隐私
* **本地文件夹挂载**：通过 Web File System Access API 绑定本地学习目录（如 Obsidian 库），自动按 `课程代码/` 规范归档笔记、字幕与配图。
* **100% 本地化隐私**：无任何自建数据收集服务器，不收集任何学生账号密码、学号、Cookie 或个人隐私；所有配置与临时缓存存储在本地 `IndexedDB` 与 `chrome.storage.local`。

---

## 🖥️ 侧边栏界面布局 (UI Architecture)

扩展采用现代化分屏设计，提供 5 个核心功能 Tab：

| 视图面板 | 核心能力 |
| :--- | :--- |
| 📚 **概览 (Overview)** | 自动识别当前 Canvas 课程代码，解析 Syllabus 与 Modules 大纲，生成知识脉络树 |
| 📝 **笔记 (Notes)** | 提取 EchoVideo 视频字幕、批量字幕抓取、一键生成 AI 总结笔记、导出 TXT/MD |
| 📁 **课件 (Materials)** | Canvas 课件资源与课程讲义集中查看与管理 |
| 💡 **助教 (AI Tutor)** | 智能随堂问答，支持笔记/习题上下文挂载与深度思考推理 |
| 🎯 **习题 (Practice)** | Canvas Quiz 题目抓取、单题/批量 AI 深度解析、公式渲染、针对性追问与试题导出 |

---

## 🚀 安装与加载指南 (Installation)

### 方式一：应用商店安装（推荐）
- [**Microsoft Edge Add-ons 商店页面**](https://microsoftedge.microsoft.com/addons) *(审核通过后更新链接)*
- [**Chrome Web Store 商店页面**](https://chromewebstore.google.com/) *(审核通过后更新链接)*

### 方式二：开发者模式离线加载
1. 下载或克隆本项目仓库，解压出 `extension_canvas_copilot` 文件夹。
2. 打开浏览器扩展管理页面：
   - Edge 浏览器：访问 `edge://extensions/`
   - Chrome 浏览器：访问 `chrome://extensions/`
3. 在页面上方开启 **“开发者模式” (Developer mode)**。
4. 点击 **“加载已解压的扩展程序” (Load unpacked)**。
5. 选择 `extension_canvas_copilot` 目录完成加载。
6. 点击工具栏的 Canvas Copilot 图标，即可在任意页面呼出 Side Panel 侧边栏。

---

## ⚙️ 快速上手与配置 (Quick Start)

1. **配置 API Key**：
   - 点击侧边栏右上角的 **⚙️ 设置** 图标打开设置抽屉。
   - 选择您常用的 **Model Provider**（DeepSeek / Google Gemini / OpenAI / Custom）。
   - 填入对应官方 API Key 并点击“获取模型”选择您需要的模型版本。
2. **挂载本地文件夹（可选）**：
   - 在设置中的【本地存储设置】下点击“浏览”，选取您的本地笔记文件夹（例如 Obsidian 知识库根目录）。
   - 开启“自动保存提取的字幕”、“自动保存生成的笔记”与“自动保存提取的习题”开关。
3. **开启学习之旅**：
   - 打开任意 Canvas 课程页面、Canvas Quiz 作答页或 Echo360 录像页面。
   - 侧边栏将自动识别当前课程与内容，点击对应功能按钮即可开始高效学习！

---

## 🛡️ 权限合规与隐私政策 (Permissions & Privacy)

Canvas Copilot 严格遵守最小权限原则：

* `storage`：用于在本地保存用户的 API Key、模型偏好与笔记缓存。
* `sidePanel`：用于承载浏览器右侧常驻交互侧边栏。
* `downloads`：用于支持导出 Markdown 笔记、字幕 TXT 及 Quiz 试题文件。
* `scripting` & `tabs`：仅在用户主动操作时与当前课程页面通信并提取公开内容。
* `activeTab`：允许用户点击工具栏图标或操作按钮时临时与活动页面建立通信。
* `optional_host_permissions`：用于支持学生在设置中按需添加并动态授权其所在高校的 Canvas LMS 域名。
* `host_permissions`：
  - 预设高校 Canvas LMS 与 Echo360 域名：用于提取课件、题目与字幕数据。
  - 大模型官方 API 端点：仅用于直连用户配置的大模型服务。

详细隐私政策请参阅 [PRIVACY.md](file:///e:/code/browser/canvas_copilot/PRIVACY.md)。

---

## 📄 开源致谢 (Acknowledgements)

本项目使用了以下优秀的开源软件与组件：
* [markdown-it](https://github.com/markdown-it/markdown-it) - 高性能 Markdown 解析器 (MIT License)
* [markdown-it-texmath](https://github.com/goessner/markdown-it-texmath) - LaTeX 数学公式扩展 (MIT License)
* [Temml](https://github.com/ronkok/Temml) - 轻量快速的 MathML / TeX 数学排版库 (MIT License)

完整第三方开源许可说明详见 [NOTICES.txt](file:///e:/code/browser/canvas_copilot/extension_canvas_copilot/NOTICES.txt)。
