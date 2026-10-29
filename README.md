# FlowKit · n8n 中文实战工作流（免费开源版）

3 个**零配置、开箱即用**的 n8n 中文工作流模板，配套中文文档。导入即跑，不需要注册任何服务、不需要 API Key。

## 为什么是这 3 个

n8n 上手最难的不是画流程，是"导入了跑不起来"。这 3 个模板刻意选了**不需要任何凭据**的场景，10 分钟内让你看到真实产出：

| 文件 | 用途 | 你会得到 |
|---|---|---|
| `workflows/01-rss-tech-daily.json` | 定时抓 RSS（默认 Hacker News），生成中文技术日报 | 一个可直接打开的日报 HTML |
| `workflows/02-site-change-monitor.json` | 监控任意网页内容变化，输出 changed 字段 | 变更记录 CSV，可接微信/飞书/钉钉推送 |
| `workflows/03-webhook-lead-collector.json` | Webhook 接口，落地页表单/外部系统 POST 即登记 | 线索台账 CSV，可扩展到飞书表格 |

三个模板分别对应 n8n 最核心的三类触发器：**Schedule（定时）、Schedule + 比对（状态化任务）、Webhook（被动接收）**。跑通它们，你就理解了 n8n 80% 的用法。

## 10 分钟跑通

```bash
# 需要 Node.js 20+
mkdir n8n-demo && cd n8n-demo
npm init -y && npm i n8n
npx n8n
```

浏览器打开 http://localhost:5678 注册本地账号 → `Workflows → Import from file` → 选 JSON → 点 `Execute workflow`。

详细步骤、Docker/云服务器部署、常见报错全部写在 [docs/安装与导入指南.md](docs/安装与导入指南.md)。

## 这是什么项目的一部分

[FlowKit 完整版](docs/工作流清单-预览.md)共 15 个中文注释工作流，覆盖信息日报、监控预警、内容创作、办公提效、客服销售、电商运营六大场景（AI 总结、价格监控、周报生成、智能客服等），并附带：

- 全部工作流集中在单一「⚙️ 配置」节点填 Key，不用挨个节点翻
- 《安装与导入指南》：从装 n8n 到跑通生产环境的完整中文文档
- 后续模板更新

闲鱼搜索「**n8n 工作流**」可找到完整版；部署嫌麻烦也提供代部署服务。

## 配套项目

- [flowskill](https://github.com/yh1988/flowskill)：FlowSkill 中文实战 Agent Skills 免费版（Claude Code 一条命令安装：n8n 工作流生成师 / 小红书笔记工坊 / 闲鱼卖家助手）——让 AI 助手替你写 n8n 工作流、写小红书笔记、写闲鱼文案。

## 给完整版用户的提示：AI Key 渠道

完整版里的 AI 工作流（总结、智能客服等）需要你自己的 API Key。官方渠道之外，社区里很多人用「API 中转站」按量付费降低成本。以下是两家被多个大型开源项目（如 70k★ 的 ppt-master）选作赞助商的中转服务，供比价参考——**这些是返利链接（aff），你注册我不加价，我拿一点返佣**：

- [APIKEY.FAN](https://apikey.fan/register?aff=haoyard) — Claude/GPT/DeepSeek 等多模型按量中转
- [RunAPI](https://runapi.host/register?aff=haoyard) — OpenAI 兼容接口中转

> 提示：中转站价格与稳定性随时会变，大额充值前先小额测试；生产/敏感数据场景建议只用官方 API。本仓库与上述服务无隶属关系。

## 环境要求

- n8n 1.x（社区版即可，本仓库 3 个模板在 n8n 2.x 实测通过）
- 无需任何 API Key、无需注册任何账号

## 支持作者

这 3 个模板完全免费、无广告。如果它们帮你省了时间，欢迎在 [爱发电](https://afdian.com/a/haoyard) 上请我喝杯咖啡 ☕——那也是催更完整版模板最有效的方式。

## License

MIT —— 可自由使用、修改、分发（保留署名即可）。欢迎 PR。
