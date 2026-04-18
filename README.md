# bazi-skills

八字命理解读相关的 Claude Skill 集合。

## 简介

本仓库蒸馏整理传统八字命理知识，封装为可供 Claude 调用的 Skill，用于**基于已给定四柱八字**的五行分析、十神结构解读、神煞判读、宫位分析、大运流年引动等命理解读任务。

> **职责边界**：本 Skill 只做**解读**，不做**排盘**。四柱干支需由用户或外部排盘工具提供。

## 使用方式

将本仓库放置于 Claude Code 可识别的 skills 目录下，Claude 会在相关提问时自动加载 SKILL.md 并按需读取 `core/` 下的知识库文件。

## 目录结构

```
bazi-skills/
├── README.md             # 本文件
├── LICENSE.datasource    # 知识内容许可证（CC BY-NC-SA 4.0，适用 core/ 与 SKILL.md 论理部分）
├── LICENSE.repo          # 仓库工程文件许可证（MIT，适用结构/封装/文档）
├── DISCLAIMER.md         # 免责声明
├── ATTRIBUTION.md        # 来源与致谢
├── SKILL.md              # 八字解读主 Skill（引用 core/ 知识库）
└── core/                 # 知识库（按命理维度组织）
    ├── 十神/              # 比肩、劫财、伤官、印星、偏印、财星、食伤…
    ├── 天干/              # 丁火、己土…
    ├── 地支/              # 伏吟、穿…
    ├── 宫位/              # 夫妻宫…
    ├── 神煞/              # 桃花、华盖、羊刃、驿马、天罗地网…
    ├── 六亲/              # （待补充）
    ├── 大运流年/           # （待补充）
    ├── 婚姻/              # （待补充）
    └── 现实议题/           # （待补充）
```

`core/` 下每个 md 文件对应一个命理概念，是 Skill 做解读时的唯一论理依据。

## 重要文件

使用本仓库**前**，请务必先阅读以下三个文件：

| 文件 | 说明 |
|---|---|
| [`LICENSE.datasource`](./LICENSE.datasource) | **知识内容**许可证。适用 `core/` 全部 md 与 SKILL.md 论理部分。采用 **CC BY-NC-SA 4.0**（署名—非商业—相同方式共享）。 |
| [`LICENSE.repo`](./LICENSE.repo) | **仓库工程文件**许可证。适用目录结构、封装格式、README 等非命理文本。采用 **MIT**。 |
| [`DISCLAIMER.md`](./DISCLAIMER.md) | 免责声明。明确使用限制、禁止用途、使用者责任。**命理内容不是科学、不是医疗、不是决策工具**。 |
| [`ATTRIBUTION.md`](./ATTRIBUTION.md) | 来源与致谢。详细说明原始知识来源与正确的署名方式。 |

> **两份 LICENSE 同时生效**，就各自适用范围独立约束。若您的衍生作品包含 `core/` 内容，即使您只打算用 MIT 部分的封装结构，也必须同时遵守 `LICENSE.datasource` 的 CC BY-NC-SA 4.0 条款。

## 来源（速览）

本仓库知识体系蒸馏自：

**玄墨师傅** — Bilibili UID [3546748700068225](https://space.bilibili.com/3546748700068225)

详细来源说明与署名要求见 [`ATTRIBUTION.md`](./ATTRIBUTION.md)。

## 许可（速览）

- **知识内容（`core/` + SKILL.md 论理部分）**：CC BY-NC-SA 4.0 — 见 [`LICENSE.datasource`](./LICENSE.datasource)
- **工程文件（README、结构、封装格式等）**：MIT — 见 [`LICENSE.repo`](./LICENSE.repo)

## 免责（速览）

命理内容仅供文化学习与自我反思参考，**不构成任何形式的医疗、法律、金融、人生决策建议**。请理性看待。完整声明见 [`DISCLAIMER.md`](./DISCLAIMER.md)。

---

**一句话**：传统文化学习笔记，署名+非商业用，想清楚了再用。
