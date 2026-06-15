# CHANGELOG.md — 投资项目IT职能助手

## 2026-06-15

### v1.0.3 — 可拖拽分割 + 公网部署
- **新增:** 左右面板可拖拽分割线，拖动时实时调整宽度
- **修复:** GitHub Pages 部署后 API 调用指向公网服务器 `http://1.14.77.3/it`
- **优化:** 初始页纯居中对话框，首次输入后过渡到双栏布局
- **部署:** GitHub Pages → https://commaluanqibazao.github.io/investment-it-tool/

### v1.0.2 — 接入真实 DeepSeek API
- **修复:** 前端替换模拟数据，通过后端 server.js 调用 DeepSeek API
- **新增:** 后端同时托管静态文件和 API，`node server.js` 一键启动
- **部署:** Nginx 反向代理 `1.14.77.3/it/` → `localhost:3200`

### v1.0.1 — 修复关键词匹配
- **修复:** 增加「投前分析」「正大」等关键词，避免被拦截

### v1.0.0 — 初始版本
- 双栏布局（左对话 / 右文档预览）
- 输入验证（仅限投资项目 IT 职能工作）
- 模拟报告生成（3种模板）
- 支持 .md / .doc 导出
