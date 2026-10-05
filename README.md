# Tau Editor Themes

社区主题与配色包仓库，供 Tau Editor 的主题市场读取 GitHub Raw catalog。

## 目录结构

- `catalog/index.json`：主题市场索引，当前使用 `schemaVersion: 2`；客户端仍兼容 v1 catalog，必须使用公开 HTTPS Raw 地址。
- `themes/`：完整主题包，可同时定义浅色与深色模式。
- `palettes/`：快速配色包，可定义文字、强调色、状态色，以及与该配色一致的应用背景和面板背景。
- `schemas/`：主题包与配色包 JSON Schema。
- `examples/`：普通用户可直接复制修改的示例。

## 当前主题

市场已发布 8 个风格迥异的社区主题：

- `Aurora Neon`：霓虹青紫、适合深色工作流
- `Forest Canopy`：森林绿、低刺激阅读
- `Rose Quartz`：玫瑰粉、柔和编辑体验
- `Amber Terminal`：琥珀终端、复古技术风
- `Violet Paper`：紫罗兰纸张、明亮文档风
- `Oceanic Depths`：深海蓝、冷色专注风
- `Desert Sunset`：沙漠橙、温暖夕阳风
- `Mono Contrast`：黑白高对比、强调可读性

每个主题都同时提供浅色和深色分支，可在 Tau Editor 设置页中安装后切换。`defaultMode` 只表示首次应用时使用的兼容分支，不代表操作系统主题模式；主题风格自身必须携带完整且协调的背景、面板、文字和强调色。

### v2 主题契约

- `modes.light` / `modes.dark` 是兼容分支；至少提供其中一个，并通过 `defaultMode` 指定首次应用分支。
- 完整主题的 `colors.bgApp`、`colors.panelBase` 是界面背景契约，缺少 `panelBase` 时客户端会按当前主题风格回退。
- palette 可以提供 `bgApp` 和 `panelBase`；旧 palette 缺少这两个字段时仍然有效，客户端保留当前背景。
- `ui.radius` 支持旧的数字写法，也支持 `base`、`control`、`card`、`panel`、`tab`、`dialog`、`badge` 分类圆角，数值按 0.5px 步进归一化。
- 远程包只包含 JSON 数据，不加入脚本、HTML、CSS 或可执行 URL。
- `schemas/catalog-v2.schema.json` 描述当前 catalog；客户端继续兼容 `schemaVersion: 1` 的旧 catalog。

## 提交主题

1. 复制 `examples/` 中的示例并修改 `id`、名称、作者、版本和颜色。
2. 把文件放入 `themes/` 或 `palettes/`。
3. 在 `catalog/index.json` 增加对应条目和 Raw 下载地址。
4. 本地运行 JSON 校验后提交 Pull Request。

应用背景和面板背景必须与当前主题分支的文字和强调色保持可读性，避免浅色模式出现白字、深色模式出现黑字。palette 可以覆盖背景，但应提供与文字颜色配套的浅色和深色背景；如果不提供，则沿用当前主题风格背景。

## 许可

提交者应确保拥有所提交颜色方案和名称的使用权。默认以 MIT License 发布仓库中的配置文件。
