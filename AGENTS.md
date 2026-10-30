# Agent instructions — 越南项目

This folder is the **越南项目** clickable prototype. Its admin is a copy of the Juan365 admin (`qq-admin-prototype`): same menus, pages, and interactions.

It is **not**:

- Juan365 管理后台 (`qq-admin-prototype`)
- 365 前台 (`365-frontend-prototype`)
- 体育管理后台 (`qq-sports-admin-prototype`)
- 体育风控后台 (`qq-sports-risk-prototype`)
- U8棋牌后台 (`qq-u8-chess-admin-prototype`)
- 活动平台 (`qq-activity-platform-prototype`)
- 萌宠乐园 / 抽奖 / QRPH 任一仓库

**需求文档规范：** 本项目需求文档一律按 [`docs/产品文档规范要求.md`](./docs/产品文档规范要求.md) 的六段结构编写。完整 PRD：[`docs/越南项目-开发测试宣讲需求.md`](./docs/越南项目-开发测试宣讲需求.md)。

- Do **not** copy pages, menus, or localStorage keys back into `qq-admin-prototype` or any other repo.
- Do **not** pull later 365 / 抽奖定稿 changes into this repo unless the user names 越南.
- Visual: dark sidebar + white Ant-like forms, **Chinese**. Logo text stays `JUAN` because this admin was copied from 365. Browser title is `越南管理后台`.
- Data: `localStorage` key `vietnam_admin_v1`, session `vietnam_admin_session_v1`. Do not reuse `juan365_*`.
- 列表必须用真实感虚拟数据（`AdminStore.demoValue`），禁止「字段 A/B/C」。
- Prototype **skips login**: open `admin/index.html` to see the full admin. `login.html` only redirects.
- Push to GitHub **only** when the user says **定稿**.

## Where to edit

| Surface | Path |
|---------|------|
| 后台 SPA | `admin/index.html` + `admin/js/*.js` |
| 样式 | `admin/css/admin.css` |
| 演示数据 / 权限 | `admin/js/store.js` |
| 页面渲染 | `admin/js/pages.js` |
| 目录页 | `admin/js/catalog.js` |
| 侧栏 / 顶栏 | `admin/js/shell.js` |

Serve from **project root**: `python3 -m http.server 8787`.

## Hard rules

1. 菜单、子页面、抽屉字段、二次确认与 365 管理后台一致。不要在本仓另写第二套活动公式、抽奖公式或资金口径。宝箱裂变活动的新增 / 编辑配置与 `qq-admin-prototype` 保持同一套，用户未另说时两边一起改。
2. 一级菜单锁定：会员管理、投注记录、充值提款、资金操作、平台游戏、优惠活动、报表管理、任务系统、联盟管理、综合报告、渠道管理、信息配置、平台配置、负责任博彩管理、投注站管理、风控管理、盈亏异常用户名单、地推管理、系统设置。点 Logo 进仪表盘。
3. 资金类操作必须二次确认。
4. 抽奖活动规则以拷贝进来的模版为准。抽奖定稿默认同步 Juan365，不要自动改本仓。
5. 不要把本仓菜单或 `vietnam_admin_v1` 写回 365。不要在新写的落地页、列表、Toast、页脚加「演示环境」类提示；已随 365 后台拷入的原文案保持不动。

## Naming

- **项目名称：越南项目**
- 站内产品名：越南管理后台
