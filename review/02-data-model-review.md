# 数据模型评审记录

## 评审目标

验证数据模型能否承载已经确定的业务闭环，并避免为了某个平台提前过度设计。

## 核心结论

1. Product、Project、Requirement、Specification、Verification、Risk、Issue、Change、Version、Release 等核心实体必须独立建模。
2. 业务关系比具体字段实现更重要。
3. 产品、项目和研发治理数据需要形成可追踪关系。
4. Baseline / Forecast / Actual 必须分开保存。
5. 关键 Dashboard 指标必须能下钻到原始记录。
6. 后续落地平台可以重新设计字段，但不得破坏业务语义和核心追踪链。

## 当前评审状态

**数据模型基线：通过。**
