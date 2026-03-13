![Day 5 Poster](./docs/assets/challenge-poster.svg)

# 30-Day OpenClaw AutoTrader Challenge

Watch a 5000 HKD 🦞 claw take on 30 public market days in U.S. stocks.
看一只起步于 5000 HKD 的 🦞 claw，连续 30 天公开挑战美股市场。

Last synced by decision / 决策触发同步时间: `2026-03-14 00:49:43 CST`

## Why Follow This Repo / 为什么值得关注

- a real 30-day live challenge, not backtest theater / 一个真实连续 30 天的实盘挑战，不是回测表演
- public updates on decisions, recaps, and turning points / 决策变化、每日复盘和关键转折都会公开更新
- a visible learning log that shows how the 🦞 claw updates its lessons over time / 一个公开学习日志，能看到 🦞 claw 如何随着挑战推进不断更新经验

## Challenge Dashboard / 首页进度看板

| Metric | Value |
| --- | --- |
| Day / 当前天数 | `5 / 30` (16.7%) |
| Starting capital / 起始资金 | `5000 HKD` |
| Current equity / 当前权益 | HKD 4,889.86 |
| Net PnL / 累计盈亏 | -HKD 110.14 |
| Open positions / 当前持仓标的 | 1 open: `BABA` |
| Latest move / 最新动作 | [US] HOLD / [US] 观望 |

## 30-Day Tracker / 30 天挑战总览

- Full challenge index / 全部挑战索引: [docs/challenge-tracker.md](./docs/challenge-tracker.md)
- Public memory / 公开记忆: [docs/public-memory/README.md](./docs/public-memory/README.md)

## Learning Log / 学习日志

Follow how the 🦞 claw turns finished trades, missed timing, and quiet sessions into reusable lessons.
看这只 🦞 claw 如何把已完成交易、时机判断和观望时段，沉淀成可复用的公开经验。

- Latest learning log / 最新学习日志: [docs/public-memory/README.md](./docs/public-memory/README.md)
- Daily notes / 每日学习记录: [docs/public-memory/short-memory.md](./docs/public-memory/short-memory.md)
- Durable lessons / 长期经验库: [docs/public-memory/long-memory.md](./docs/public-memory/long-memory.md)

## Latest Snapshot / 最新概览

- Updated / 更新时间: 2026-03-14 00:49:42 CST (UTC+08:00)
- Current book / 当前组合: `BABA`
- Floating PnL / 当前浮动盈亏: -HKD 18.10
- Latest decision / 最新决策: [US] HOLD / [US] 观望
- Next milestone / 下一阶段: Day `6` of `30`
- Public monitor / 公开监控: [docs/public-monitor/2026/2026-03-14.md](./docs/public-monitor/2026/2026-03-14.md)
- Daily report / 每日报告: [docs/daily-reports/2026/2026-03-14.md](./docs/daily-reports/2026/2026-03-14.md)

## Today's Trading Rules & Adjustments / 今日交易规则与策略调整

- Execution objective / 执行目标: deploy pocket capital only when the expected edge remains meaningfully above fees and sizing limits, with no leverage and no shorting. 仅在预期优势明显高于手续费且满足仓位上限时动用口袋资金，不加杠杆、不做空。
- Session discipline / 时段纪律: live decisions stay inside regular sessions, capped at 1 trade(s) per hour, with a 25% cash reserve and HKD 90 daily loss stop. 实盘决策仅在常规交易时段内执行，每小时最多 1 笔，并保留 25% 现金缓冲，单日亏损达到 HKD 90 即停止扩张。
- Live pools today / 今日实盘池: US: `MU`, `AMD`, `BABA` | HK: `1810.HK`, `3750.HK`, `0388.HK`. 今日实盘池如上，按市场分别执行。
- Observation focus today / 今日观察重点: themes `半导体`, `AI芯片`, `云软件`, `中概`, `电动车`, `手机链`, `消费电子`, `CPO`, `光模块`, `存储`; public observation pool US: `SNDK`, `AAOI`, `EWY`, `COHR`, `TSM`, `LITE`, `TSLA`, `BIDU` | HK: `9868.HK`, `2015.HK`, `0981.HK`, `9888.HK`, `3690.HK`, `9961.HK`. 今日观察主题为 `半导体`, `AI芯片`, `云软件`, `中概`, `电动车`, `手机链`, `消费电子`, `CPO`, `光模块`, `存储`，并同步公开观察池变化。
- Explicit exclusions / 明确排除: `智谱`, `MiniMax`, `三星电子`, `SK 海力士`, `7709.HK` stay out of the live universe when they violate the rules. 凡与规则冲突的标的（如上）均不进入实盘池。
- Latest gate result / 最新门槛结论: No US candidate cleared the live entry bar. The strongest name, `MU`, still showed score -1.94, post-fee EV -0.72%, and win probability 56.2%. / 维持 HOLD。comparison_stage 已明确首选 HOLD，且当前没有足够具体的新证据支持推翻。三只允许标的中，MU、BABA、AMD 的 ev_after_fee_pct 分别约为 -0.7232%、-2.1814%、-3.2824%，全部为负，均未满足“预期优势显著高于往返交易成本”的硬约束；其中 MU 虽相对最好，但仍未达到可执行阈值。事件层也不支持新开仓：latest_event_signals.market_gate.block_new_buys=true，市场级原因包括 geopolitics_risk 与 shipping_disruption，属于先阻断新增买入的硬门控。资金层面同样不构成可行动作：可用 pocket_cash_hkd 仅 1801.19，虽勉强达到 min_trade_notional_hkd 1800，但几乎贴线，扣除单笔费用 15.6 HKD 后缺乏有效缓冲，同时还要遵守 25% cash reserve 与 prefer_fewer_trades。现有 BABA 持仓约 0.938 股，按现价约 126.95 USD，折合大致仍低于进行一笔合规减仓后保留 min_residual_position_hkd 1000 的理想操作空间；而且当前并无止损、止盈或强制风险下降触发，因此最优净收益决策仍是空操作。

## Latest Decision Basis / 最新决策依据

- Result / 结果: [US] HOLD / [US] 观望
- Rationale / 理由: No US candidate cleared the live entry bar. The strongest name, `MU`, still showed score -1.94, post-fee EV -0.72%, and win probability 56.2%. / 维持 HOLD。comparison_stage 已明确首选 HOLD，且当前没有足够具体的新证据支持推翻。三只允许标的中，MU、BABA、AMD 的 ev_after_fee_pct 分别约为 -0.7232%、-2.1814%、-3.2824%，全部为负，均未满足“预期优势显著高于往返交易成本”的硬约束；其中 MU 虽相对最好，但仍未达到可执行阈值。事件层也不支持新开仓：latest_event_signals.market_gate.block_new_buys=true，市场级原因包括 geopolitics_risk 与 shipping_disruption，属于先阻断新增买入的硬门控。资金层面同样不构成可行动作：可用 pocket_cash_hkd 仅 1801.19，虽勉强达到 min_trade_notional_hkd 1800，但几乎贴线，扣除单笔费用 15.6 HKD 后缺乏有效缓冲，同时还要遵守 25% cash reserve 与 prefer_fewer_trades。现有 BABA 持仓约 0.938 股，按现价约 126.95 USD，折合大致仍低于进行一笔合规减仓后保留 min_residual_position_hkd 1000 的理想操作空间；而且当前并无止损、止盈或强制风险下降触发，因此最优净收益决策仍是空操作。
- Decision basis / 决策依据: Regime: mixed tape; Path: compare-stage hold review; Model: GPT-5.4; Purpose: hold discipline; confidence 0.00. / 市场状态：混合状态；决策链路：候选比较后维持观望；模型：GPT-5.4；目的：观望纪律；置信度 0.00。
- Candidate check / 候选检查: Reviewed 3 active candidate(s). Top checks: `MU` (semiconductor) | score -1.94 | post-fee EV -0.72% | win 56.2%; `BABA` (China internet) | score -2.68 | post-fee EV -2.18% | win 49.6%; `AMD` (semiconductor) | score -4.44 | post-fee EV -3.28% | win 43.3%. / 共检查 3 只活跃候选。靠前检查结果：`MU`（半导体） | 评分 -1.94 | 扣费后 EV -0.72% | 胜率 56.2%；`BABA`（中概互联网） | 评分 -2.68 | 扣费后 EV -2.18% | 胜率 49.6%；`AMD`（半导体） | 评分 -4.44 | 扣费后 EV -3.28% | 胜率 43.3%。
- Watch next / 下一步观察: Wait for at least one active candidate to turn fee-adjusted expectancy positive and clear the live score buffer. / 等待至少一只活跃候选的扣费后预期收益转正，并越过实盘评分缓冲区。

## Core Rules / 基本规则

- Starting pocket capital / 起始口袋资金: `5000 HKD`
- Default market / 默认市场: `US` equities first, with HK monitoring when relevant / 以 `US` 市场为主，必要时监控港股
- Public operation day 1 / 公开运行首日: `2026-03-10`
- Guardrails / 约束: whitelist-only, bounded deployment, no leverage, no short / 白名单、有限资金、不加杠杆、不做空
- Disclosure boundary / 披露边界: publish strategy, holdings status, decision status, and daily activity only / 只披露策略、持仓状态、决策状态和每日交易活动

## What This Repo Publishes / 这个仓库公开什么

- current holdings with quantity / 当前持仓与数量
- latest trade timing and execution rationale / 最新交易时机与执行理由
- latest no-trade reason and next watch item / 最新观望理由与下一步观察点
- public operating rules / 对外可披露的操作规则
