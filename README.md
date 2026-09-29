# Tau Editor Themes

社区主题与配色包仓库，供 Tau Editor 的主题市场读取 GitHub Raw catalog。

## 目录结构

- `catalog/index.json`：主题市场索引，必须使用公开 HTTPS Raw 地址。
- `themes/`：完整主题包，可同时定义浅色与深色模式。
- `palettes/`：快速配色包，只允许定义前景色和状态色，不覆盖应用背景和面板背景。
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

每个主题都同时提供浅色和深色模式，可在 Tau Editor 设置页中安装后切换。

## 提交主题

1. 复制 `examples/` 中的示例并修改 `id`、名称、作者、版本和颜色。
2. 把文件放入 `themes/` 或 `palettes/`。
3. 在 `catalog/index.json` 增加对应条目和 Raw 下载地址。
4. 本地运行 JSON 校验后提交 Pull Request。

主题包不能把 `bgApp`、`panelBase` 作为自定义配色字段。应用背景和面板背景由主题模式与主题风格统一管理，避免浅色模式出现白字、深色模式出现黑字。

## 许可

提交者应确保拥有所提交颜色方案和名称的使用权。默认以 MIT License 发布仓库中的配置文件。
