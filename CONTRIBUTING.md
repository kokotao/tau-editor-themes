# Contributing Themes

欢迎通过 Pull Request 分享 Tau Editor 主题和配色包。

## 清单

- 使用 `schemaVersion: 2`。
- `type` 必须是 `theme` 或 `palette`。
- `id` 只能使用小写字母、数字和连字符。
- 同时提供 `modes.light` 与 `modes.dark`，或明确 `defaultMode`。
- 颜色使用 `#RRGGBB` 或 `#RRGGBBAA`。
- 不在 palette 包中加入 `bgApp`、`panelBase`。
- 在 `catalog/index.json` 中加入唯一条目。
- 通过仓库 Actions 的 JSON Schema 校验。

## PR 内容

请说明主题的视觉目标、推荐模式、预览截图（可选）以及是否从已有主题派生。
