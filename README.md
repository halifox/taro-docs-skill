# Taro Docs Skill

面向支持 Agent Skills 的 AI agent 的 Taro 中文文档查询 Skill，内置 Taro 1.x、2.x、3.x 和 4.x 的文档快照。适合查配置、组件和 API，也可以用来核对平台支持情况或跨版本迁移时的用法差异。

## 工作流程

1. **确定版本和平台。** 优先采用问题中指定的版本和平台。结合现有项目排查时，查看项目依赖、构建命令或配置。
2. **定位相关文档。** 在对应版本下按文件名、API 签名或组件名搜索，按主题浏览时使用完整目录。
3. **核对并引用。** 检查参数、返回值、平台支持和版本限制。比较多个版本时分别查阅，并在回答中引用文档页首的原始链接。

## 文件说明

| 文件或目录 | 用途 |
| --- | --- |
| [`SKILL.md`](skills/taro-docs/SKILL.md) | Skill 入口，包含版本选择、文档查找和引用规则 |
| [`INDEX.md`](skills/taro-docs/INDEX.md) | 按版本和主题组织的完整文档目录 |
| [`references/`](skills/taro-docs/references/) | Markdown 文档。4.x 位于此目录，旧版分别位于 `3.x/`、`2.x/` 和 `1.x/` |
| [`assets/`](skills/taro-docs/assets/) | 文档引用的本地图片 |
| [`LICENSE`](skills/taro-docs/LICENSE) | 随 Skill 一起分发的 MIT 许可证 |

## 安装

在终端运行以下命令，并按提示选择要安装 Skill 的 agent。

```bash
npx skills add halifox/taro-docs-skill --skill taro-docs
```

如需在多个项目中使用，可添加 `--global` 安装到用户级目录。 [Skills CLI 文档](https://github.com/vercel-labs/skills/blob/main/docs/commands.md)

## 使用

安装后，可以直接向 agent 提问，并说明要查的 Taro 版本和目标平台。

```text
用 taro-docs 查一下 Taro 3.x 的 Taro.request 在微信小程序和 H5 的支持情况，附上文档来源。
```

在现有项目中，可以让 agent 结合项目配置查询。

```text
用 taro-docs 根据这个项目使用的 Taro 版本，检查微信小程序的分包配置，并引用相关文档。
```

## 环境要求

- 使用支持 [Agent Skills](https://agentskills.io/home) 的 AI agent。
- 通过 `npx` 安装时需要 Node.js 和 npm。
- 文档随 Skill 一起安装，查询快照时直接读取本地 Markdown 文件。

## 设计原则

- **以版本和平台为准。** 同名 API 的参数和支持情况可能随版本或平台变化，结论以所查版本的文档为准。
- **按需读取。** 入口只保留查询流程，完整目录和文档正文在需要时读取。
- **保留出处。** 文档页首保留原始链接，便于回查。 [Taro 文档上游仓库](https://github.com/NervJS/taro-docs)

## 反馈

文档缺失、目录链接错误或安装问题可以在 GitHub 提交。反馈时附上 Taro 版本、目标平台和相关文档路径。 [GitHub Issues](https://github.com/halifox/taro-docs-skill/issues)

## 许可证

本项目采用 MIT 许可证，保留上游版权声明。 [仓库许可证](LICENSE)
