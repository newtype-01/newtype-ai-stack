# newtype AI Stack

`newtype-ai-stack` 是一个 Codex Skill,用于基于 **newtype AI Stack 方法论**分析 AI 产业链投资问题。

它把公司、ticker、技术、产业新闻、瓶颈迁移和组合配置问题,翻译成结构化研究判断:

- 一个资产位于 AI 产业链哪一层
- 一条 AI 产业新闻谁受益、谁受损、如何验证
- 当前瓶颈在哪里,下一阶段稀缺性会迁移到哪里
- 一家公司是过渡期赢家还是终局赢家
- 如何把候选公司分成 Core 7 / N-Stack 20 / Watch List 50

> 本 Skill 只提供研究分析框架,不构成个性化投资建议。

## 安装

把仓库安装到本地 Codex skills 目录:

```bash
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills"
git clone https://github.com/newtype-01/newtype-ai-stack.git \
  "${CODEX_HOME:-$HOME/.codex}/skills/newtype-ai-stack"
```

安装后重启 Codex。

调用方式:

```text
$newtype-ai-stack
```

## 能做什么

这个 Skill 使用轻量 `SKILL.md` 作为总入口,根据用户问题按需读取 `references/` 里的方法包,避免一次性加载全部上下文。

| 用户意图 | 方法包 |
| --- | --- |
| 判断公司、ticker、产品、技术或概念在 AI 产业链哪一层 | `references/stack-mapping.md` |
| 把 AI 新闻翻译成受益者、受损者和验证信号 | `references/stack-news.md` |
| 追踪当前和未来的稀缺性瓶颈 | `references/scarcity-trace.md` |
| 判断过渡期赢家 vs 终局赢家 | `references/bridge-vs-endgame.md` |
| 构建 Core 7 / N-Stack 20 / Watch List 50 分仓框架 | `references/position-sizing.md` |
| 共享七层定义、稀缺性等级和合规边界 | `references/shared-framework.md` |

## newtype AI Stack 七层产业地图

```text
第7层  应用层 Apps
第6层  模型层 Models
第5层  算力服务层 Cloud / IaaS
第4层  算力硬件层 Compute Hardware
第3层  互联与存储层 Interconnect & Memory
第2层  基础设施层 Infrastructure
第1层  能源层 Energy
```

核心判断是:长期、可验证的投资稀缺性往往不在应用层,而更容易集中在第1-4层,也就是能源、基础设施、互联与存储、算力硬件。

## 示例 Prompt

```text
$newtype-ai-stack 分析一下 VRT 在 AI 产业链的位置
```

```text
$newtype-ai-stack HBM 不再短缺后,下一个瓶颈是什么?
```

```text
$newtype-ai-stack NVDA 是过渡期赢家还是终局赢家?
```

```text
$newtype-ai-stack 给 NVDA, TSM, ASML, MU, VRT, CEG, AVGO 做一个 Core / N-Stack / Watch List 分仓
```

## 仓库结构

```text
.
├── SKILL.md
├── agents/
│   └── openai.yaml
├── references/
│   ├── shared-framework.md
│   ├── stack-mapping.md
│   ├── stack-news.md
│   ├── scarcity-trace.md
│   ├── bridge-vs-endgame.md
│   └── position-sizing.md
├── README.md
├── README.zh.md
└── LICENSE
```

## 免责声明

本 Skill 的所有输出均为基于 newtype AI Stack 方法论的研究分析判断,不构成个性化投资建议、财务建议,也不构成任何证券的买入或卖出建议。

用户应自行验证所有实时数据,包括股价、市值、估值倍数、财报、订单、产能、市场份额、监管状态和管理层指引。具体投资决策应结合个人风险承受能力、资金属性、税务状况,并在必要时咨询合格投资顾问。

## License

MIT
