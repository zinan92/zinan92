# Hey, it's Park

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

build stuff最重要的就是定goal和success criteria，然后拆解到每一个可以被review/test的atomic unit.

```
调研 research ➜ 设计 plan/design ➜ 开发 code & review ➜ 包装 package ➜ 维护 maintain （后面这两个我不太熟悉，还需要学习）
```

**调研** — 使用dbskill/gstack来聊清楚需求。不凭空造。先找到最像的产品当锚点（"80% TradingView + 20% Koyfin"），截图收集 UI 参考。更高维度的需求和分析可以用naval google来聊：https://gemini.google.com/gem/aafc1ff1539f/5ef401e610e971c5 

**设计** — superpowers/Brainstorm → PRD → 实现计划 → 产品原型图。原型要完全定义最终产品的样式，只是 design 不写代码。这里要deliver prd, implementation plan, ui（现在ui设计还是有点missing）

**开发** — gsd开发。编码 → review → 打回 → 重写，循环直到全部通过。/codex可以在cc里面直接review代码。

**包装** — 产品化。部署上线、CI/CD、README、Landing Page、域名绑定。能跑不等于能用。（现在只有gh readme一个skill改readme，部署，cicd，域名这些都是每次直接做，后期需要固定skill或者流程）

**维护** — 监控告警、用户反馈、迭代优化。（现在没有这方面的流程）

---

## 在造的东西

### 交易

> **一个世界观，交易任何资产。**

8 步管线。每一步是一个独立 capability，定义清楚 input / output。GitHub 上的编号是组织结构，运行时是事件驱动。

```
 01 行情数据    02 情报采集    03 信号合成    04 方法论路由
 ┌──────┐    ┌──────┐    ┌──────┐    ┌──────┐
 │kline │───▶│intel │───▶│signal│───▶│copil-│
 │      │    │      │    │      │    │ot    │
 └──────┘    └──────┘    └──────┘    └──────┘
     ●           ●           ◐           ●

 05 回测验证    06 风控决策    07 执行引擎    08 复盘学习
 ┌──────┐    ┌──────┐    ┌──────┐    ┌──────┐
 │back- │    │risk  │───▶│execu-│───▶│journ-│
 │test  │    │      │    │tor   │    │al    │
 └──────┘    └──────┘    └──────┘    └──────┘
     ●           ◐           ◐           ◐

 ● = 已有   ◐ = 有代码种子(tradinghouse)   ○ = 待建
```

**已有的 capability：**

- **01 行情数据** — in ticker+timeframe → out OHLCV candles。A股/美股/加密/商品（[kline](https://github.com/zinan92/kline)）
- **02 情报采集** — in 10+ 信息源 → out LLM 评分 + 跨源事件聚类（[intel](https://github.com/zinan92/intel)）
- **03 信号合成** — in OHLCV + 事件 → out 归一化交易信号（[signal](https://github.com/zinan92/signal)）
- **04 方法论路由** — in 信号 + 上下文 → out 44 套方法论匹配分析（[copilot](https://github.com/zinan92/copilot)）
- **05 回测验证** — in 策略定义 → out 胜率 / 盈亏比 / 最大回撤（[backtest](https://github.com/zinan92/backtest)）
- **06 风控决策** — in 信号 + 分析 + 持仓 → out 交易计划（方向/入场/止损/仓位）（[risk](https://github.com/zinan92/risk)）
- **07 执行引擎** — in 交易计划 → out API 下单 + 执行确认（[executor](https://github.com/zinan92/executor)）
- **08 复盘学习** — in 执行记录 + 原始信号 → out 归因分析 + 月度复盘（[journal](https://github.com/zinan92/journal)）

**To-Do：**

- [ ] **数据源补齐** — 外汇/债券/商品 OHLCV 接入
  📍 kline
- [ ] **资产关联图谱** — 跨资产因果关系建模，宏观事件 → 各资产预期方向
  📍 signal
- [ ] **回测泛化** — 从缠论专用 → 任意策略 + 任意资产
  📍 backtest
- [ ] **实盘对接** — Alpaca (美股) → Binance (加密) → 东方财富 (A股)
  📍 executor
- [ ] **统一世界观引擎** — 所有资产、所有数据源融合成一份研判
  📍 risk
- [ ] **A 股端到端闭环** · **美股端到端闭环** · **加密端到端闭环**
  📍 全部 8 个 stage 贯通即达成

<details>
<summary>📦 相关项目与工具</summary>

📊 **[quant-data-pipeline](https://github.com/zinan92/quant-data-pipeline)** — 原始多市场数据平台（28 组 API，8 数据源）。kline + signal 的代码种子来源

🔖 [daily_stock_analysis](https://github.com/ZhuLinsen/daily_stock_analysis) — LLM 每日自动研判，GitHub Actions 零成本运行

</details>

---

### 内容

> **创作者负责思考，机器负责其他一切。**

终局是一条 8 步管线。每一步是一个独立 capability，定义清楚 input / output / failure，做到极致。

```
 01 信号发现    02 内容获取    03 内容理解    04 选题决策
 ┌──────┐    ┌──────┐    ┌──────┐    ┌──────┐
 │signal│───▶│downl-│───▶│extra-│───▶│cura- │
 │scanner│    │oader │    │ctor  │    │tor   │
 └──────┘    └──────┘    └──────┘    └──────┘
     ○           ●           ●           ○

 05 内容生产    06 成品组装    07 分发       08 反馈学习
 ┌──────┐    ┌──────┐    ┌──────┐    ┌──────┐
 │rewri-│───▶│asset │───▶│publi-│───▶│perfo-│
 │ter   │    │studio│    │sher  │    │rmance│
 └──────┘    └──────┘    └──────┘    └──────┘
     ●           △           ●           ○

 ● = 已有   △ = 有底座   ○ = 待建
```

**已有的 capability：**

- **02 内容获取** — URL 进去，原始文件 + 元数据出来。adapter 架构支持 4 平台，抖音需 cookies（[content-downloader](https://github.com/zinan92/content-downloader)）
- **03 内容理解** — 视频转录 + 图片 OCR + 文章清洗 + 图集叙事合成 → 结构化文本。支持裸视频文件直接提取（[content-extractor](https://github.com/zinan92/content-extractor)）
- **05 内容生产** — 跨平台改写引擎。支持裸 .md/.txt 直接改写，--from/--to 有默认值（[content-rewriter](https://github.com/zinan92/content-rewriter)）
- **06 成品组装** — 7 个视频编辑 CLI + pipeline 串联 + 批量处理 + AI 降级兜底（[videocut](https://github.com/zinan92/videocut)）
- **07 分发** — 7 平台定时批量发布，manifest.json 驱动（[social-auto-upload](https://github.com/dreammis/social-auto-upload)）
- **00 统一入口** — `content <能力> [参数]`，6 个能力按需安装，中文 help，智能错误提示（[content-toolkit](https://github.com/zinan92/content-toolkit)）

**To-Do（按管线顺序）：**

- [ ] **01 signal-scanner** — 跨平台信号扫描 + 趋势检测
  📍 新 repo（intelligence 能力并入）
  ✅ 配置关注列表后，输出每日 scored signal feed

- [ ] **04 content-curator** — 从 100 条里选 3 条值得做的
  📍 新 repo
  ✅ 输入一批结构化内容 + 创作者画像，输出 ranked picks + 角度建议 + 理由

- [x] **06 重构 videocut** — ~~拆出独立能力~~ 已完成：7 个 CLI 能力 + pipeline 串联 + 91 tests
  📍 videocut
  ✅ `videocut autocut` / `subtitle` / `hook` / `clip` / `cover` / `speed` / `pipeline`

- [x] **07 content-publisher** — 使用 [social-auto-upload](https://github.com/dreammis/social-auto-upload) 作为发布引擎
  📍 content-toolkit（batch-publish 编排脚本）· social-auto-upload（执行引擎）
  ✅ 抖音/小红书/B站/快手/视频号/TikTok 定时批量发布

- [ ] **08 performance-tracker** — 发布后追踪表现，归因到选题
  📍 新 repo
  ✅ 跨平台数据回收，输出 what worked / what didn't

<details>
<summary>📦 相关项目与工具</summary>

**采集**

🍴 [MediaCrawler](https://github.com/NanmiCoder/MediaCrawler) — 多平台主动爬虫，覆盖小红书/抖音/快手/B站/微博

🍴 [wechat-article-exporter](https://github.com/wechat-article/wechat-article-exporter) — 微信公众号文章批量导出 · 8k⭐

**视频生产**

🔖 [seedance-expert](https://github.com/zinan92/seedance-expert) — 即梦 2.0 视频 prompt 技能

🔖 [remotion-skills](https://github.com/remotion-dev/skills) — React 程序化视频生成

🍴🔖 [AI-videos](https://github.com/zinan92/AI-videos) — 虚拟角色视频管线 · RunningHub 模型对比

**分发**

[social-auto-upload](https://github.com/dreammis/social-auto-upload) — Patchright 驱动的多平台自动发布引擎，7 个平台 · 作为 content-toolkit 的 publish capability

🍴 [xiaohongshu-skills](https://github.com/autoclaw-cc/xiaohongshu-skills) — 小红书全功能自动化（搜索/互动/发布），Chrome Extension 架构

**图片生产**

🔖 [text-to-image-prompt-optimizer](https://github.com/manzxiao/text-to-image-prompt-optimizer) — 全平台图片 Prompt 优化

🔖 [midjourney-replicate-flux](https://github.com/rawveg/skillsforge-marketplace) — FLUX 1.1 Pro 产品摄影级出图

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
