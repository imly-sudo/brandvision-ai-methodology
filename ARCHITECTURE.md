# 5-Agent Collaboration Architecture

> Engineering architecture for multi-engine AI search visibility monitoring.
> 多引擎 AI 搜索能见度监测的工程化架构。

---

## Overview

BrandVision AI operates as a one-person company augmented by five specialized AI agents working in collaboration. Each agent has a defined role, input, and output, with rigorous handoff protocols between stages.

```
┌──────────┐    ┌────────┐    ┌─────────┐    ┌──────────┐    ┌──────────┐
│Collector │ → │ Parser │ → │ Analyst │ → │ Reporter │ → │ Watchdog │
└──────────┘    └────────┘    └─────────┘    └──────────┘    └──────────┘
   采集            解析           分析            报告            监察
```

## Agent Roles

### 1. Collector · 采集

**Role**: Multi-engine task scheduling and pattern locking.

**Function**:
- Schedules query execution across 10 target AI engines
- Locks engine state to ensure reproducibility (e.g., web search on / deep thinking off)
- Captures raw browser-side responses with full HTML context

**Output**: Raw answer corpus with engine metadata

### 2. Parser · 解析

**Role**: Structured extraction from raw answers.

**Function**:
- Normalizes 6 different domestic engine response formats into a unified schema
- Extracts citation sources from answer HTML structure
- Performs automated data validity verification

**Output**: Structured records with brand mentions, positions, citations

### 3. Analyst · 分析

**Role**: Cross-engine comparison and risk discourse identification.

**Function**:
- Computes 8-dimension scorecard metrics
- Identifies risk discourse patterns (incorrect specs, outdated pricing, competitor diversion)
- Uses LLM secondary reasoning for nuanced classification
- Computes cross-engine consistency scores

**Output**: Scored matrix + risk discourse alerts

### 4. Reporter · 报告

**Role**: Automated diagnostic report generation.

**Function**:
- Template-driven report assembly
- LLM-driven prose generation for executive summary
- Content governance recommendation drafting

**Output**: Client-ready diagnostic report + governance recommendations

### 5. Watchdog · 监察

**Role**: Anomaly alerting and three-gate quality verification.

**Function**:
- Real-time alerting on anomalous risk discourse
- **Three-gate data quality SOP**:
  1. Answer structure verification (post-parsing)
  2. Noise filtering (ad / SEO / aggregator deweighting)
  3. Sampled human re-verification

**Output**: Quality-assured dataset + escalation alerts

---

## Key Engineering Principles

### 1. Browser-Side Measurement

All data collection happens through real browser execution, not static API calls. This:
- Reflects the experience of actual users
- Captures engine-specific UI elements (citations, recommended next-questions, etc.)
- Avoids API rate-limit artifacts that distort static-call sampling

### 2. Engine State Locking

Each engine has multiple operational modes (web search on/off, deep thinking on/off, model variant selection). Without locking, the same query produces different answers — making measurement meaningless.

The Collector locks each engine to a single canonical state before any measurement.

### 3. Statistical Verification Built In

Repeatability and reproducibility verification are not afterthoughts — they are integrated into the Analyst stage. Every published score has confidence intervals.

### 4. Reverse-GEO as Output

Most GEO tools stop at measurement. BrandVision AI continues into the Content Asset Governance module, where citation source structure analysis informs reverse-engineering of content investment priorities.

---

## What's Not in This Repository

The following are proprietary and not published:

- Engine-specific Collector configurations
- Parser regex / DOM selectors per engine
- Analyst prompt templates for risk discourse classification
- Citation source authority tier database
- Cross-engine consistency formula

---

## 中文摘要

### 五个 Agent 角色

| Agent | 职能 | 核心功能 |
|---|---|---|
| **Collector 采集** | 多引擎任务调度 + 模式锁定 | 跨 10 大引擎调度，浏览器端原始答案抓取 |
| **Parser 解析** | 答案结构化 + 引用源提取 | 6 引擎统一解析规则，数据有效性自动验证 |
| **Analyst 分析** | 跨引擎对照 + 风险话术识别 | 8 维评分计算，LLM 深度推理 |
| **Reporter 报告** | 诊断报告自动生成 | 模板驱动 + LLM 段落撰写 |
| **Watchdog 监察** | 异常告警 + 三关核证 | 答案结构验证 → 噪音过滤 → 抽样复核 |

### 工程化原则

1. **浏览器端实测** — 还原真实用户体验
2. **引擎状态锁定** — 保证测量可重复
3. **统计验证内置** — 重复性 + 再现性双维度
4. **反向 GEO 输出** — 从测量延伸至内容治理建议

### 不公开部分

- 各引擎 Collector 具体配置
- 各引擎 Parser 选择器
- Analyst 风险话术分类的 prompt 模板
- 引用源域名权威性分级库
- 跨引擎一致性的具体计算公式
