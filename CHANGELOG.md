# CHANGELOG

## [Unreleased]

### Changed

- `qtrecurit/index.md` 收敛为域介绍与两步意图（投递进收件箱 → 发实训邀请邮件、申请者点群邀请链接进群），撤下「流程」与「Pipeline 分解」导航
- `qtrecurit/send-invite-email.md` 按案例格式成文：需求（情境 / 难点）→ 意图（自然语言 / 形式化规则）→ 规格（自然语言 / YAML）→ 实现，与 quanttide-github 案例集 `second-brain/transfer-submodule-to-another.md` 同构
- 投递发码入口由二维码附件改为群邀请链接：取链要用 HR 用户身份（外部群机器人身份取不到），链接非永久，过期后重发是常规动作
- `qtrecurit/send-invite-email.md` 实现记为可复制的 `lark-cli` 命令序列，并补：投递主题按「岗位-姓名-学校-时长」取第二段解析姓名、发后核对按归档文件夹回读、批量发送每封间隔 1-2 秒避开 `Concurrent write conflict`、缺邮箱的投递不进「待发码」
- qtrecurit 域内文件名统一为小写连字符：`send-invite-email.md`（原 `send_group_qr_email.md`）、`watch-group-entry.md`（原 `watch_group_entry.md`）、`send-survey-email.md`（原 `send_survey_email.md`）
- `CONTRIBUTING.md` 命名规则由下划线改为连字符

### Removed

- 删除 `qtrecurit/watch-group-entry.md`（进群检测）与 `qtrecurit/send-survey-email.md`（问卷发放）两篇 pipeline 文档，域内暂只留投递发码一案

## [0.0.1] - 2026-10-12

初始版本。

- 新增 `qtrecurit/index.md`：量潮招聘的飞书流程
- 新增 qtrecurit 三篇 pipeline 文档（投递发码 / 进群检测 / 问卷发放），index 挂分解导航
- 新增 `CONTRIBUTING.md`：目录围绕业务域，文件围绕一条自动化流水线
- qtrecurit 三篇文件名去掉 `pipeline_` 前缀（pipeline 是概念，不进文件名）
- qtrecurit 三篇文件名改为动宾式：`send_group_qr_email` / `watch_group_entry` / `send_survey_email`
