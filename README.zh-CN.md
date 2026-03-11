# OpenClaw AutoTrader

这是一个面向公开展示的仓库，服务于 `Tiger Pocket Agent` 的直播追踪场景，只同步脱敏后的自动监控卡片与每日日报/复盘。

[English README](./README.md)

## 仓库命名建议

- 主推荐名：`openclaw-autotrader`
- 命名含义：OpenClaw + 全自动交易执行
- 直播短标题可用：`OpenClaw AutoTrader Daily`

备选名字：

- `tigerpocket-openclaw-autotrader`
- `openclaw-live-autotrader`
- `openclaw-trading-bot`

如果你要兼顾“品牌感”和“可搜索性”，主推荐名最稳，足够简洁，也适合后续拆分子模块。

## 这个仓库是干什么的

这个 repo 适合你每天直播时作为公开主仓库，用来做几件事：

- 发布脱敏后的自动监控卡片
- 每天更新脱敏日报与复盘
- 给直播观众一个稳定可看的公开页面
- 严格避免上传身份、代码和实盘细节

## 推荐目录结构

```text
.
├── README.md
├── README.zh-CN.md
├── .gitignore
├── docs/
│   ├── public-monitor/
│   │   ├── README.md
│   │   └── 2026/
│   │       └── 2026-03-11.md
│   ├── daily-reports/
│   │   ├── README.md
│   │   └── 2026/
│   │       └── 2026-03-11.md
│   ├── weekly-recaps/
│   └── incidents/
├── logs/
│   ├── README.md
│   └── .gitkeep
├── strategies/
│   └── README.md
├── configs/
│   └── .env.example
└── scripts/
    └── README.md
```

## 公开仓库里到底放什么

允许同步到 GitHub 的只有：

- `docs/public-monitor/YYYY/YYYY-MM-DD.md`
- `docs/daily-reports/YYYY/YYYY-MM-DD.md`

不要上传的内容包括：

- 账户余额、现金、收益数字
- 持仓数量、成交价格、成本、PnL
- 订单号、broker 元数据
- token 用量、模型链路
- 身份信息、本机路径、脚本细节、配置真值

## 自动监控卡片放哪里更新

建议固定放在：

- `docs/public-monitor/YYYY/YYYY-MM-DD.md`

例如：

- `docs/public-monitor/2026/2026-03-11.md`

## 每天的交易日报放哪里更新

建议固定放在：

- `docs/daily-reports/YYYY/YYYY-MM-DD.md`

例如：

- `docs/daily-reports/2026/2026-03-11.md`

这样有几个好处：

- 按年份归档，后面几百篇日报也不会乱
- 直播时路径稳定，观众容易理解
- 后续做自动化汇总、统计或网页展示也方便

## 日志怎么处理

真实日志只保留在本机，不提交到这个公开 repo。

`logs/` 目录在仓库里只是一个说明占位，不存放真实运行日志。

## 每日日报建议字段

每篇日报建议至少包含：

1. 市场环境
2. 公开状态快照
3. 动作摘要
4. 当日复盘
5. 异常与风险提示
6. 下一个交易日观察点

## 直播更新流程建议

1. 本地自动交易系统继续产出完整私有监控信息
2. GitHub tracking agent 先做脱敏
3. 自动监控卡片写入 `docs/public-monitor/YYYY/YYYY-MM-DD.md`
4. 每日日报/复盘写入 `docs/daily-reports/YYYY/YYYY-MM-DD.md`
5. repo 只提交和推送这些公开 markdown 文件

## 公开仓库建议

因此配置应该只放模板，不放真值。

## 下一步可以继续做什么

如果你要，我下一步可以继续帮你补：

- 一个更像正式开源项目的首页文案
- GitHub Actions 自动检查公开日报格式
- 更适合直播展示的项目封面和 badge
