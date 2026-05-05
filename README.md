# meme-skills

中文互联网迷因（meme）知识库，以 open agent skill 格式维护。每个 skill 可供 AI agent 在对话中按需加载，获取精确的文化语境知识。

## 为什么

LLM 的训练数据永远滞后于中文互联网的造梗速度。当用户说"豪意值拉满"，AI 却一本正经地拆字释义——这很准确，但也很扫兴。

一个真正称职的个人 AI 助手，不该只是个工具。它应该懂你的梗，接得住你的玩笑。你说"你已急哭"，它能回:"那你别急。"

本项目将热梗知识以 open agent skill 格式组织分发，让任何 AI agent 按需加载，跟上梗的版本，不做局外人。

## 已收录梗

| Skill | 梗名 | 分类 | 触发关键词 |
|---|---|---|---|
| [meme-jiahao](./meme-jiahao/SKILL.md) | 嘉豪 | 网络流行词 | 嘉豪、嘉欣、豪意值 |
| [meme-niyijiku](./meme-niyijiku/SKILL.md) | 你已急哭 | 表情包迷因 | 你已急哭、外星人表情包、急了 |
| [meme-wodedaodun](./meme-wodedaodun/SKILL.md) | 我的刀盾 | 空耳梗 | 我的刀盾、刀盾狗、What the dog doing |
| [meme-bibilabu](./meme-bibilabu/SKILL.md) | 比比拉布 | 无意义音效梗 | 比比拉布、bibilabu、Howieazy |

## 安装

将 skill 目录复制到 agent 的 skills 目录：

```bash
# OpenCode / Sisyphus
cp -r meme-* ~/.agents/skills/
```

## 贡献

参见 [AGENTS.md](./AGENTS.md) 了解 skill 格式和添加新梗的流程。

## 协议

[CC0 1.0 Universal](./LICENSE) — 放弃一切版权及相关权利，可自由复制、修改、分发，无需署名。
