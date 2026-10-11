# 个人工作台 v0.1.1

> 移除记账模块，保留计划、专注、知识库与日记。

**发布类型**：功能调整，体验版 / Prerelease。  
**上一版本**：本地测试阶段，最近为 Android 第十九版；本仓库首次公开发布。  
**系统要求**：Windows 11 x64；Android 构建最低 API 24 / Android 7，未逐一验证所有系统版本。  
**日期**：2026-10-11。

---

## 下载

| 平台 | 安装包 | 大小 | 说明 |
| --- | --- | --- | --- |
| Windows x64 | [下载 EXE](https://github.com/lyq-05/personal-workbench/releases/download/v0.1.1/personal-workbench-v0.1.1-windows-x64-setup.exe) | 193.45 MiB | Squirrel 安装程序，未代码签名 |
| Android | [下载 APK](https://github.com/lyq-05/personal-workbench/releases/download/v0.1.1/personal-workbench-v0.1.1-android.apk) | 42.51 MiB | 测试签名，versionCode 20 |

[SHA256SUMS.txt](https://github.com/lyq-05/personal-workbench/releases/download/v0.1.1/SHA256SUMS.txt)

## 升级说明

- 先在设置中导出结构化备份；知识库与日记文件需要另外导出或备份目录。
- Android 保持既有包名与签名，可尝试覆盖旧测试版；不要为了安装先卸载或清数据。签名冲突时停止并确认版本来源。
- Windows 未签名，系统可能提示未知发布者。请核对下载来源，不建议关闭系统安全保护。
- 旧账目数据库不删除，备份格式继续兼容，但本版无法再使用记账界面。**没有自动迁移至独立记账应用的功能。**
- 尚未完成 Windows / Android 实际覆盖升级验收；备份后再体验。

## 本次更新

| 操作/位置 | 本版行为 |
| --- | --- |
| 首次引导、设置、记录页 | 不再显示记账开关和账目入口 |
| 读取旧配置、恢复旧备份 | 记账模块保持关闭，不会重新开启 |
| Android 支付采集 | 删除服务声明、插件注册，构建排除采集类；不再监听支付通知或页面 |
| 历史数据 | 保留旧数据库与备份兼容，不清空用户账目 |
| 其他工作台模块 | 继续保留计划、专注、知识库、日记等能力 |

## 界面

隔离数据的真实渲染预览，不是 Android 真机截图。

<table><tr><th>桌面计划</th><th>手机记录</th></tr><tr><td><img width="640" alt="桌面计划" src="https://raw.githubusercontent.com/lyq-05/personal-workbench/v0.1.1/docs/screenshots/01-plan-desktop.png"></td><td><img width="260" alt="手机记录" src="https://raw.githubusercontent.com/lyq-05/personal-workbench/v0.1.1/docs/screenshots/02-records-mobile.png"></td></tr></table>

## 验证与已知问题

已通过 192 项自动测试、TypeScript 检查、离线冒烟检查、前端构建与双平台打包。隔离预览验证了旧记账开关无法开启、入口消失及模拟历史记录未被删除。APK 清单和 DEX 检查确认支付监听/无障碍采集服务及采集类不在包内，签名校验通过。

Windows 打包后的完整界面冒烟测试未全部通过：知识库紧凑布局测得文件索引栏宽度为 0，未达到现有测试预期。尚未确定是布局行为还是测试预期需要调整，本次未修改知识库。上述通过项不代表完整界面测试通过。

这些检查不替代真机使用。本版仍待验证：Windows 安装/升级、Android 覆盖升级、各机型后台提醒与旧数据恢复。手机后台策略仍可能影响任务提醒；Windows 未代码签名，Android 为测试签名。没有自动云同步或独立记账应用迁移。

## 相关链接

[项目首页](https://github.com/lyq-05/personal-workbench) · [更新记录](https://github.com/lyq-05/personal-workbench/blob/main/CHANGELOG.md) · [早期本地测试说明](https://github.com/lyq-05/personal-workbench/blob/main/docs/HISTORY.md)
