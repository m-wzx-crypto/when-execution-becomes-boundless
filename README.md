# 当执行趋于无限：人工智能时代的组织形态

**When Execution Becomes Boundless: Organizational Form in the Age of Artificial Intelligence**

> 组织是委托链，而委托链终止于不可让渡者。判断的微观制度、行动能力的产权安排与一种组织的设计。
>
> *The firm is a chain of delegation, and every chain of delegation must terminate in a subject that cannot be alienated.*

[![License: CC BY-NC-ND 4.0](https://img.shields.io/badge/License-CC%20BY--NC--ND%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-nd/4.0/)
[![Language](https://img.shields.io/badge/language-中文%20%7C%20English-blue.svg)](#contents)
[![Version](https://img.shields.io/badge/version-v1.0-brightgreen.svg)](#citation)

---

## 这是什么 / What this is

一份关于**人工智能时代组织形态**的研究论文，约 1.8 万字，附 17 项待检验命题与一次多智能体仿真实验的读数。

核心问题不是「AI 会不会取代管理者」，而是：**当执行能力趋于无限，组织还剩下什么可配置？** 本文的回答是判断——组织必须以判断权为配置对象，并使每一条自主行动链的末端系于一个可被指名的主体。

**英文全文已完成**：[`paper/en/full.md`](paper/en/full.md)（约 13,600 词，十节全译）。也可按节阅读，见目录。

A design-theory paper on **organizational form under agentic AI**: delegation chains, judgment rights, the inalienability of accountability, and the property arrangement of action capacity. Includes 17 testable propositions and one controlled multi-agent simulation. Chinese full text; English abstract available, English full text forthcoming.

**关键词 / Keywords:** 人工智能组织 · 组织形态 · 判断权 · 不可让渡性 · 责任锚定 · 委托链 · 行动能力 · 智能体治理 · 多智能体仿真 · 共生体组织

`AI organization` · `organization theory` · `agentic AI` · `AI governance` · `accountability` · `delegation chain` · `judgment rights` · `inalienability` · `organizational design` · `multi-agent simulation` · `human-in-the-loop` · `future of work` · `AI safety governance`

---

## 核心主张 / Core claims

论文给出五条设计原则，每条各自依赖一个前提，前提不成立时相应原则失效——这一点与主张同等篇幅。

| 原则 | Principle | 一句话 |
|---|---|---|
| R1 全息 | Holographic visibility | 判断须以看得见执行状态为条件；逐级压缩信息的层级因此失去存在理由 |
| R2 共生 | Symbiosis | 人与智能体互为条件；任何一方的净抽取都要被测量并校正 |
| R3 流变 | Fluidity | 结构随任务重算；稳定性落在规则层，而不是常设的岗位图谱上 |
| R4 锚定 | Anchoring | 无锚不行动；每一次自主行使都须落在某个具名主体的授权范围之内 |
| R5 再生 | Regeneration | 判断力是稀缺资源，须设预算、监测存量、建设回补机制 |

配套装置：三环两纵架构（意图 / 编排 / 执行 + 锚定通道 + 记忆层）、最小治理集（闸门、留痕、可保性核验、受方定价权）、在险部署，以及行动能力资产负债表。

---

## 实验读数 / What the simulation found

以多智能体仿真实现四种组织形态，同一任务集、同一模型版本、同一注入位置，每次只改一个变量：

- **产物层错误**：无闸门的形态全部漏放，有闸门的形态全部拦对。
- **意图层错误**：只审产物的形态全部穿透；仅把「允许节点回查简报」这一个权限打开，同一批错误全部被下游自行纠正——而那一格没有闸门。
- **一条设计时未写明的条件**：闸门既然不读真值，就必须看得见被判断的那一层，否则会把正确的纠正当成违规。

在线实验台（逐格公布判决，含不利结果）：<https://cmgl.top/research/live>

---

## 目录 / Contents

```
.
├── paper/
│   ├── zh/                                   # 中文全文
│   │   ├── when-execution-becomes-boundless.zh.md
│   │   ├── when-execution-becomes-boundless.zh.pdf
│   │   └── figures/                          # 图 1–6
│   └── en/
│       ├── full.md                           # 英文全文（合订，13,600 词）
│       ├── abstract.md                       # English abstract + keywords
│       ├── 00-glossary.md                    # 术语对照表
│       ├── 01-introduction.md                # I
│       ├── 02-theoretical-reflection.md      # II
│       ├── 03-microeconomics-of-judgment.md  # III
│       ├── 04-inalienability.md              # IV
│       ├── 05-property-in-action-capacity.md # V
│       ├── 06-symbiotic-organization-a/b/c.md # VI（三段）
│       ├── 07-evolution-and-limits.md        # VII
│       ├── 08-propositions.md                # VIII
│       ├── 09-a-tensions.md                  # IX.1–2
│       ├── 09-b-two-controlled-runs.md       # IX.3
│       └── 10-conclusion.md                  # X
├── CITATION.cff
├── LICENSE
└── README.md
```

论文结构：一、问题的重述 · 二、四种组织形态 · 三、判断的现货化 · 四、五条设计原则 · 五、行动能力的产权 · 六、制度化方案 · 七、极限形态：三人公司 · 八、检验与命题 · 九、张力、暗面与失效条件 · 十、结论

---

## Roadmap

- [x] 中文全文（v1.0，2026-10）
- [x] 英文标题、摘要、关键词
- [x] 英文术语表（`paper/en/00-glossary.md`）
- [x] 英文 §I 引言、§II 理论反思
- [x] 英文全文 §I–§X（约 13,600 词，`paper/en/full.md`）
- [ ] 实验数据与复现脚本（整理中）
- [ ] 引文与参考文献的 DOI 补全

---

## 引用 / Citation

```bibtex
@article{wang2026boundless,
  title   = {当执行趋于无限：人工智能时代的组织形态},
  author  = {Wang, Zexin},
  year    = {2026},
  version = {v1.0},
  url     = {https://github.com/m-wzx-crypto/when-execution-becomes-boundless},
  note    = {When Execution Becomes Boundless: Organizational Form in the Age of Artificial Intelligence}
}
```

GitHub 也提供 [CITATION.cff](CITATION.cff)，点击仓库右侧「Cite this repository」可直接导出 APA / BibTeX。

---

## 相关链接 / Related

- 官网全文：<https://cmgl.top/research/when-execution-becomes-boundless>
- 公开实验台：<https://cmgl.top/research/live>
- 作者：Wang Zexin（承明科技）· <m15635229542@163.com>

---

## 许可 / License

本文采用 [CC BY-NC-ND 4.0](https://creativecommons.org/licenses/by-nc-nd/4.0/) 许可：可自由转载与引用，须署名、不得商业使用、不得演绎修改。

This work is licensed under CC BY-NC-ND 4.0 — share and cite freely with attribution; no commercial use; no derivatives.

---

*版本 v1.0 · 2026-10 · 承明科技研究成果*
