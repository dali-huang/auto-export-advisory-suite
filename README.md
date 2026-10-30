# 中国汽车出口国家经理 · 专家顾问团 Skill 套件

> 面向汽车出海国家经理岗位的专家顾问团 Skill 套件：把三位经典专家的心智模型与三本方法论著作蒸馏成可调用的独立 Skill，由总控 Skill 做多视角路由与评审。

## 套件结构

7 个 Skill（3 专家 + 3 方法论 + 1 总控），可独立安装、也可成套使用。

| # | Skill | 定位 | 触发关键词 |
|---|---|---|---|
| 1 | `auto-export-advisor-li-shufu` | 李书福视角：本地伙伴共营与总部借力 | 李书福、Li Shufu、本地伙伴、总部借力、伙伴共营、出口合作 |
| 2 | `auto-export-advisor-ghemawat` | Ghemawat 视角：跨国差异度量与进入/深耕模式取舍 | Ghemawat、盖马沃特、CAGE、AAA、半全球化、国家差异、进入模式、区域协同 |
| 3 | `auto-export-advisor-grove` | Andy Grove 视角：管理产出、战略拐点与数字化业务流 | 格鲁夫、Grove、管理杠杆、经营指标、授权、战略拐点、产出 |
| 4 | `auto-export-method-channels` | 《Marketing Channels》：渠道模式选择、伙伴尽调与激励、多渠道冲突 | 渠道设计、经销商、伙伴经营、总代、代理模式、渠道冲突、伙伴复盘 |
| 5 | `auto-export-method-pricing` | 《定价的战略与战术》：上市定价、折扣返利、TCO 与价值沟通 | 定价、价格瀑布、TCO、价值定价、折扣、贡献、盈亏平衡销量、汇率定价 |
| 6 | `auto-export-method-operations` | 《丰田模式（第二版）》：运营诊断、库存发运、备件售后、滚动经营 | 运营、库存、发运、备件、售后、Toyota Way、滚动经营、持续改善、平准化 |
| 7 | 总控 Skill | 问题路由与多视角评审，输出共识、分歧、条件化建议、责任人与验证指标 | 顾问团、开评审、汽车出海决策 |

> 各 Skill 内部的汽车出口实务改编均显式标注，不冒充专家本人观点或原书规则。

## 安装方式

每个子目录是一个独立、可单独安装的 Skill，可复制到 Agent 的 Skills 目录（Claude Code / Codex / Trae 等），互不依赖。

- 单独安装：将目标子目录（如 `auto-export-advisor-grove/`）复制到对应 Agent 的 Skills 目录。
- 成套使用：建议**先安装总控 Skill**，再按需安装专家与方法论 Skill；总控负责路由，未安装的子 Skill 会在路由时提示缺失。
- 资料文件：每个 Skill 的 `references/` 包含研究底稿或框架源文件，供追溯依据；`references/contemporary-export-methods.md` 是当代出口方法的统一研究底稿。

## 快速上手

### 场景一：单视角问答
**提示词**：「用李书福的视角看，在泰国找总代，总部和国家团队的权责边界该怎么划？」
**预期产出**：以李书福视角给出伙伴互补、权责边界、根基能力三方面的判断，标注事实与推断，并提示当地代理法/数据法规需另行核验。

### 场景二：开评审会（多视角）
**提示词**：「开评审：印尼市场要从 CBU 转 CKD，各顾问怎么看？」
**预期产出**：总控路由李书福（伙伴与长期投入）、Ghemawat（CAGE 距离与进入模式）、Grove（产出与拐点）、渠道/定价/运营方法论分别给意见，最终汇总共识、分歧、关键假设与验证指标。

### 场景三：套用模板出汇报
**提示词**：「用定价方法论，给 X 车型在墨西哥的上市定价出一份决策卡。」
**预期产出**：基于「单次价格决策卡 + 贡献及折扣瀑布」框架，输出成交价口径、竞品替代、经济桥、盈亏平衡销量与情景敏感性，标注税费/汇率为「未核验」。

## 诚实边界

本套件**不覆盖**以下需实时核验的事项，涉及动态事实时一律标注「未核验」并指向官方来源：

- 具体国家的准入法规、关税与非关税壁垒、认证要求
- 信用证条款、外汇管制、贸易救济与电子单证法律效力
- 当地用工合规、数据法规、代理法、召回制度
- 真实销量、库存、授信条件等企业内部数据

AI 可辅助整理与生成情景；公式与数据须可复算，外部执行需明确授权。

## 构建工作流

有兴趣了解套件如何生成，可按以下阶段追溯：

1. **候选名单**（`CANDIDATES.md`）：初选 3 专家 + 3 方法论 + 1 总控，核验语料来源数量与独立性。
2. **调研**：逐条采集一手/署名来源，记录证据与矛盾，达不到门槛则替换。
3. **蒸馏**：每位专家提炼 3 个心智模型 + 7 条决策启发式；每本方法论提炼框架与可执行规则，标注章节来源。
4. **构建**：写入各子目录 `SKILL.md` 与 `references/`；当代出口应用作为独立改编模块，不冒充原书或专家观点。
5. **QA**（`RESEARCH-REVIEW.md`）：审阅范围、核心输出与限制，预置多模型分歧与决策条件。

## 文件结构树

```
auto-export-advisory-suite/
├── README.md                              ← 本文件
├── CANDIDATES.md                          ← 候选名单与语料来源
├── RESEARCH-REVIEW.md                     ← 调研审阅与预置分歧
├── references/
│   └── contemporary-export-methods.md     ← 当代出口方法研究底稿
├── auto-export-advisor-li-shufu/          ← 专家：李书福视角
│   ├── SKILL.md
│   └── references/research.md
├── auto-export-advisor-ghemawat/          ← 专家：Ghemawat 视角
│   ├── SKILL.md
│   └── references/research.md
├── auto-export-advisor-grove/             ← 专家：Andy Grove 视角
│   ├── SKILL.md
│   └── references/research.md
├── auto-export-method-channels/           ← 方法论：Marketing Channels
│   ├── SKILL.md
│   └── references/framework.md
├── auto-export-method-pricing/            ← 方法论：定价的战略与战术
│   ├── SKILL.md
│   └── references/framework.md
└── auto-export-method-operations/         ← 方法论：丰田模式（第二版）
    ├── SKILL.md
    └── references/framework.md
```

---

生成日期：2026-10-14
