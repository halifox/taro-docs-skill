# Taro 中文文档 Skill

面向 Codex 的社区整理版 Agent Skill，收录 Taro 1.x、2.x、3.x 和 4.x 的中文文档快照。它按项目版本和目标平台查阅配置、组件、API 及迁移文档，并提供原始页面链接。安装后可直接查阅本地 Markdown。

## 安装

### 从本地仓库安装到 Codex

在本仓库根目录运行以下命令，把完整 Skill 安装到当前用户的 Codex 技能目录。目标路径已有同名 Skill 时，先检查该安装的来源。

```bash
mkdir -p "$HOME/.agents/skills"
taro_skill_path="$HOME/.agents/skills/taro-docs"
if [ ! -e "$taro_skill_path" ] && [ ! -L "$taro_skill_path" ]; then
  ln -s "$PWD/skills/taro-docs" "$taro_skill_path"
else
  printf '目标路径已存在：%s\n' "$taro_skill_path" >&2
fi
```

### 从公开 GitHub 仓库安装

仓库公开发布后，把命令中的 `OWNER` 替换为实际 GitHub 用户名或组织名。以下命令使用 Vercel 的 `skills` CLI。

```bash
npx skills add OWNER/taro-docs-skill --skill taro-docs --agent codex --global
```

也可在 Codex 中通过内置 Skill 安装器安装。

```text
$skill-installer install https://github.com/OWNER/taro-docs-skill/tree/main/skills/taro-docs
```

## 使用

在 Codex 中调用。

```text
$taro-docs 查一下 Taro 3.x 的 Taro.request 在微信小程序和 H5 的支持情况，附上文档来源。
```

也可以直接浏览[文档目录](skills/taro-docs/INDEX.md)和 [Skill 入口](skills/taro-docs/SKILL.md)。

## 文档来源与许可证

文档来自 Taro 中文文档，各页保留「原始页面」链接。此仓库由社区整理，文档以收录快照为准。上游源码和许可声明见 [NervJS/taro-docs](https://github.com/NervJS/taro-docs)。

项目采用 [MIT 许可证](LICENSE)，并保留上游版权声明。[Skill 目录](skills/taro-docs/)内也附有一份[许可证](skills/taro-docs/LICENSE)，供单独安装时一并分发。
