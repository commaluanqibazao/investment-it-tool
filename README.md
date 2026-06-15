# 投资项目IT职能助手 🏗️

一个面向投资项目中 IT 职能工作的 AI 辅助工具。左侧 DeepSeek 式对话界面，右侧文档实时预览。

## 功能

- 🎯 **专项服务** — 仅响应投资项目 IT 职能相关工作（IT尽调、技术评估、风险筛查等）
- 🤖 **Agent 调度** — 识别需求类型后自动调用对应能力生成结构化报告
- 📄 **双栏布局** — 左侧对话 / 右侧文档预览，一目了然
- 📥 **文档导出** — 支持下载 `.md` 和 `.doc` 格式

## 本地运行

直接用浏览器打开 `index.html` 即可：

```bash
open index.html
# 或
python3 -m http.server 8080
# 访问 http://localhost:8080
```

## 部署到 GitHub Pages

1. 创建 GitHub 仓库，将此目录推送到 `main` 分支
2. 仓库 Settings → Pages → 选择 `main` 分支 `/` 根目录
3. 等待自动部署，访问 `https://<你的用户名>.github.io/<仓库名>`

## 与真实 Agent 对接

当前 `callAgent()` 函数返回模拟数据。如需对接真实 Agent（如 OpenClaw risk-analyst）：

```javascript
async function callAgent(userInputText) {
  const response = await fetch('https://your-api-endpoint/agent/run', {
    method: 'POST',
    headers: { 'Content-Type': 'application/json' },
    body: JSON.stringify({ prompt: userInputText, agent: 'risk-analyst' })
  });
  const data = await response.json();
  return data.report;  // 返回 Markdown 格式的报告
}
```

## 技术栈

纯前端 HTML + CSS + JavaScript，零依赖。
