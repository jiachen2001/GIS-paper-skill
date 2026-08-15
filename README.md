# GIS-paper-skill

面向 GIS、空间科学与空间实证研究的方法学审查 Skill。它的目标不是机械推荐更多模型，而是检查研究问题、空间定义、数据生成机制、样本形成、统计建模、程序实现和结论解释是否真正一致。

## 适合处理的任务

- GIS / 空间实证研究设计与方法审查
- 距离、缓冲区、可达性、路径、暴露与网络分析
- POI、遥感、轨迹、路网、行政区等多源空间数据融合
- 空间连接、地理编码、匹配、去重、加权与聚合审查
- 小样本、高维 embedding、传统机器学习与空间机器学习
- 空间交叉验证、分组验证、时空验证与数据泄漏检查
- GeoPandas / GIS 数据处理代码与可复现性审查
- 稳健性、敏感性、论文方法、结果、局限和结论边界

## 不适合把它当成什么

它不是通用论文代写器，也不默认某一种 GIS 方法、空间模型或机器学习算法永远更优。具体方法必须由研究机制、数据结构、空间尺度、样本量和推断目标决定。

## 核心原则

1. 研究问题、理论构念、变量操作化、数据生成机制和分析方法一致。
2. 估计对象、空间尺度、样本形成和推断边界明确。
3. 程序实现忠实于方法定义，不因计算便利静默改变研究对象。
4. 模型复杂度与有效样本量、特征维度、依赖结构和验证方式匹配。
5. 结论强度不超过证据强度。

## 仓库结构

```text
GIS-paper-skill/
├── SKILL.md
├── README.md
├── agents/
│   └── openai.yaml
├── references/
│   ├── review-checklists.md
│   ├── research-design.md
│   ├── spatial-analysis.md
│   ├── data-quality-and-matching.md
│   ├── statistical-modeling.md
│   ├── small-sample-modeling.md
│   ├── spatial-ml-validation.md
│   ├── code-and-reproducibility.md
│   ├── robustness-and-sensitivity.md
│   └── reporting-and-interpretation.md
└── examples/
    ├── accessibility-study.md
    ├── small-sample-ml-study.md
    └── code-review-example.md
```

## 典型调用

### 1. 审查空间可达性设计

> 使用 $gis-spatial-research-methodology 审查我的公共服务设施可达性研究。重点判断直线距离、网络距离、缓冲区和空间尺度是否与研究问题一致。

### 2. 小样本机器学习

> 我只有 120 个样本，同时有人工变量和 DINO/LLM embedding。使用 $gis-spatial-research-methodology 帮我判断模型复杂度、交叉验证、降维和数据泄漏风险，并优先给出适合当前样本规模的方案。

### 3. 审查 GIS 数据处理代码

> 使用 $gis-spatial-research-methodology 检查这段 GeoPandas spatial join 和 groupby 代码是否改变了样本量、重复计数或空间含义，并指出需要增加的数量审计。

## 输出风格

Skill 默认先给总体判断，再按“关键 / 重要 / 一般”标注问题，并说明：

- 证据在哪里；
- 问题为什么成立；
- 可能如何影响结果；
- 最小可行修改是什么；
- 是否需要敏感性或替代设定验证；
- 当前证据能支持到什么结论。

没有足够信息时明确写“无法判断”，不补造研究设定。
