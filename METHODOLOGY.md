# 8-Dimension Scorecard · Methodology

> Conceptual framework for evaluating brand AI search visibility.
> Specific formulas, weights, and thresholds are proprietary and not disclosed.
>
> 8 维评分卡概念框架。具体公式、权重、阈值为专有方法学，不在本仓库公开。

---

## Design Principles

1. **Internationally aligned, locally adapted** — 5 dimensions track established methodology (Profound, AthenaHQ); 3 extensions address gaps unique to multi-engine and Chinese-language environments.
2. **Browser-side measurement** — All dimensions are computed from real-user-equivalent browser-side answer collection, not static API endpoints.
3. **Statistical validity** — Each measurement is subject to repeatability and reproducibility verification.

## Five Internationally-Aligned Dimensions

### 1. Brand Answer Share

Frequency at which the target brand appears in the answer corpus for category-relevant queries.

- Inputs: query set × engine matrix
- Output: per-query and aggregated share

### 2. Recommendation Rate

Frequency at which the AI engine actively recommends the brand (vs. passively mentioning it).

- Distinguishes between mention and recommendation
- Includes intent signals (e.g., "you should consider...", "the best option is...")

### 3. Substitution Rate

Frequency at which the AI engine recommends a competitor when the target brand is the natural answer.

- Identifies traffic diversion patterns
- Includes near-miss substitutions (e.g., wrong sub-brand)

### 4. Semantic Position

Position of brand mention within the answer (head / mid / tail).

- Head: first 25% of answer length
- Mid: 25%-75%
- Tail: last 25%

### 5. Citation Source Structure

Distribution of citation sources backing the brand-related content in answers.

- Source type classification (official / media / community / aggregator)
- Domain authority tier

## Three Unique Extensions

### 6. Cross-Engine Consistency Index

Measures how stable the answer to the same query is across multiple AI engines.

- Higher consistency = more trustworthy / robust brand positioning
- Lower consistency = brand position is engine-dependent and fragile

### 7. Citation Source Weighting Model

Weighted scoring that combines source domain authority and informational gain value.

- Not all citations are equal
- Self-referential and SEO-noise sources are deweighted

### 8. Risk Discourse Classification

Two-dimensional classification of risk content found in answers:

- **Falsifiability dimension**: how easy is the false claim to verify and refute
- **Commercial impact dimension**: how much does the false claim damage purchase intent

Combined into a tiered alert system.

## Statistical Validity Framework

Two-dimensional statistical verification:

- **Repeatability**: variance control via N repeated samples per query, same engine, same time window
- **Reproducibility**: cross-engine and cross-brand consistency verification

Aligns with established academic standards for measurement reliability.

## What Is Proprietary

The following are **not** disclosed in this repository:

- Specific weight coefficients within each dimension
- Threshold values for risk classification tiers
- Per-engine prompt rotation and locking patterns
- Citation domain authority tier definitions
- The exact computation of the Cross-Engine Consistency Index

For evaluation purposes, please contact directly.

---

## 中文

### 设计原则

1. **国际对齐 + 本土适配** — 5 维对齐 Profound / AthenaHQ 国际方法学；3 维独有扩展填补多引擎与中文环境的方法学空白
2. **浏览器端实测** — 所有维度均通过浏览器端答案采集计算，非 API 静态端点
3. **统计有效性** — 每个测量都需重复性与再现性验证

### 5 维国际对齐

**1. 品牌出现率（Answer Share）** — 目标品牌在该品类相关问题答案中出现的频次

**2. 主动推荐率（Recommendation Rate）** — AI 引擎主动推荐品牌的频次（区别于被动提及）

**3. 竞品替代率（Substitution Rate）** — 当目标品牌应为自然答案时，AI 转而推荐竞品的频次

**4. 语义位置（Semantic Position）** — 品牌在答案中的位置（头 / 中 / 尾）

**5. 引用源结构（Citation Source Structure）** — 答案中支撑品牌相关内容的引用源分布

### 3 维独有扩展

**6. 跨引擎一致性指数** — 同一问题在多个 AI 引擎间答案的稳定程度

**7. 引用源权重模型** — 综合域名权威性与信息增益价值的加权评分

**8. 错误话术风险分级** — 按可证伪程度与商业影响双维度分级告警

### 不公开的部分

- 各维度内的具体权重系数
- 风险分级的阈值数值
- 各引擎的 prompt 轮换与锁定模式
- 引用源域名权威性分级定义
- 跨引擎一致性指数的具体计算

如需评估，请联系 will@will-luck.com
