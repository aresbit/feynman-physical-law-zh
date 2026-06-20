# 物理定律的本性 (The Character of Physical Law)

> **Richard Feynman 著** | 1964 年 Messenger Lectures, Cornell University
> 1965 年出版, 2017 年 MIT Press 再版 (Frank Wilczek 新序)
>
> 中译版 — 完整 7 章 + Wilczek 前言

---

## 关于本书

1964 年 11 月，理查德·费曼在康奈尔大学发表了七场 Messenger 讲座。这些讲座被整理成《The Character of Physical Law》，成为 20 世纪最经典的科学著作之一。

费曼从引力定律出发，逐章讨论了数学与物理学的关系、守恒原理、对称性、时间之箭、量子力学的不确定性，以及发现新定律的方法论。全书以口语化的演讲风格写成，充满了费曼标志性的智慧、幽默和深刻的物理洞察。

2017 年 MIT Press 再版时，诺贝尔奖得主 **Frank Wilczek** 撰写了新前言，为原始讲座提供了半个世纪以来的关键科学更新：量子色动力学 (QCD)、渐近自由、引力熵与大爆炸宇宙学等。

## 目录

| 章节 | 中文标题 | 英文原题 |
|------|----------|----------|
| — | [前言与导言](docs/ch00_前言与导言) | Foreword by Wilczek, Sleath & Corson |
| 1 | [引力定律——物理定律的一个例子](docs/ch01_引力定律——物理定律的一个例子) | The Law of Gravitation |
| 2 | [数学与物理学的关系](docs/ch02_数学与物理学的关系) | The Relation of Mathematics to Physics |
| 3 | [伟大的守恒原理](docs/ch03_伟大的守恒原理) | The Great Conservation Principles |
| 4 | [物理定律中的对称性](docs/ch04_物理定律中的对称性) | Symmetry in Physical Law |
| 5 | [过去与未来的区分](docs/ch05_过去与未来的区分) | The Distinction of Past and Future |
| 6 | [概率与不确定性——量子力学的自然观](docs/ch06_概率与不确定性——量子力学的自然观) | Probability and Uncertainty — the Quantum Mechanical View |
| 7 | [寻找新定律](docs/ch07_寻找新定律) | Seeking New Laws |

## 在线阅读

本站通过 GitHub Pages 发布，数学公式使用 MathJax 3 渲染。

访问: **https://aresbit.github.io/feynman-physical-law-zh/**

## 翻译说明

- **风格**: 忠实保留费曼的口语化、诙谐的演讲风格
- **术语**: 首次出现标注 `中文 (English)`，全书术语统一见 [术语表](docs/glossary.md)
- **数学**: `$$...$$` 格式，兼容 GitHub Pages (kramdown + MathJax 3)
- **更新**: 结合 Wilczek (2017) 新前言的关键科学更新

## 本地构建

```bash
# 安装 Jekyll
gem install bundler jekyll
cd docs
bundle init && bundle add jekyll github-pages

# 本地预览
bundle exec jekyll serve
```

数学公式在本地预览时可能需额外配置 MathJax，推送到 GitHub Pages 后会自动渲染。

## 致谢

- Richard Feynman — 永恒的好奇心和"套在可怕紧身衣里的想象力"
- Frank Wilczek — 2017 年前言提供了宝贵的科学更新
- MIT Press — 版权方，请支持正版

> "我们所需的是想象力，但必须是套在可怕紧身衣里的想象力。"
> — Richard Feynman

## License

中文翻译采用 [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/) 许可。

原著版权归 MIT Press 所有。请购买正版支持。
