# 嘿，我是 parkzz

> 我自动化交易，自动化写代码，自动化做视频。
> 正在研究怎么自动化睡觉。

上海

![Python](https://img.shields.io/badge/-Python-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/-FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![TypeScript](https://img.shields.io/badge/-TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Claude](https://img.shields.io/badge/-Claude-000000?style=flat-square&logo=anthropic&logoColor=white)
![SQLite](https://img.shields.io/badge/-SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white)
![Shell](https://img.shields.io/badge/-Shell-121212?style=flat-square&logo=gnu-bash&logoColor=white)

---

🍴 = Fork 他人的项目 · 🔖 = 备选（还没用，未来可能用）

---

## 我怎么造东西

每个项目都走同一条线，AI 干活，我做决策。

```
调研 ➜ 设计 ➜ 开发 ➜ 包装 ➜ 维护
```

**调研** — 不凭空造。先找到最像的产品当锚点（"80% TradingView + 20% Koyfin"），截图收集 UI 参考。

**设计** — Brainstorm → PRD → 实现计划 → 产品原型图。原型要完全定义最终产品的样式，只是 design 不写代码。

**开发** — 交给 Droid。Orchestrator 拆任务分发给 worker agents，编码 → review → 打回 → 重写，循环直到全部通过。

**包装** — 产品化。部署上线、CI/CD、README、Landing Page、域名绑定。能跑不等于能用。

**维护** — 监控告警、用户反馈、迭代优化。能用不等于能卖。

---

## 在造的东西

### 交易

`数据采集` ➜ `分析` ➜ `决策`

#### 数据采集

**[quant-data-pipeline](https://github.com/zinan92/quant-data-pipeline)** — A股/美股/期货行情数据 → 标准化 SQLite 存储 + FastAPI 查询接口

**[qualitative-data-pipeline](https://github.com/zinan92/qualitative-data-pipeline)** — 交易信号情报系统。10+ 信息源 → 跨源事件聚类 → AI 叙事生成 → 标的价格影响评分 → 力导向星座图可视化

#### 分析

🔖 [daily_stock_analysis](https://github.com/ZhuLinsen/daily_stock_analysis) — LLM 每日自动研判，GitHub Actions 零成本运行

#### 决策

🔖 [trading-copilot](https://github.com/zinan92/trading-skills-catalog) — 跟 AI 说你的交易想法，它从 44 套方法论中选最合适的给你分析。免费用

### 内容

`收集` ➜ `分析` ➜ `生产`

#### 收集

**[XHS-Downloader](https://github.com/JoeanAmier/XHS-Downloader)** — 小红书图文/视频批量提取 · 10k⭐

🍴 **[MediaCrawler](https://github.com/NanmiCoder/MediaCrawler)** — 多平台主动爬虫，覆盖小红书/抖音/快手/B站/微博 5 大平台

🍴 **[douyin-downloader](https://github.com/zinan92/douyin-downloader-1)** — 抖音批量下载，去重 + 重试 + 浏览器兜底 + Whisper 语音转录

🍴 **[wechat-article-exporter](https://github.com/wechat-article/wechat-article-exporter)** — 微信公众号文章批量导出为离线可读格式 · 8k⭐

🔖 [res-downloader](https://github.com/putyy/res-downloader) — 被动资源嗅探，无需登录即可抓取页面媒体

🔖 [Scrapling](https://github.com/D4Vinci/Scrapling) — 通用爬虫框架，自适应解析 + 反检测

🔖 [RedBox](https://github.com/Jamailar/RedBox) — 小红书创作工作台，内容管理 + 数据分析

#### 分析

**[intelligence](https://github.com/zinan92/intelligence)** — 多品类内容研究引擎。JSONL 输入 → 自动评分 + 结构化分析报告

#### 生产 · 视频

**[videocut](https://github.com/zinan92/videocut)** — 录一次，全平台发。自动剪辑 → 字幕 → 文章 → 卡片 → 发布到 8 个平台

🔖 [seedance-expert](https://github.com/zinan92/seedance-expert) — Claude Code 技能，让你变成即梦 2.0 导演。10 种任务类型，50+ 提示词模板

🔖 [seedance-2.0-prompter](https://github.com/pexoai/pexo-skills) — Seedance 结构化 Prompt 工程，场景/镜头/风格一键生成

🔖 [seedance-storyboard](https://github.com/elementsix/elementsix-skills) — 即梦 Seedance 分镜脚本生成器

🔖 [MoneyPrinterV2](https://github.com/FujiwaraChoki/MoneyPrinterV2) — 自动化内容赚钱，YouTube/Twitter 视频批量生成 · 23k⭐

🍴🔖 [AI-videos](https://github.com/zinan92/AI-videos) — 虚拟角色视频管线。Klein 换装 + Kling 动作迁移 + RunningHub 模型对比

🍴🔖 [mm-easy-voice](https://github.com/openclaw/skills/tree/main/skills/blue-coconut/mm-easy-voice) — MiniMax 语音合成技能，一句话生成自然人声

🔖 [remotion-skills](https://github.com/remotion-dev/skills) — Remotion 程序化视频生成，React 写视频

🔖 [gsap-skills](https://github.com/greensock/gsap-skills) — GSAP 官方动画技能包，专业级 Web 动画

🍴🔖 [libtv-skills](https://github.com/libtv-labs/libtv-skills) — LibLib.tv AIGC 平台技能，通过 OpenAPI 生成图片和视频

#### 生产 · 图

🔖 [text-to-image-prompt-optimizer](https://github.com/manzxiao/text-to-image-prompt-optimizer) — 全平台图片 Prompt 优化，支持 Gemini/Midjourney/SD/DALL-E

🔖 [midjourney-replicate-flux](https://github.com/rawveg/skillsforge-marketplace) — 产品摄影级 Prompt 工程 + FLUX 1.1 Pro 出图

🍴🔖 [frontend-slides](https://github.com/zarazhangrui/frontend-slides) — Claude Code 技能，从零或从 PPT 生成动画丰富的 HTML 演示文稿

### 开发工具

`框架` ➜ `自动化` ➜ `增强`

#### 框架

**[doc-driven-dev-workflow](https://github.com/zinan92/doc-driven-dev-workflow)** — 5 阶段 / 22 步的文档驱动开发框架。内置 task scaffolding、workflow guards、状态机 + 本地 observer dashboard

🍴 **[get-shit-done](https://github.com/gsd-build/get-shit-done)** — GSD 开发框架。AI 自主规划→执行→验证，全流程自动化

🍴 **[superpowers](https://github.com/obra/superpowers)** — AI 编程工作流。7 阶段方法论 + TDD 驱动，从头脑风暴到代码审查

**[proactive-explorer](https://github.com/zinan92/proactive-explorer)** — 下一步做什么？5 维框架，帮 v1 项目找到产品方向

🔖 [deer-flow](https://github.com/bytedance/deer-flow) — 字节跳动 SuperAgent，研究/编码/创作全能 · 40k⭐

🔖 [agent-core](https://github.com/zinan92/agent-core) — Agent 的操作系统，由 Agent 自己构建。生命周期 + 工具 + 记忆管理

🔖 [skills-repo](https://github.com/zinan92/skills-repo) — 61 个 AI Agent 技能，按领域分组 + frontmatter 路由

#### 自动化

🍴 **[bb-browser](https://github.com/zinan92/bb-browser)** — 你的浏览器就是 API。CLI + MCP server，让 AI Agent 控制 Chrome

🍴 **[agent-browser](https://github.com/zinan92/agent-browser)** — 快照驱动的浏览器自动化，专为 AI Agent 设计

🍴 **[web-access](https://github.com/eze-is/web-access)** — 让 Claude Code 完整联网，三层通道（搜索 + 抓取 + API）

🍴🔖 [CLI-Anything](https://github.com/HKUDS/CLI-Anything) — 任何软件一键生成 CLI 界面

🍴🔖 [opencli](https://github.com/zinan92/opencli) — 把任何网站变成你的 CLI。AI 原生浏览器自动化 + 数据提取

#### 增强

🍴 **[self-improving-agent](https://github.com/zhaono1/agent-playbook/tree/main/skills/self-improving-agent)** — 自我进化 Agent，运行后自动分析 + 调优自身性能

🍴🔖 [lossless-claw](https://github.com/zinan92/lossless-claw) — 无损上下文管理插件，防止对话压缩丢信息

🍴🔖 [skill-vetter](https://github.com/openclaw/skills/tree/main/skills/spclaudehome/skill-vetter) — AI Agent 技能质量检查器，自动评估触发准确率 + 输出质量

### 产品评测

Fork → 部署 → 逐条验证 README 承诺 → 记录真实结果与证据。

这里的 repo 都是我实际部署并评估过的工具和 skills。每个都会重写 README：上半部分是 claim-by-claim 的评测结论，下半部分保留原始 README 作为对照。命名规范：`eval__项目名`。

[eval__MoneyPrinterV2](https://github.com/zinan92/eval__MoneyPrinterV2) — 自动化内容赚钱工具（23k⭐），最终结论：能硬跑出 MP4，但 setup 成本高、文档缺失严重、成片质量垃圾，判定失败

---

## 活跃度

![GitHub Contribution Graph](https://ghchart.rshah.org/zinan92)

---

## 冷知识

我所有的 repo 要么是为了赚钱，要么是为了省时间。通常两个都是。

```
行情走势:  ████████████████▄▄  📈
我的睡眠:  ▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄  📉
```
