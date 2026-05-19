# BrandVision AI · Methodology

> **High-Decision Consumer Brand AI Search Visibility Monitoring · Methodology Repository**
>
> 高决策消费品牌 AI 搜索能见度监测平台 · 方法论展示仓库

[English](#english) · [中文](#中文)

---

## English

**BrandVision AI** is an AI search visibility monitoring platform for high-decision consumer brands. It addresses systemic new risks brands face in AI answers — being suppressed by competitors, having key specs misstated, AI actively diverting traffic to competitors, and loss of content asset control.

This repository documents the **public methodology framework** — the conceptual architecture, evaluation dimensions, and engineering principles. Proprietary formulas, weights, thresholds, and client data are **not** disclosed here.

### Three Product Modules

| Module | Function |
|---|---|
| **BrandVision Monitor** | Continuous AI search visibility tracking across 10 major AI answer engines |
| **Brand Risk Radar** | Real-time alerting on incorrect specs, outdated pricing, competitor traffic diversion, standard misstatements |
| **Content Asset Governance** | Reverse-GEO content investment and correction recommendations |

### Engine Coverage

- **Domestic (live)**: DeepSeek · Doubao · Tongyi · Wenxin · Kimi · GLM
- **International (Q3)**: ChatGPT · Claude · Gemini · Perplexity

### 8-Dimension Scorecard (Concept)

**5 dimensions aligned with international methodology** (Profound / AthenaHQ):
1. Brand Answer Share
2. Recommendation Rate
3. Substitution Rate
4. Semantic Position (head / mid / tail)
5. Citation Source Structure

**3 unique extensions** (BrandVision AI proprietary):
6. Cross-Engine Consistency Index
7. Citation Source Weighting Model
8. Risk Discourse Classification System

> Specific weights, thresholds, and computation formulas are proprietary and not published in this repository.

### 5-Agent Collaboration Architecture

```
Collector → Parser → Analyst → Reporter → Watchdog
```

See [ARCHITECTURE.md](./ARCHITECTURE.md) for details.

### Repository Contents

- [`METHODOLOGY.md`](./METHODOLOGY.md) — 8-dimension scorecard conceptual framework
- [`ARCHITECTURE.md`](./ARCHITECTURE.md) — 5-Agent collaboration architecture
- [`WHITEPAPER.md`](./WHITEPAPER.md) — Methodology whitepaper (redacted)
- [`examples/`](./examples/) — Sample prompt sets and output formats (using public brands)

---

## 中文

**BrandVision AI** 是面向高决策消费品牌的 AI 搜索能见度监测平台。解决品牌在 AI 答案中被竞品压制、关键参数被误述、AI 主动导流竞品、内容资产失控等系统性新风险。

本仓库展示**公开方法论框架** — 概念架构、评估维度、工程原则。专有的公式、权重、阈值与客户数据不在此公开。

### 产品三模块

| 模块 | 功能 |
|---|---|
| **BrandVision Monitor** | 跨 10 大主流 AI 答案引擎的持续能见度监测 |
| **Brand Risk Radar** | 错误参数 / 过时定价 / AI 导流竞品 / 行业标准误述的实时分级告警 |
| **Content Asset Governance** | 反向 GEO 的内容投放与修正建议 |

### 引擎覆盖

- **国产已就位**：DeepSeek / 豆包 / 通义 / 文心 / Kimi / GLM
- **海外 Q3 接入**：ChatGPT / Claude / Gemini / Perplexity

### 8 维评分卡（概念）

**5 维国际方法学对齐**（对标 Profound / AthenaHQ）：
1. 品牌出现率（Answer Share）
2. 主动推荐率（Recommendation Rate）
3. 竞品替代率（Substitution Rate）
4. 语义位置（答案头 / 中 / 尾）
5. 引用源结构（Citation Tracking）

**3 维独有扩展**（BrandVision AI 自研）：
6. 跨引擎一致性指数
7. 引用源权重模型
8. 错误话术风险分级

> 具体权重、阈值、计算公式为专有方法学，不在本仓库公开。

### 5 Agent 协同架构

```
Collector（采集）→ Parser（解析）→ Analyst（分析）→ Reporter（报告）→ Watchdog（监察）
```

详见 [ARCHITECTURE.md](./ARCHITECTURE.md)。

### 仓库结构

- [`METHODOLOGY.md`](./METHODOLOGY.md) — 8 维评分卡概念框架
- [`ARCHITECTURE.md`](./ARCHITECTURE.md) — 5 Agent 协同架构
- [`WHITEPAPER.md`](./WHITEPAPER.md) — 方法论白皮书（脱敏版）
- [`examples/`](./examples/) — 示例问题集与输出格式（使用公开品牌）

---

## Contact

**Hu Wei (Will)** · Owner & Founder, BrandVision AI

📧 will@will-luck.com
🏢 Shenzhen, China

---

## License

MIT License — see [LICENSE](./LICENSE)

© 2026 BrandVision AI. Methodology documentation only. Proprietary formulas, weights, and client data not included.
</content>
