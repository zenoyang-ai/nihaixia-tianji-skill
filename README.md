# 天纪提示词工具

> **项目已整合至主仓库（推荐前往主仓获取最新维护与开源知识库）**：
> 本 Skill 现已并入主仓库 **[`zenoyang-ai/nihaixia-knowledge-graph`](https://github.com/zenoyang-ai/nihaixia-knowledge-graph/tree/main/skills/nihaixia-tianji)**，并与 64 节点知识图谱、Obsidian 双链库、AI/RAG 语料包及《天纪》《人纪》开源阅读资料统一维护。
> 推荐使用最新一行安装命令：
> ```bash
> npx skills add zenoyang-ai/nihaixia-knowledge-graph --skill nihaixia-tianji
> ```

这是一个可安装的提示词工具。它以天机道、人间道、地脉道为主要框架，帮助用户用传统术数的思路梳理命理和现实问题。

> **声明**：本项目为个人学习整理，不是倪海厦官方授权项目。所有分析仅供学习参考，不构成医疗、投资、婚姻等重大决策的唯一依据。

## 配套网站

如果你想先浏览知识图谱、学习路径和提示词示例，可以访问国内主站：[倪海厦知识图谱（www.nihaixia-knowledge.xyz）](https://www.nihaixia-knowledge.xyz/)（海外备份：[GitHub Pages](https://zenoyang-ai.github.io/nihaixia-knowledge-graph/)），或直接前往整合后的 [GitHub 主仓库](https://github.com/zenoyang-ai/nihaixia-knowledge-graph)。

本仓库仅作旧安装命令的历史兼容保留，后续更新与维护均在主仓库 [`skills/nihaixia-tianji/`](https://github.com/zenoyang-ai/nihaixia-knowledge-graph/tree/main/skills/nihaixia-tianji) 进行。

## 可以做什么

| 功能 | 说明 |
|------|------|
| 八字分析 | 基础校盘与现实复盘、大运流年与阶段策略 |
| 紫微斗数 | 命盘结构化解读（需用户提供文墨天机命盘数据） |
| 易经三才 | 现实问题拆解（不需要术数数据，只需要一个具体问题） |
| 小六壬 | 日常小事快断（支持手动时间/当前时间两种模式） |

## 安装

在终端运行下面这一条命令：

```bash
python3 ~/.codex/skills/.system/skill-installer/scripts/install-skill-from-github.py \
  --repo zenoyang-ai/nihaixia-tianji-skill \
  --path skills/nihaixia-tianji
```

安装完成后重启 Codex，让它加载这个工具。本项目只安装提示词和参考规则，不会下载完整的知识图谱或个人资料。

## 使用示例

```
用倪海厦天纪帮我看一下这个八字
我有紫微命盘，帮我结构化分析
用易经三才帮我拆一下要不要换工作
按现在时间用小六壬看一下今天去谈合作顺不顺
```

## 目录结构

```
nihaixia-tianji-skill/
├── README.md                           # 本文件
├── LICENSE                              # MIT License
└── skills/
    └── nihaixia-tianji/
        ├── SKILL.md                     # 触发条件、路由选择、执行流程
        ├── agents/
        │   └── openai.yaml              # Agent 元数据
        └── references/
            ├── prompts.md               # 4 个完整提示词
            └── xiaoliuren.md            # 小六壬算法与速查表
```

## 提示词列表

| 提示词 | 场景 |
|--------|------|
| 八字基础校盘与现实复盘 | 有八字数据，看整体格局、喜用神、过去经历验证 |
| 八字大运流年与阶段策略 | 已确认格局，看财运事业婚姻健康趋势和未来十年 |
| 紫微斗数命盘结构化解读 | 有紫微命盘，看宫位星曜、流年人际、职场细节 |
| 易经三才现实问题拆解 | 有具体困惑，用阴阳三才时位框架分析 |
| 小六壬日常决策 | 日常小事快速参考（出行/约见/办事/交易） |

## 安全边界

- 不自行排盘，八字/命盘/起课数据必须由用户提供
- 不做绝对化断言，所有结论为"参考分析/倾向/可能性"
- 不构成医疗、投资、婚姻等重大决策的唯一依据
- 仅供学习参考

## License

MIT
