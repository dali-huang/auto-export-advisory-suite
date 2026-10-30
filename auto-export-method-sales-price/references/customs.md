# 海关数据源与取数契约

来源核查日：2026-10-30。入口核查不代表已下载目标国数据；每次决策重新查询可用期间及修订。

| 来源 | 用途 | 限制 |
|---|---|---|
| [中国海关统计查询](https://stats.customs.gov.cn/)；[海关政务服务](https://online.customs.gov.cn/) | 中国报告的商品、伙伴、期间进出口 | 可能有交互验证；公开汇总通常不能识别车型配置、品牌、买家或消费者成交价 |
| [UN Comtrade Plus](https://comtradeplus.un.org/) | 各报告国商品贸易与镜像比较 | 报送滞后、修订、覆盖差异；访问额度与下载条件以当次为准 |
| [贸易估值说明](https://uncomtrade.org/docs/trade-valuation/) | FOB/CIF 及国家例外 | 不可假定所有进口都是 CIF |
| [数量与重量说明](https://uncomtrade.org/docs/quantity-and-weight-data-in-un-comtrade/) | 数量标准化和估算 | 官方数据库也可能含估算数量，不等于逐票观测 |
| [补充数量单位](https://uncomtrade.org/docs/supplementary-quantity-units/) | 数量单位核查 | 保留原单位及估算标记；kg 不等于辆 |

目的国海关入口应从该国政府官网确认，不按名称猜 URL。官方平台不可访问时保留失败记录，换官方替代源；商业提单库标明供应商、覆盖和授权，不能称作海关官方全量。

每个数据批次保存：`dataset_id, source_url, publisher, table_or_query, downloaded_at, period, reporter, partner_basis, partner, flow, hs_revision, commodity_code, vehicle_scope, quantity, quantity_unit, value, currency, valuation_basis, estimate_flags, revision_status, raw_file, row_locator`。

保留原始值和转换后值；金额“千美元/万美元/亿元”、数量“辆/万辆”必须先规范单位。文件哈希可用于固化版本。查询 URL 不保存令牌；找不到发布日填“未标明”，不能用下载日冒充。
