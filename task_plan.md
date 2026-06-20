# Task Plan: feiman-translation — 《物理定律的本性》中译

## Goal
将 Richard Feynman 的《The Character of Physical Law》(1965, 2017 MIT Press 再版) 全书翻译为结构化的中文 Markdown，通过 GitHub Pages (Jekyll + MathJax) 发布。

## Book Structure
| 章节 | 原标题 | 中文标题 | 预估页数 |
|------|--------|----------|----------|
| Foreword | Foreword by Frank Wilczek + BBC Producer | 前言 (Wilczek + Sleath) | 1-11 |
| Ch1 | The Law of Gravitation | 引力定律——物理定律的一个例子 | 13-34 |
| Ch2 | The Relation of Mathematics to Physics | 数学与物理学的关系 | 35-58 |
| Ch3 | The Great Conservation Principles | 伟大的守恒原理 | 59-83 |
| Ch4 | Symmetry in Physical Law | 物理定律中的对称性 | 84-107 |
| Ch5 | The Distinction of Past and Future | 过去与未来的区分 | 108-126 |
| Ch6 | Probability and Uncertainty — Quantum Mechanical View | 概率与不确定性——量子力学的自然观 | 127-148 |
| Ch7 | Seeking New Laws | 寻找新定律 | 149-173 |

## Current Phase
Phase 1 — 素材采集与分章

## Phases

### Phase 1: 素材采集与分章 (Ingest)
- [x] PDF 文本提取 (pdftotext, ClearScan OCR)
- [ ] 按章节拆分原文到 raw/chXX_*.txt
- [ ] 建立术语表 glossary.md 初稿
- **Status:** in_progress

### Phase 2: 深度研究与并行翻译 (Research + Translate)
- [ ] Mythos 研究每章物理概念 (7 chapters × mythos research)
- [ ] Paper Agent 并行翻译每章 (batch of 3-4 agents)
- [ ] 每章输出到 docs/chXX_中文标题.md
- **Status:** pending

### Phase 3: 一致性与数学公式 QA (Quality)
- [ ] 术语一致性检查 (vs glossary.md)
- [ ] kramdown 数学公式验证 (verify_math_kramdown.rb)
- [ ] promote_inline_math + fix_math_pipes
- **Status:** pending

### Phase 4: 组装与发布 (Assemble & Publish)
- [ ] 生成 docs/index.md, docs/_sidebar.md
- [ ] 配置 _config.yml, head-custom.html (MathJax 3)
- [ ] GitHub Pages 推送
- [ ] 浏览器端公式验证
- **Status:** pending

## Decisions Made
| Decision | Rationale |
|----------|-----------|
| 输出格式适配为物理讲座风格 | 此书非 CS 课程，无代码/论文精读，需调整为费曼物理讲座风格 |
| 保留原章节顺序和标题 | 费曼的讲座结构本身就是精心设计的叙事弧线 |
| 数学公式全部用 $$...$$ | kramdown 兼容性要求，避免 GitHub Pages 渲染错误 |

## Output Template (per chapter, adapted for physics lectures)
```markdown
# 第N章: 中文标题
> 原书: The Character of Physical Law, Richard Feynman, 1965
> 本章基于 Messenger Lecture N

## 一、本章概要
- 核心问题与动机
- 与前后章节的逻辑关系

## 二、核心概念与物理论证
- 关键定义 (中英对照)
- 完整数学推导 ($$...$$ 格式)
- 物理直觉与费曼式解释

## 三、费曼的关键洞察 (Feynman's Insights)
- 3-5 个核心洞察
- 与后续物理学发展的关联 (Wilczek 评注)

## 四、延伸思考 (Further Reflections)
- 开放问题与研究方向
- 推荐延伸阅读
```
