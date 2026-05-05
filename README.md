# meme-skills

中文互联网迷因（meme）知识库，以 open agent skill 格式维护。每个 skill 可供 AI agent 在对话中按需加载，获取精确的文化语境知识。

## 为什么

LLM 的训练数据永远滞后于中文互联网的造梗速度。当用户说"豪意值拉满"，AI 却一本正经地拆字释义——这很准确，但也很扫兴。

一个真正称职的个人 AI 助手，不该只是个工具。它应该懂你的梗，接得住你的玩笑。你说"你已急哭"，它能回:"那你别急。"

本项目将热梗知识以 open agent skill 格式组织分发，让任何 AI agent 按需加载，跟上梗的版本，不做局外人。

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

## 已收录梗

| Skill | 梗名 | 分类 | 触发关键词 |
|---|---|---|---|
| [meme-jiahao](./meme-jiahao/SKILL.md) | 嘉豪 | 网络流行词 | 嘉豪、嘉欣、豪意值 |
| [meme-niyijiku](./meme-niyijiku/SKILL.md) | 你已急哭 | 表情包迷因 | 你已急哭、外星人表情包、急了 |
| [meme-wodedaodun](./meme-wodedaodun/SKILL.md) | 我的刀盾 | 空耳梗 | 我的刀盾、刀盾狗、What the dog doing |
| [meme-bibilabu](./meme-bibilabu/SKILL.md) | 比比拉布 | 无意义音效梗 | 比比拉布、bibilabu、Howieazy |
| [meme-nailong](./meme-nailong/SKILL.md) | 奶龙/大笑奶龙 | AI生成抽象梗 | 奶龙、大笑奶龙、奶龙捧腹大笑、变异奶龙 |
| [meme-yanquan](./meme-yanquan/SKILL.md) | 炎拳/对他使用炎拳吧 | 二次元二创模板 | 炎拳、对他使用炎拳、阿格尼脸 ⭐新增 |
| [meme-liuyi](./meme-liuyi/SKILL.md) | 互联网六艺 | 网络文化基础 | 典、孝、急、乐、绷、赢 ⭐新增 |
| [meme-yinhui](./meme-yinhui/SKILL.md) | 淫秽性团结 | 学术梗 | 淫秽性团结、黄图团结 ⭐新增 |

## 安装

将 skill 目录复制到 agent 的 skills 目录：

```bash
# OpenCode / Sisyphus
cp -r meme-* ~/.agents/skills/
```

## 贡献

参见 [AGENTS.md](./AGENTS.md) 了解 skill 格式和添加新梗的流程。

## 协议

[MIT](./LICENSE)

虽然本项目本质是中文互联网迷因知识库（文档/数据集合），但 agent skill 作为 AI 运行时可加载的资源，更接近「可执行知识」，故采用 MIT 许可证以最大化 GitHub 生态兼容性。效果等价于 CC0 的「自由使用」精神，仅增加保留原作者署名条款。
