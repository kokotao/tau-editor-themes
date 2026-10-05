# Contributing Themes

欢迎通过 Pull Request 分享 Tau Editor 主题和配色包。

## 清单

- 使用 `schemaVersion: 2`。
- `type` 必须是 `theme` 或 `palette`。
- `id` 只能使用小写字母、数字和连字符。
- 同时提供 `modes.light` 与 `modes.dark`，或至少提供一个分支并明确 `defaultMode`。
- 颜色使用 `#RRGGBB` 或 `#RRGGBBAA`。
- 完整主题应在每个提供的分支中配置 `bgApp`、`textPrimary`，推荐同时配置 `panelBase`。
- palette 可以配置 `bgApp`、`panelBase`；如果省略，客户端会保留当前主题风格的背景。
- 可选的 `ui.radius` 支持数字或分类对象：`base`、`control`、`card`、`panel`、`tab`、`dialog`、`badge`。普通分类建议在 0–24px 内，`badge` 可使用 999px 胶囊值。
- 在 `catalog/index.json` 中加入唯一条目。
- 通过仓库 Actions 的 JSON Schema 校验。

## PR 内容

请说明主题的视觉目标、默认分支、背景/面板配色、圆角策略、预览截图（可选）以及是否从已有主题派生。
