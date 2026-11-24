# Taro Docs Skill

给 Codex 用的 Taro 中文文档查询 Skill。收录 Taro 1.x、2.x、3.x 和 4.x 的文档快照，可按项目版本和目标平台查阅配置、组件、API 和迁移指南，并引用原始文档。

## 安装

在终端运行以下命令，将 `taro-docs` 安装到 Codex 的用户技能目录。

```bash
npx skills add halifox/taro-docs-skill --skill taro-docs --agent codex --global
```

也可以在 Codex 对话中使用内置安装器。

```text
$skill-installer install https://github.com/halifox/taro-docs-skill/tree/main/skills/taro-docs
```

## 使用

在 Codex 中输入 `$taro-docs`，并在问题里注明 Taro 版本和目标平台。

```text
$taro-docs 查一下 Taro 3.x 的 Taro.request 在微信小程序和 H5 的支持情况，附上文档来源。
```

也可以在项目中直接提问，例如「检查这个 Taro 项目的微信小程序分包配置，并引用对应版本的配置文档」。Skill 会根据项目依赖和构建配置确认版本与平台。

## 文档目录

[完整目录](skills/taro-docs/INDEX.md)按版本组织，可直接在 GitHub 上浏览。[Skill 入口](skills/taro-docs/SKILL.md)说明 Codex 如何选择版本和引用页面。

## 来源与许可证

本项目由社区整理，文档来自 Taro 中文文档。各页顶部保留「原始页面」链接，便于回查。 [Taro 文档上游仓库](https://github.com/NervJS/taro-docs)

本项目采用 MIT 许可证并保留上游版权声明。单独安装的 Skill 目录也包含许可证。 [仓库许可证](LICENSE) · [Skill 许可证](skills/taro-docs/LICENSE)
