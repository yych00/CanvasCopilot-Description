# Privacy Policy for Canvas Copilot

Last updated: August 27, 2026

This Privacy Policy describes how the **Canvas Copilot** browser extension ("the Extension", "we", "our") handles your data and respects your privacy.

---

## 1. Zero Personal Data Collection (零个人数据收集)

- **No Developer Central Server**: We do NOT operate any centralized tracking, telemetry, or user analytics servers. We do NOT collect, store, track, sell, or transmit any personally identifiable information (PII), student ID numbers, passwords, Canvas session cookies, or general browsing history.
- **Pure Local Execution**: All core functionalities—including Canvas LMS and EchoVideo page content extraction, transcript reconnection, Quiz parsing, and Markdown formatting—execute entirely within your local browser environment.

---

## 2. Third-Party AI Services & Direct Transmission (第三方大模型服务)

Canvas Copilot provides intelligent study notes, interactive Quiz explanations, and academic Q&A powered by modern Large Language Models (such as DeepSeek, Google Gemini, OpenAI, or user-configured custom endpoints).

- **Bring Your Own Key (BYOK)**: All AI features communicate directly with official AI provider endpoints using the API key provided and configured by the user in the extension's settings.
- **Data Sent to LLMs**: Only the specific text explicitly requested by the user for analysis (e.g., lecture transcript excerpts, Quiz questions, or user chat prompts) is transmitted to the selected LLM provider's official API endpoint:
  - DeepSeek: `api.deepseek.com`
  - Google Gemini: `generativelanguage.googleapis.com`
  - OpenAI: `api.openai.com`
- **No Identity Attachment**: Network requests sent to AI providers contain only the necessary prompt text/images and never include student credentials, session cookies, or personal identifiers.
- Third-party AI requests are governed by each provider's respective privacy policy:
  - [DeepSeek Privacy Policy](https://www.deepseek.com/privacy)
  - [Google Privacy Policy](https://policies.google.com/privacy)
  - [OpenAI Privacy Policy](https://openai.com/policies/privacy-policy)

---

## 3. Permissions Justification (权限使用说明)

The Extension requests only the minimum permissions necessary to function:

- `storage`: Used to securely store your customized preferences (chosen AI providers, per-panel model configurations, reasoning levels, custom prompts) and local note/quiz caches on your device.
- `sidePanel`: Used to display the persistent, non-intrusive split-screen study workspace alongside your Canvas course or video player.
- `downloads`: Used to enable one-click export of Markdown notes, subtitle TXT files, and Quiz problem packages to your local machine.
- `scripting` & `tabs`: Used strictly to communicate with the active Canvas/Echo360 tab when you request course analysis or transcript extraction.
- `host_permissions`:
  - Canvas LMS & EchoVideo domains (`canvas.lms.unimelb.edu.au`, `canvas.sydney.edu.au`, `rmit.instructure.com`, `echo360.net.au`): Required to detect course pages, extract public subtitles, and parse quiz structures.
  - LLM API endpoints (`generativelanguage.googleapis.com`, `api.openai.com`, `api.deepseek.com`): Required to request AI completions directly from official APIs.

---

## 4. Local File System Access (本地工作区访问)

If you choose to link a local directory using the Web File System Access API, the Extension uses this permission exclusively to save your generated Markdown notes, subtitles, and quiz images to the selected folder. We do NOT access, scan, or read any other files or directories on your system.

---

## 5. Security & Data Retention (数据安全与保留)

All configuration settings and cached data are stored locally in your browser's `chrome.storage.local` and `IndexedDB`. You retain full control over your data at all times. Clearing your browser storage or uninstalling the extension will completely remove all stored extension data from your device.

---

# 隐私政策 (中文版)

**生效日期：2026 年 8 月 27 日**

本隐私政策说明了 **Canvas Copilot** 浏览器扩展（以下简称“本插件”或“我们”）如何处理您的信息及保护您的个人隐私。

## 1. 零个人数据收集
- **无中心化追踪**：我们不运营任何中心化数据收集服务器，绝不收集、记录、出售或上传您的任何个人身份信息、学生学号、账号密码、Canvas 登录 Cookie 或日常浏览历史。
- **纯本地运行**：所有页面提取、字幕黏连合并和笔记排版逻辑均完全在您的浏览器本地执行。

## 2. 第三方大模型服务交互
- **用户自备 API Key (BYOK)**：所有 AI 智能功能均通过用户在设置中自行配置的官方 API Key 直连服务商。
- **数据交互范围**：仅当用户主动点击生成笔记、解析题目或发起助教问答时，相关的课程字幕片段或题目文本才会发送至对应官方大模型端点（DeepSeek、Google Gemini、OpenAI）。请求中绝不附带任何用户个人账号信息或 Cookie。

## 3. 权限说明
- `storage`: 用于在浏览器本地保存用户偏好设置（如模型配置、5大面板独立路由、自定义 Prompt）与笔记缓存。
- `sidePanel`: 用于承载右侧常驻交互侧边栏。
- `downloads`: 用于支持一键导出 Markdown 笔记、双语字幕 TXT 与测验试题包。
- `scripting` & `tabs`: 用于与当前 Canvas 课程页面安全通信并提取课程公开内容。
- `host_permissions`: 用于在受支持的 Canvas LMS / Echo360 页面运行提取逻辑，以及直连各大模型官方 API。

## 4. 本地工作区访问
若您通过 File System Access API 绑定了本地文件夹，插件仅用于将您生成的笔记和字幕保存到该指定目录中，绝不会读取或扫描该目录以外的任何其他文件。
