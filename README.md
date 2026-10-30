# 越南项目

独立可点原型：**越南项目**。管理后台照搬 Juan365 管理后台（`qq-admin-prototype`）的菜单、页面和交互。与 Juan365 / 365 前台 / 体育管理后台 / 体育风控后台 / U8棋牌后台 / 活动平台 **不是同一个系统**。

演示数据在浏览器 `localStorage` 键 `vietnam_admin_v1`。不要复用 `juan365_admin_v4`。

**项目名称：越南项目**

## 本地打开

```bash
cd /Users/Admin/Projects/qq-vietnam-prototype
python3 -m http.server 8787
```

- 入口：http://localhost:8787/
- 后台（打开即进，无需登录）：http://localhost:8787/admin/index.html#/dashboard

暗色侧栏 + 白底表单，中文。侧栏 Logo 仍为 **JUAN**（照搬 365 管理后台）。浏览器标题为「越南管理后台」。

## 给开发 / 测试宣讲

完整需求：[`docs/越南项目-开发测试宣讲需求.md`](./docs/越南项目-开发测试宣讲需求.md)

短页：[`docs/prd.html`](./docs/prd.html)

Agent 约定：[`AGENTS.md`](./AGENTS.md)

## 目录

```
qq-vietnam-prototype/
  admin/     # 照搬 365 的管理后台
  docs/      # 六段 PRD
  README.md
  AGENTS.md
```
