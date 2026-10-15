# CHANGELOG

## [Unreleased]

### Added

- 新增 `qtadmin/` 域：`index.md` 与 `delib.md`——内部管理周会议事案例（主持人与书记员分工、会前准备、会中议事与投票、纪要区块结构、大群播报格式、检查清单），人名、客户与治理决策已类型化脱敏

### Changed

- `CONTRIBUTING.md`：文件模型由「自动化流水线」放宽为「业务流程」，人主导的议事流程可单独成文
- `qtrecurit/send-invite-email.md`：投递主题示例改用虚构姓名与高校（张三 / 某高校），并以 `git filter-repo` 清理历史中的真实信息

## [0.1.0] - 2026-10-14

### Changed

- `qtrecurit/index.md` 升级流程：信息流 邮箱（申请）→ 群（沟通）→ 实训基地（初审）→ 公司（复审）
- 记状态落为邮箱侧动作：投递邮件标记已读并移入「已发送实训邀请」文件夹（旧流程的「已邀请入群」），一条 `mail user_mailbox.messages modify` 同时完成
- `qtrecurit/send-invite-email.md` 按案例格式成文：需求（情境 / 难点）→ 意图（自然语言 / 形式化规则）→ 规格（自然语言 / YAML）→ 实现，与 quanttide-github 案例集 `second-brain/transfer-submodule-to-another.md` 同构
- 投递发码入口由二维码附件改为群邀请链接：取链要用 HR 用户身份（外部群机器人身份取不到），链接非永久，过期后重发是常规动作
- `qtrecurit/send-invite-email.md` 实现记为可复制的 `lark-cli` 命令序列，并补：投递主题按「岗位-姓名-学校-时长」取第二段解析姓名、发后核对按归档文件夹回读、批量发送每封间隔 2-10 秒避开 `Concurrent write conflict`、缺邮箱的投递不进「待发码」
- qtrecurit 域内文件名统一为小写连字符：`send-invite-email.md`（原 `send_group_qr_email.md`）、`watch-group-entry.md`（原 `watch_group_entry.md`）、`send-survey-email.md`（原 `send_survey_email.md`）
- `qtrecurit/send-invite-email.md` 规格与实现补批量：分轮跑、每轮固定人数、多轮到未读清空（投递从晚到早，未读即未处理），轮内逐人执行四步，跳过已发/姓名解析不出/缺邮箱，单人失败不阻断、轮末补跑，每轮取链轮内复用，两层节流防并发（间隔实测定为 2-10 秒），产出报告；批量临时脚本写系统 `/tmp`、跑完即删
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
