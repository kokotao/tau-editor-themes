# Tau Editor Themes

社区主题与配色包仓库，供 Tau Editor 的主题市场读取 GitHub Raw catalog。

## 目录结构

- `catalog/index.json`：主题市场索引，必须使用公开 HTTPS Raw 地址。
- `themes/`：完整主题包，可同时定义浅色与深色模式。
- `palettes/`：快速配色包，只允许定义前景色和状态色，不覆盖应用背景和面板背景。
- `schemas/`：主题包与配色包 JSON Schema。
- `examples/`：普通用户可直接复制修改的示例。

## 提交主题

1. 复制 `examples/` 中的示例并修改 `id`、名称、作者、版本和颜色。
2. 把文件放入 `themes/` 或 `palettes/`。
3. 在 `catalog/index.json` 增加对应条目和 Raw 下载地址。
4. 本地运行 JSON 校验后提交 Pull Request。

主题包不能把 `bgApp`、`panelBase` 作为自定义配色字段。应用背景和面板背景由主题模式与主题风格统一管理，避免浅色模式出现白字、深色模式出现黑字。

## 许可

提交者应确保拥有所提交颜色方案和名称的使用权。默认以 MIT License 发布仓库中的配置文件。
