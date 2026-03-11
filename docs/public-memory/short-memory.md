# Trading Short Memory / 交易短期记忆

Updated / 更新时间: 2026-03-11 23:55:14 CST (UTC+08:00)

Sanitized day-level trading memory exported from Tiger Pocket.
从 Tiger Pocket 导出的脱敏日级交易记忆。

## What You Can Read Here / 这里能看到什么

- daily operating rhythm / 每日运行节奏
- decision and fill counts / 决策与成交次数
- end-of-day equity snapshot / 日终权益快照
- compact lessons surfaced from that day / 当天提炼出的简洁教训

## 2026-03-10

**Summary / 摘要**: 2026-03-10 共 9 次计划、1 次成交、5 次换汇记录，收盘口袋权益 HKD 0.00，未实现盈亏 HKD 0.00。

| Metric / 指标 | Value / 数值 |
| --- | --- |
| Decision Count / 决策次数 | 9 |
| Order Submissions / 提交订单 | 1 |
| Filled Trades / 成交笔数 | 1 |
| FX Events / 换汇记录 | 5 |
| Benchmarks / 基准快照 | 0 |
| Latest Decision / 最新决策 | [US] HOLD 无 |
| End Equity / 结束权益 | HKD 0.00 |
| End Unrealized PnL / 结束未实现盈亏 | HKD 0.00 |

---

## 2026-03-11

**Summary / 摘要**: 2026-03-11 共 57 次计划、3 次成交、6 次换汇记录，对账权益 HKD 4,900.53，对账未实现盈亏 HKD -18.89。

| Metric / 指标 | Value / 数值 |
| --- | --- |
| Decision Count / 决策次数 | 57 |
| Order Submissions / 提交订单 | 1 |
| Filled Trades / 成交笔数 | 3 |
| FX Events / 换汇记录 | 6 |
| Benchmarks / 基准快照 | 15 |
| Latest Decision / 最新决策 | [US] HOLD 无 |
| End Equity / 结束权益 | HKD 4,900.53 |
| End Unrealized PnL / 结束未实现盈亏 | HKD -18.89 |

**Lessons Learned / 提取教训**

- **cash_reserve_block**: 现金不足会直接阻断后续决策与轮动，必须保留至少20%机动现金。
  - Tags / 标签: `portfolio:cash, risk:reserve`

- **realtime_quote_gate**: 需要实时行情或明确的开盘状态才能进入实盘决策，缺行情时不要强行交易。
  - Tags / 标签: `execution:quotes, execution:session`

- **fx_split_retry**: 换汇失败时应优先分批换汇并确认目标币种已到账，再继续股票下单。
  - Tags / 标签: `execution:fx, execution:sequencing`

- **weak_followthrough_buy_RIVN**: RIVN 最近买入后的延续较弱，除非 EV 和胜率显著改善，否则不要继续追高。
  - Tags / 标签: `symbol:RIVN, market:us, tier:satellite, sector:ev, regime:unknown, context_action:buy, context_purpose:open, ref_type:decision, theme:电动车, theme:高波动, source:backfill, backfill_source:journal_backfill_v1, execution_status:plan_only`

---
