# 天纪提示词 Skill

倪海厦天纪体系学习助手。基于天机道、人间道、地脉道框架做现代化转译，帮用户用传统术数思维分析命理和现实问题。

> **声明**：本项目为个人学习整理，不是倪海厦官方授权项目。所有分析仅供学习参考，不构成医疗、投资、婚姻等重大决策的唯一依据。

## 能力

| 功能 | 说明 |
|------|------|
| 八字分析 | 基础校盘与现实复盘、大运流年与阶段策略 |
| 紫微斗数 | 命盘结构化解读（需用户提供文墨天机命盘数据） |
| 易经三才 | 现实问题拆解（不需要术数数据，只需要一个具体问题） |
| 小六壬 | 日常小事快断（支持手动时间/当前时间两种模式） |

## 安装

### 从 GitHub 安装

```bash
# 使用 skill-installer
python3 ~/.codex/skills/.system/skill-installer/scripts/install-skill-from-github.py \
  --repo <GitHub用户名>/nihaixia-tianji-skill \
  --path skills/nihaixia-tianji
```

或使用 URL 形式：

```bash
python3 ~/.codex/skills/.system/skill-installer/scripts/install-skill-from-github.py \
  --url https://github.com/<GitHub用户名>/nihaixia-tianji-skill/tree/main/skills/nihaixia-tianji
```

安装后重启 Codex 以加载新 Skill。

### 手动安装

```bash
# 克隆仓库
git clone https://github.com/<GitHub用户名>/nihaixia-tianji-skill.git

# 复制到 skills 目录
cp -r nihaixia-tianji-skill/skills/nihaixia-tianji ~/.codex/skills/
```

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
