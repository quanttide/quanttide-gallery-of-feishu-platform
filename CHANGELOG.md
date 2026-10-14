# CHANGELOG

## [Unreleased]

### Changed

- `qtrecurit/send-invite-email.md` 按案例格式重写：需求（情境 / 难点）→ 意图（规则 / 形式化）→ 规格（自然语言 / YAML）→ 实现，与 quanttide-github 案例集 `second-brain/transfer-submodule-to-another.md` 同构
- qtrecurit 三篇文件名统一为连字符：`send-invite-email.md`（原 `send_group_qr_email.md`）、
  `watch-group-entry.md`（原 `watch_group_entry.md`）、`send-survey-email.md`（原 `send_survey_email.md`）
- `CONTRIBUTING.md` 命名规则由下划线改为连字符；`qtrecurit/index.md` 链接同步

## [0.0.1] - 2026-10-12

初始版本。

- 新增 `qtrecurit/index.md`：量潮招聘的飞书流程
- 新增 qtrecurit 三篇 pipeline 文档（投递发码 / 进群检测 / 问卷发放），index 挂分解导航
- 新增 `CONTRIBUTING.md`：目录围绕业务域，文件围绕一条自动化流水线
- qtrecurit 三篇文件名去掉 `pipeline_` 前缀（pipeline 是概念，不进文件名）
- qtrecurit 三篇文件名改为动宾式：`send_group_qr_email` / `watch_group_entry` / `send_survey_email`
