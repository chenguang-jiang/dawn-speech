# 来源与整理说明

整理日期：2026-10-18。以下版本号为本次读取时的 Git 提交，可用于核对；不表示跟随上游自动更新。

| 来源 | 本次版本 | 采用内容 |
| --- | --- | --- |
| [oil-oil/oil-tone](https://github.com/oil-oil/oil-tone/tree/39cbf92f76c90b7bb27a5b5d4ed88a1fc5fa31f6) | `39cbf92f76c90b7bb27a5b5d4ed88a1fc5fa31f6` | 主要基础：事实边界、理解顺序、自然语法、虚词处理、全文连读；改编中文措辞提示脚本 |
| [blader/humanizer](https://github.com/blader/humanizer/tree/8c307f367c91bd974002f10f2be2965d642c13df) | `8c307f367c91bd974002f10f2be2965d642c13df` | 参考样文匹配、结构层面的模板表达识别、改写后检查事实增删 |
| [softaworks/agent-toolkit](https://github.com/softaworks/agent-toolkit/tree/3027f20f3181758385a1bb8c022d4041dfb4de84/skills/writing-clearly-and-concisely) | `3027f20f3181758385a1bb8c022d4041dfb4de84` | 参考具体用词、段落集中一个主题、相关词靠近与删减冗余的原则 |

## 取舍

- 以 GitHub 最新版 oil-tone 为基础，而非直接复制本地较旧版本。保留“常用单字动词可以直接使用”的规则，不恢复机械替换要求。
- 不绑定 oil 的姓名、经历和固定公众号问候；也不把 Dawn 当作所有用户的真实姓名。
- 借鉴 Humanizer 的检查思路，不照搬其默认同时输出草稿、批评和终稿的流程，也不采用全面禁止破折号的要求。
- 不把英文写作教材的语法细则机械应用到中文，不把简洁等同于删除必要虚词。
- 不合并多个技能的完整规则清单，避免重复和指令冲突。技能本身无需安装上游技能，也没有运行时网络依赖。
- 新增示例用于澄清范围和事实边界；不声称通过 AI 检测，不保证匹配未提供的个人风格。

## 许可与归属

oil-tone 为 MIT，Copyright (c) 2026 oil-oil。本仓库包含其改编内容与脚本，完整许可保留于根目录 [LICENSE](LICENSE)。

Humanizer 为 MIT，Copyright (c) 2025 Siqi Chen；agent-toolkit 为 MIT，Copyright (c) 2026 Leonardo Flores。本次参考其方法并重新组织为中文规则，未打包其代码、整篇技能、教程或示例。为明确归属，以下保留两者的 MIT 声明：

```text
MIT License

Copyright (c) 2025 Siqi Chen
Copyright (c) 2026 Leonardo Flores

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
