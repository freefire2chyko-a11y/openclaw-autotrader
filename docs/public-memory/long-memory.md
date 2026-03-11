# Trading Long Memory / 交易长期记忆

Updated / 更新时间: 2026-03-11 23:55:14 CST (UTC+08:00)

Sanitized durable lessons distilled from repeated trading patterns.
从重复交易模式中提炼的脱敏长期教训。

## What This Page Tracks / 这个页面记录什么

- durable operating lessons that survived repeated observation / 经重复观察后保留下来的长期经验
- evidence count for each lesson / 每条教训的证据次数
- last-seen date and scope / 最近出现日期与作用域

## Lesson Summary / 教训摘要

**Total Lessons / 教训总数**: 4
**Total Evidence Points / 累计证据点**: 4

## cash_reserve_block

**Lesson / 教训**: 现金不足会直接阻断后续决策与轮动，必须保留至少20%机动现金。
**Scope / 作用域**: `portfolio`
**Evidence Count / 证据次数**: 1
**Last Seen / 最后出现**: 2026-03-11
**Dates / 出现日期**: 2026-03-11
**Tags / 标签**: `portfolio:cash, risk:reserve`

## realtime_quote_gate

**Lesson / 教训**: 需要实时行情或明确的开盘状态才能进入实盘决策，缺行情时不要强行交易。
**Scope / 作用域**: `execution`
**Evidence Count / 证据次数**: 1
**Last Seen / 最后出现**: 2026-03-11
**Dates / 出现日期**: 2026-03-11
**Tags / 标签**: `execution:quotes, execution:session`

## fx_split_retry

**Lesson / 教训**: 换汇失败时应优先分批换汇并确认目标币种已到账，再继续股票下单。
**Scope / 作用域**: `execution`
**Evidence Count / 证据次数**: 1
**Last Seen / 最后出现**: 2026-03-11
**Dates / 出现日期**: 2026-03-11
**Tags / 标签**: `execution:fx, execution:sequencing`

## weak_followthrough_buy_RIVN

**Lesson / 教训**: RIVN 最近买入后的延续较弱，除非 EV 和胜率显著改善，否则不要继续追高。
**Scope / 作用域**: `RIVN`
**Evidence Count / 证据次数**: 1
**Last Seen / 最后出现**: 2026-03-11
**Dates / 出现日期**: 2026-03-11
**Tags / 标签**: `symbol:RIVN, market:us, tier:satellite, sector:ev, regime:unknown, context_action:buy, context_purpose:open, ref_type:decision, theme:电动车, theme:高波动, source:backfill, backfill_source:journal_backfill_v1, execution_status:plan_only`
