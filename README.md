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

> **一个世界观，交易任何资产。**

不管是 A 股、美股、加密、黄金、外汇还是债券，所有资产共享同一个宏观判断。通过多源数据融合形成统一世界观，再从世界观推导出每个资产的交易决策。

```
数据标准化                    融合分析                 决策与执行

Quantitative ──┐         ┌─ 信号检测 ──┐         ┌─ 策略生成
 K线/指标/资金   │         │  异常/突破/模式 │         │  入场/止盈/止损
 A股/美股/加密   ├── 标准化 ─┤             ├─ 世界观 ─┤
 商品/债券/外汇   │   接口   │  叙事生成    │   形成   │  执行连接
Qualitative ──┘         │  跨源聚类    │         │  交易所API
 新闻/研报/社媒           └─ 宏观关联 ──┘         └─ 风控监控
```

**现在能做到的：**

- **多市场行情标准化采集** — 1900+ A 股、美股、加密、商品，28 组 API，8 数据源（[quant-data-pipeline](https://github.com/zinan92/quant-data-pipeline)）
- **多源信号情报聚合** — 10+ 信息源 → 跨源事件聚类 → AI 叙事生成 → 星座图可视化（[qualitative-data-pipeline](https://github.com/zinan92/qualitative-data-pipeline)）
- **感知信号引擎** — 价格突破、量价异常、资金流、技术形态自动检测（[quant-data-pipeline](https://github.com/zinan92/quant-data-pipeline)）
- **模拟交易** — 纸上交易、持仓跟踪、盈亏计算（[quant-data-pipeline](https://github.com/zinan92/quant-data-pipeline)）
- **44 套交易方法论对话决策**（[trading-copilot](https://github.com/zinan92/trading-skills-catalog)）

**To-Do：**

- [ ] **A 股端到端闭环** — 现有数据 + 感知信号 → 结构化交易建议（入场/止盈/止损）
  📍 quant-data-pipeline · qualitative-data-pipeline
  ✅ 给定一只股票，系统输出完整的交易计划（方向、入场价、止损、目标价、依据）

- [ ] **回测验证** — 用历史数据验证交易建议的胜率
  📍 quant-data-pipeline
  ✅ 任意策略可跑 1 年回测，输出胜率/盈亏比/最大回撤

- [ ] **实盘 API 对接** — 先接一个交易所（Alpaca 美股）
  📍 quant-data-pipeline
  ✅ 能通过 API 下单、查持仓、查订单状态

- [ ] **风控系统** — 仓位管理 + 止损执行 + 暴露监控
  📍 quant-data-pipeline
  ✅ 超过预设风险阈值自动报警或拒绝下单

- [ ] **美股端到端闭环** — 复制 A 股闭环到美股
  📍 quant-data-pipeline
  ✅ 美股也能输出完整交易计划 + 实盘执行

- [ ] **加密端到端闭环** — 接币安 API，复制闭环
  📍 quant-data-pipeline
  ✅ 加密资产也能走完 数据→建议→执行

- [ ] **资产关联图谱** — 跨资产因果关系建模
  📍 quant-data-pipeline · qualitative-data-pipeline
  ✅ 输入宏观事件（如"美联储加息"），输出各资产预期方向

- [ ] **统一世界观引擎** — 所有资产、所有数据源融合成一份研判
  📍 全部 trading repos
  ✅ 一份报告覆盖股/债/汇/商品/加密的统一观点和交易建议

- [ ] **外汇/债券/商品数据源补齐**
  📍 quant-data-pipeline
  ✅ 覆盖主要外汇对、美国国债、原油/黄金/铜

- [ ] **交易日志与自动复盘** — 每笔交易归因到触发信号
  📍 quant-data-pipeline
  ✅ 交易记录自动关联原始信号，月度复盘报告

<details>
<summary>📦 相关项目与工具</summary>

📊 **[quant-dashboard](https://github.com/zinan92/quant-dashboard)** — A股缠论量化回测看板。分型→笔→中枢→背驰→买卖点全流程 + 组合回测 + QuantStats 绩效报告 + Bokeh 交互图

🔖 [daily_stock_analysis](https://github.com/ZhuLinsen/daily_stock_analysis) — LLM 每日自动研判，GitHub Actions 零成本运行

</details>

---

### 内容

> **创作者负责思考，机器负责其他一切。**

从趋势洞察到内容发布，创作环节是人的判断，其他环节全部自动化。最终目标：把这套管线开放给其他创作者。

```
趋势洞察              人工创作              自动化后处理           分发与追踪

多平台采集 ──┐                         ┌─ 自动剪辑 ──┐
 小红书/抖音  │    ┌──────────┐        │  字幕/拆条   │    ┌─ 多平台发布
 微信/微博    ├──▶ │  你的大脑  │ ──▶   ├─ 文章生成   ├──▶ │  抖音/小红书
 Twitter/RSS │    └──────────┘        │  卡片/封面   │    │  微信/视频号
趋势分析 ───┘                         └─ 格式适配 ──┘    │  Twitter
 评分/聚类                                              └─ 效果追踪
 热度排名                                                  点赞/转发/评论
```

**现在能做到的：**

- **多平台内容采集** — 小红书、抖音、微信公众号批量下载 + 语音转录（[XHS-Downloader](https://github.com/JoeanAmier/XHS-Downloader), [douyin-downloader](https://github.com/zinan92/douyin-downloader-1)）
- **趋势情报分析** — 多品类内容评分、趋势聚类、结构化报告 + 交互式 Dashboard（[intelligence](https://github.com/zinan92/intelligence)）
- **录制到发布一条龙** — 自动剪辑 → 字幕 → 文章 → 卡片 → 发布到 8 个平台（[videocut](https://github.com/zinan92/videocut)）

**To-Do：**

- [ ] **抖音→小红书转化** — 成品抖音视频自动生成小红书图文/切片
  📍 videocut
  ✅ 输入一个抖音视频，输出小红书格式的图文帖（封面+正文+标签）

- [ ] **抖音→微信转化** — 成品视频自动适配微信视频号 + 公众号文章
  📍 videocut
  ✅ 视频号直接复制；公众号输出图文文章（含关键帧截图+文字整理）

- [ ] **智能拆条** — 长视频自动识别高光片段生成 short
  📍 videocut
  ✅ 输入 30 分钟视频，输出 5-8 个 60 秒 short

- [ ] **多平台一键分发** — 生成的内容自动发布到各平台
  📍 videocut
  ✅ 一个命令发布到抖音+小红书+视频号+公众号

- [ ] **趋势预警推送** — 品类/话题升温时 Telegram 通知
  📍 intelligence
  ✅ 配置关注品类后，自动推送热度异动

- [ ] **竞品内容监控** — 跟踪指定账号发布和互动趋势
  📍 intelligence
  ✅ 配置竞品账号列表，每周报告

- [ ] **内容效果追踪** — 各平台数据自动回收
  📍 videocut · intelligence
  ✅ 统一 Dashboard 看各平台点赞/转发/评论

- [ ] **个人风格训练** — 基于历史内容学习表达风格
  📍 intelligence
  ✅ 输入过往内容，输出风格指南

- [ ] **商业化封装** — 管线打包为 SaaS
  📍 新 repo
  ✅ 其他创作者能用完整的 采集→分析→生产→分发→追踪 管线

<details>
<summary>📦 相关项目与工具</summary>

**采集**

🍴 [MediaCrawler](https://github.com/NanmiCoder/MediaCrawler) — 多平台主动爬虫，覆盖小红书/抖音/快手/B站/微博 5 大平台

🍴 [wechat-article-exporter](https://github.com/wechat-article/wechat-article-exporter) — 微信公众号文章批量导出为离线可读格式 · 8k⭐

🔖 [res-downloader](https://github.com/putyy/res-downloader) — 被动资源嗅探，无需登录即可抓取页面媒体

🔖 [Scrapling](https://github.com/D4Vinci/Scrapling) — 通用爬虫框架，自适应解析 + 反检测

🔖 [RedBox](https://github.com/Jamailar/RedBox) — 小红书创作工作台，内容管理 + 数据分析

**生产 · 视频**

🔖 [seedance-expert](https://github.com/zinan92/seedance-expert) — Claude Code 技能，让你变成即梦 2.0 导演。10 种任务类型，50+ 提示词模板

🔖 [seedance-2.0-prompter](https://github.com/pexoai/pexo-skills) — Seedance 结构化 Prompt 工程，场景/镜头/风格一键生成

🔖 [seedance-storyboard](https://github.com/elementsix/elementsix-skills) — 即梦 Seedance 分镜脚本生成器

🔖 [MoneyPrinterV2](https://github.com/FujiwaraChoki/MoneyPrinterV2) — 自动化内容赚钱，YouTube/Twitter 视频批量生成 · 23k⭐

🍴🔖 [AI-videos](https://github.com/zinan92/AI-videos) — 虚拟角色视频管线。Klein 换装 + Kling 动作迁移 + RunningHub 模型对比

🍴🔖 [mm-easy-voice](https://github.com/openclaw/skills/tree/main/skills/blue-coconut/mm-easy-voice) — MiniMax 语音合成技能，一句话生成自然人声

🔖 [remotion-skills](https://github.com/remotion-dev/skills) — Remotion 程序化视频生成，React 写视频

🔖 [gsap-skills](https://github.com/greensock/gsap-skills) — GSAP 官方动画技能包，专业级 Web 动画

🍴🔖 [libtv-skills](https://github.com/libtv-labs/libtv-skills) — LibLib.tv AIGC 平台技能，通过 OpenAPI 生成图片和视频

**生产 · 图**

🔖 [text-to-image-prompt-optimizer](https://github.com/manzxiao/text-to-image-prompt-optimizer) — 全平台图片 Prompt 优化，支持 Gemini/Midjourney/SD/DALL-E

🔖 [midjourney-replicate-flux](https://github.com/rawveg/skillsforge-marketplace) — 产品摄影级 Prompt 工程 + FLUX 1.1 Pro 出图

🍴🔖 [frontend-slides](https://github.com/zarazhangrui/frontend-slides) — Claude Code 技能，从零或从 PPT 生成动画丰富的 HTML 演示文稿

</details>

---

### 开发工具

> **造东西时顺手造出的工具，自用 → 沉淀 → 开源。**

开发流程已标准化，Doc-Driven Workflow 驱动所有项目。

```
开发框架              自动化工具             增强能力

[GSD]               [bb-browser]         [self-improving-agent]
 规划→执行→验证        浏览器即API             自我进化
[superpowers]       [agent-browser]
 7阶段工作流           快照驱动自动化
[proactive-explorer]
 产品方向探索
        │                   │                     │
        └───────── 全部服务于 Trading + Content ──────┘
```

**现在能做到的：**

- **文档驱动开发框架** — 5 阶段 / 22 步，内置 task scaffolding + workflow guards + 状态机（[doc-driven-dev-workflow](https://github.com/zinan92/doc-driven-dev-workflow)）
- **AI 驱动全流程开发** — 规划→执行→验证自动化（[GSD](https://github.com/gsd-build/get-shit-done), [superpowers](https://github.com/obra/superpowers)）
- **浏览器自动化** — AI Agent 控制 Chrome，快照驱动交互（[bb-browser](https://github.com/zinan92/bb-browser), [agent-browser](https://github.com/zinan92/agent-browser)）
- **产品方向发现** — 5 维框架帮 v1 项目找下一步（[proactive-explorer](https://github.com/zinan92/proactive-explorer)）

<details>
<summary>📦 相关项目与工具</summary>

**框架**

🔖 [deer-flow](https://github.com/bytedance/deer-flow) — 字节跳动 SuperAgent，研究/编码/创作全能 · 40k⭐

🔖 [agent-core](https://github.com/zinan92/agent-core) — Agent 的操作系统，由 Agent 自己构建。生命周期 + 工具 + 记忆管理

🔖 [skills-repo](https://github.com/zinan92/skills-repo) — 61 个 AI Agent 技能，按领域分组 + frontmatter 路由

**自动化**

🍴 [web-access](https://github.com/eze-is/web-access) — 让 Claude Code 完整联网，三层通道（搜索 + 抓取 + API）

🍴🔖 [CLI-Anything](https://github.com/HKUDS/CLI-Anything) — 任何软件一键生成 CLI 界面

🍴🔖 [opencli](https://github.com/zinan92/opencli) — 把任何网站变成你的 CLI。AI 原生浏览器自动化 + 数据提取

**增强**

🍴 [self-improving-agent](https://github.com/zhaono1/agent-playbook/tree/main/skills/self-improving-agent) — 自我进化 Agent，运行后自动分析 + 调优自身性能

🍴🔖 [lossless-claw](https://github.com/zinan92/lossless-claw) — 无损上下文管理插件，防止对话压缩丢信息

🍴🔖 [skill-vetter](https://github.com/openclaw/skills/tree/main/skills/spclaudehome/skill-vetter) — AI Agent 技能质量检查器，自动评估触发准确率 + 输出质量

</details>

---

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
