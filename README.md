# 天纪学习助手 Skill（nihaixia-tianji）

面向倪海厦《天纪》体系的轻量 AI Skill，以**天机道、人间道、地脉道**为框架，提供八字、紫微斗数、易经三才与小六壬四类结构化学习与问题拆解提示词，支持 Claude Code、Codex、Cursor、Antigravity 等通用 Skills 客户端一键安装。

> **独立轻量入口说明**：本仓库只包含 `nihaixia-tianji` Skill 规则与参考提示词，适合希望快速单独安装 Skill 的用户。如果你希望完整浏览 **69 节点知识导图**、Obsidian 双链笔记、AI/RAG 语料包及《天纪》《人纪》阅读资料，欢迎前往主仓库 **[`zenoyang-ai/nihaixia-knowledge-graph`](https://github.com/zenoyang-ai/nihaixia-knowledge-graph)** 或直接访问在线站点 **[www.nihaixia-knowledge.xyz](https://www.nihaixia-knowledge.xyz/)**。

> **声明**：本项目为个人学习整理，非倪海厦官方授权项目。所有分析仅供学习交流与思路参考，不构成医疗、投资、婚姻等重大决策依据。

## 核心能力

| 模块 | 适用场景与说明 |
|------|------|
| **八字分析** | 基础校盘与现实复盘、大运流年与阶段策略 |
| **紫微斗数** | 命盘结构化解读（需用户提供文墨天机等排盘数据） |
| **易经三才** | 现实决策问题拆解（无需术数排盘，直接输入具体问题即可） |
| **小六壬** | 日常小事快断（支持手动指定时间或当前时间两种模式） |

## 快速安装

### 方式一：通用一键安装（推荐，支持 Claude Code / Codex / Cursor 等）

```bash
npx skills add zenoyang-ai/nihaixia-tianji-skill
```

也可直接从知识导图主仓库安装同一 Skill：

```bash
npx skills add zenoyang-ai/nihaixia-knowledge-graph --skill nihaixia-tianji
```

### 方式二：Codex 内置脚本安装

```bash
python3 ~/.codex/skills/.system/skill-installer/scripts/install-skill-from-github.py \
  --repo zenoyang-ai/nihaixia-tianji-skill \
  --path skills/nihaixia-tianji
```

安装完成后开启新对话即可触发使用。本项目仅安装规则与提示词，不会下载完整知识库文件。

## 使用示例

```text
用倪海厦天纪帮我看一下这个八字
我有紫微命盘，帮我做结构化分析
用易经三才帮我拆一下要不要换工作
按现在时间用小六壬看一下今天去谈合作顺不顺
```

## 配套在线站点与主仓库

- **在线知识导图与 AI 问答主站**：[www.nihaixia-knowledge.xyz](https://www.nihaixia-knowledge.xyz/)（海外镜像：[GitHub Pages](https://zenoyang-ai.github.io/nihaixia-knowledge-graph/)）
- **开源主仓库（100+ Stars，含 69 节点图谱与双链库）**：[`zenoyang-ai/nihaixia-knowledge-graph`](https://github.com/zenoyang-ai/nihaixia-knowledge-graph)

## 目录结构

```text
nihaixia-tianji-skill/
├── README.md                           # 本文件
├── LICENSE                             # MIT License
└── skills/
    └── nihaixia-tianji/
        ├── SKILL.md                    # 触发条件、路由选择与执行流程
        ├── agents/
        │   └── openai.yaml             # Agent 元数据
        └── references/
            ├── prompts.md              # 核心提示词模板
            └── xiaoliuren.md           # 小六壬算法与速查表
```

## 内置提示词清单

| 提示词 | 适用场景 |
|--------|----------|
| 八字基础校盘与现实复盘 | 已有八字排盘，查看整体格局、喜用神与过往验证 |
| 八字大运流年与阶段策略 | 已确认格局，梳理阶段节奏与现实应对方向 |
| 紫微斗数命盘结构化解读 | 已有紫微命盘，按宫位星曜、流年人际与职场细节解读 |
| 易经三才现实问题拆解 | 面临具体困惑，用阴阳三才时位框架梳理取舍 |
| 小六壬日常决策 | 日常出行、约见、办事等轻量场景参考 |

## 安全边界

- 不代为排盘，八字、命盘与起课数据须由用户提供
- 不做绝对化断言，结论统一作为倾向与思路参考
- 不构成医疗、投资、婚姻等重大决策的唯一依据

## License

MIT License
