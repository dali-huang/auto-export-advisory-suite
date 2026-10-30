# 宏观指标来源与取数

核查日：2026-10-30。数据源会修订；不预填当前数值。

| 来源 | 可用信息 | 使用限制 |
|---|---|---|
| 目的国统计局/交通机构 | 实际收入、就业、CPI、车辆注册与保有量 | 优先当地定义；注册/销售/在用存量分别记录 |
| 目的国央行/金融监管机构 | 汇率、利率、信贷、金融统计 | 即期/均值、买卖价、政策利率/车贷APR分开 |
| [World Bank 指标API](https://datahelpdesk.worldbank.org/knowledgebase/articles/898599-indicator-api-queries) | 跨国可比历史指标及元数据 | 更新滞后不同；不得用末次非空值冒充当年值 |
| [IMF WEO 数据](https://data.imf.org/datasets/WEO)与[FAQ](https://www.imf.org/en/Publications/WEO/frequently-asked-questions) | 宏观历史、机构估算和预测 | 保存发布批次；历史项也可能为工作人员估算，不能仅按年份判断 |
| 当地海关 / [UN Comtrade](https://comtradeplus.un.org/) | 进口结构与供给压力 | 不是消费者需求；与海关方法核对 |
| 当地能源监管/公用事业 | 燃油零售、家充/公充电价 | 城市、时段、套餐、税费与用户类型匹配 |

World Bank 可检索代码：`NY.GDP.MKTP.KD.ZG` 实际GDP增长、`NY.GDP.PCAP.CD` 当年美元人均GDP、`FP.CPI.TOTL.ZG` CPI通胀、`PA.NUS.FCRF` 官方汇率。执行时读取指标元数据确认定义及覆盖；人均GDP只作宏观背景。

每次保存 `source_url, dataset, indicator_code, country, unit, period, value, status, release_vintage, retrieved_at, revision_note, raw_file/row`。IMF网页若拒绝访问，可用官方数据门户或官方已发布文件核实，不能以搜索摘要补造缺失值。
