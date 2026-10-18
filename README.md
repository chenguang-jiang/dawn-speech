# dawn-speech

让文章、口播、演讲与产品文案自然、清楚、有事实依据的写作技能。支持中文和英文，适用于支持 `SKILL.md` 的 Agent。

基于 [oil-tone](https://github.com/oil-oil/oil-tone) 整理，参考 [Humanizer](https://github.com/blader/humanizer) 和 [Writing Clearly and Concisely](https://github.com/softaworks/agent-toolkit/tree/main/skills/writing-clearly-and-concisely)。保留事实边界和自然表达原则，增加改写范围控制、样文匹配与口播适配，不绑定原作者身份。

## 安装

将本仓库克隆到 Agent 的技能目录，目录名保留为 `dawn-speech`。例如，Codex 默认用户技能目录：

```bash
git clone https://github.com/chenguang-jiang/dawn-speech.git ~/.codex/skills/dawn-speech
```

如果设置了 `CODEX_HOME`，请使用对应的 `skills/dawn-speech` 目录。若目标目录已存在，先检查现有版本，避免覆盖个人修改。其他 Agent 使用各自的技能目录；重新加载技能或开启新会话后使用。

## 使用

```text
使用 $dawn-speech 润色下面的文章，保留观点、信息顺序和个人判断。

使用 $dawn-speech，把这份材料整理成约 3 分钟的中文口播。
受众是不熟悉这个产品的读者，保留目前尚未测试的限制。

使用 $dawn-speech，参考这两段我自己的文章调整语气。
样文只用于匹配表达，不作为新稿的事实来源。
```

没有样文时采用平实语气，不假装已经学会作者个人风格。称呼、署名、固定开场白和品牌信息由用户提供。

## 与原版的整理差异

| 内容 | dawn-speech 的处理 |
| --- | --- |
| 自然、易读、通顺、清楚 | 保留，优先于压缩字数与书面化 |
| 事实和个人判断 | 保留，并明确条件、统计口径和成果归属 |
| 润色与重写 | 分开约定允许修改的范围 |
| 减少 AI 腔 | 按语境复核结构和套话，不机械禁词 |
| 个人风格 | 支持样文匹配，不预设作者身份或经历 |
| 口播和演讲 | 补充听众理解顺序、停顿和时长粗估方法 |
| 输出 | 默认只给一版成稿，按要求提供审稿或说明 |
| 辅助检查 | 保留轻量中文提示脚本，修正部分 Markdown 误报 |

## 文件

- [SKILL.md](SKILL.md)：技能入口与写作规则。
- [references/examples.md](references/examples.md)：改写边界与正反例，按需读取。
- [scripts/tone_lint.py](scripts/tone_lint.py)：仅使用 Python 标准库的中文措辞提示。
- [agents/openai.yaml](agents/openai.yaml)：Codex 展示名称与默认提示。
- [SOURCES.md](SOURCES.md)：来源版本、采用内容与取舍。

可选检查：

```bash
python3 scripts/tone_lint.py article.md
python3 scripts/tone_lint.py --self-test
```

`WARN` 提示需要结合语境复核，正常扫描返回码为 0；读取失败或参数错误返回非零。脚本不修改文件，不验证事实，不检测 AI 作者，不支持直接解析 PDF 或 Word。

## 许可

MIT。保留 oil-tone 上游版权声明；相关参考与许可见 [SOURCES.md](SOURCES.md)。
