# meme-skills

- 中文互联网文化微型知识库，以[现行agent skill开放标准`agentskills.io`](https://agentskills.io/)格式维护。覆盖**热梗知识**「`meme-{xx}`」与**游戏知识**「`game-{xx}`」两大领域。每个 skill 可供 AI agent 在对话中按需加载，获取精确的文化语境知识。
- 这个项目追求模块化、轻量化，并非百科式的详尽，而是为AI提供一套模块化的文化速查，类似《十万个为什么》。有时你与助手对上电波，不需要长篇大论的理解对齐，仅需会心一笑，你懂ta，ta也懂你。

## 为什么

LLM 的训练数据永远滞后于中文互联网的造梗速度与游戏发布节奏。当用户说"豪意值拉满"，AI 却一本正经地拆字释义——~~这很准确~~（这准确嘛w），但也很扫兴。
当用户兴奋地聊起《杀戮尖塔2》的新角色，AI 只能回答"截至2025年5月我无法确认该信息"——未免有些让人失望。

一个真正称职的个人 AI 助手，不该只是个工具。它应该懂你的梗，接得住你的玩笑；了解你玩的游戏，能聊到一起。你说「你已急哭」，它能回「✋👽✋」。
你讨论尖塔2的~~第四层~~（有第四层吗¿）机制，它能接得住话。

本项目将热梗与游戏知识以现行agent skill格式组织分发，让任何 AI agent 按需加载，跟上文化的版本，不做局外人。

### 主流国产 LLM 的训练数据截止日期

以下数据来自 [models.dev](https://models.dev) 及各模型官方文档（截至 2026 年 5 月）：

| 模型 | 训练数据截止 | 发布时间 | 知识滞后 |
|---|---|---|---|
| DeepSeek V4 Flash / Pro | 2025-05 | 2026-04 | ~11 个月 |
| Kimi K2.6 | 2025-04 | 2026-04 | ~12 个月 |
| GLM 5.1 | 2025-04 | 2026-04 | ~12 个月 |
| MiniMax M2.7 | 2025-01 | 2026-03 | ~14 个月 |
| Qwen 3.6 Plus | 2025-04 | 2026-04 | ~12 个月 |
| MiMo V2.5 Pro | 2024-12 | 2026-04 | ~16 个月 |

即使是 2026 年 3-4 月发布的最新模型，训练数据也停留在 2024 年底至 2025 年初。而互联网热梗的生命周期往往只有几周到几个月——这意味着**任何 LLM 都天然无法覆盖发布时已存在的梗，更不用说发布后的新梗**。Skill 机制正是为填补这个结构性缺口而设计。

## 部分已收录

### 热梗

| Skill | 梗名 | 分类 | 触发关键词 |
|---|---|---|---|
| [meme-jiahao](./skills/meme-jiahao/SKILL.md) | 嘉豪 | 网络流行词 | 嘉豪、嘉欣、豪意值 |
| [meme-niyijiku](./skills/meme-niyijiku/SKILL.md) | 你已急哭 | 表情包迷因 | 你已急哭、外星人表情包、急了 |
| [meme-wodedaodun](./skills/meme-wodedaodun/SKILL.md) | 我的刀盾 | 空耳梗 | 我的刀盾、刀盾狗、What the dog doing |
| [meme-bibilabu](./skills/meme-bibilabu/SKILL.md) | 比比拉布 | 无意义音效梗 | 比比拉布、bibilabu、Howieazy |
| [meme-nailong](./skills/meme-nailong/SKILL.md) | 奶龙/大笑奶龙 | AI生成抽象梗 | 奶龙、大笑奶龙、奶龙捧腹大笑、变异奶龙 |
| [meme-suanbird](./skills/meme-suanbird/SKILL.md) | 蒜鸟 | 方言谐音梗 | 蒜鸟、蒜鸟蒜鸟、武汉和平鸟、都不容易 |
| [meme-jichu](./skills/meme-jichu/SKILL.md) | xx基础xx就不基础 | 万能句式梗 | 基础款、显贵公式、基础不基础 |
| [meme-bababoyi](./skills/meme-bababoyi/SKILL.md) | 巴巴博一/巴巴博弈 | 空耳梗 | 巴巴博一、巴巴博弈、bababooey、bababoy |
| [meme-yuzhoulengmo](./skills/meme-yuzhoulengmo/SKILL.md) | 宇宙冷漠 | 口癖/模仿梗 | 宇宙冷漠、农神、宇！宙！冷！漠！、人类最大的恐惧 |
| [meme-diaochabingtuan](./skills/meme-diaochabingtuan/SKILL.md) | 公厕调查兵团 | 网络迷因 | 调查兵团、公厕调查兵团、献出膀胱、cityshit、厕所先烈 |

### 游戏

| Skill | 游戏名 | 分类 | 触发关键词 |
|---|---|---|---|
| [game-slay-the-spire-2](./skills/game-slay-the-spire-2/SKILL.md) | 杀戮尖塔2 | 肉鸽卡牌 | 杀戮尖塔2、Slay the Spire 2、STS2、尖塔2、爬塔2 |

## 目录说明

| 目录 | 用途 |
|---|---|
| [skills/](./skills/) | 正式收录的梗 skill、游戏 skill 和元工具，按规范编写 |
| [`incoming/`](./incoming/) | 待处理的投稿，暂时不适宜移入`skills/`，需要处理后移入 |
| [`archive/`](./archive/) | 已过时或不再维护的 skill 封存 |

## 安装

将 skill 目录复制到 agent 的 skills 目录：

```bash
# OpenCode / OpenClaw
cp -r skills/meme-* ~/.agents/skills/
cp -r skills/game-* ~/.agents/skills/
```

> 将在日后登录skills.sh和clawhub等平台。

## 使用建议

### 按需加载，不必全开

每个 skill 安装后，其 `name`、`description` 和 `location` 会被注入 LLM 上下文，作为 agent 框架判断是否加载 skill body 的依据（每个 skill 描述块约 200-400 字符）。这部分元数据虽然轻量，但积少成多：

| 已启用 skill 数量 | 约消耗上下文 | 对 200K 窗口 | 对 1M 窗口 |
|---|---|---|---|
| ~10 个 | ~2-4k | ~1-2%，几乎无感 | <0.5%，无感 |
| ~20 个 | ~4-8k | ~2-4%，轻微 | <1%，无感 |
| ~50 个 | ~10-20k | ~5-10%，有感知 | ~1-2%，几乎无感 |
| ~100 个 | ~20-40k | ~10-20%，需要取舍 | ~2-4%，轻微 |

当前本仓库收录 7 个梗 skill 和 1 个游戏 skill，按这个节奏扩到 50 个也在可控范围。如果你同时安装了其他大量 skill（前端、后端、运维、设计等），推荐使用 **OpenClaw 前端的 Skills 管理界面**或类似工具的开关面板，根据当下场景按需启用，而非一股脑全开。

以 **DeepSeek V4** 系列为代表的 1M 上下文次世代 LLM 基本不受影响——100 个 skill 的元数据在其窗口里只占约 2%。

## 贡献

参见 [AGENTS.md](./AGENTS.md) 了解 skill 格式和添加新梗/游戏的流程。

推荐使用内置的 **[梗技能创建器](./skills/meme-skill-creator/SKILL.md)** —— 一个元 skill，可在对话中自动完成梗研究、交叉验证、按模板编写和索引更新的全流程。游戏 skill 由人工编写把关。

## 协议

[MIT](./LICENSE)

虽然本项目本质是中文互联网迷因知识库（文档/数据集合），但 agent skill 作为 AI 运行时可加载的资源，更接近「可执行知识」，故采用 MIT 许可证以最大化 GitHub 生态兼容性。效果等价于 CC0 的「自由使用」精神，仅增加保留原作者署名条款。
