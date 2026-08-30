# 指标与业务规则

## 1. 总体原则

所有 Dashboard 指标必须有明确口径，并能下钻到原始数据。

## 2. Project Progress

推荐按任务权重计算：

```text
Progress = Σ(Task Weight × Task Completion) / Σ(Task Weight)
```

避免简单使用“已完成任务数量 / 任务总数量”导致大小任务被同等计算。

## 3. Schedule Variance

```text
Schedule Variance = Current Forecast Date - Baseline Date
```

正值表示相对基线存在延期；负值表示提前。

Actual 完成后，应保留 Actual 与 Baseline 的差异。

## 4. Requirement Closure Rate

基础口径：

```text
Verified Approved Requirement / Approved Requirement
```

如果需要更细粒度，可同时展示 Approved、Implemented、Verified 三个阶段。

## 5. Verification Pass Rate

```text
PASS / Executed Tests
```

BLOCKED 和 NOT RUN 不应计入 Executed Tests，但必须单独展示，避免掩盖验证缺口。

## 6. Issue Closure Rate

```text
Closed Issue / Total Issue
```

同时必须关注 Critical / Major 未关闭数量及 Issue Age。

## 7. Risk Level

基础风险模型：

```text
Risk Score = Probability × Impact
```

再根据组织规则映射为 Low / Medium / High / Critical。

## 8. Project Health

项目健康度应综合：

- Schedule
- Milestone
- Risk
- Issue
- Dependency
- 关键任务阻塞情况

建议输出 Green / Yellow / Red，并要求 Red / Yellow 有明确原因。

## 9. Release Readiness

Release Readiness 不是简单平均分，而应支持“硬性阻塞条件”。例如：

- Critical Issue 未关闭
- 必须验证项未完成
- Qualification 未通过
- 必需文档未批准
- Release Approval 未完成

即使综合评分较高，只要存在硬阻塞条件，也不能判定 READY。

## 10. Upcoming Milestones

Dashboard 默认突出未来 30 / 60 / 90 天关键里程碑，并优先展示：

- Critical Milestone
- At Risk
- Delayed
- 受关键依赖影响的 Milestone

## 11. 异常优先规则

展示层应优先排序：

```text
Critical / Red
  ↓
High / Yellow
  ↓
即将到期
  ↓
正常
```

## 12. 数据下钻规则

所有聚合数字都应能够回到对应原始业务记录。例如：

```text
项目进度 72%
  ↓
阶段进度
  ↓
里程碑
  ↓
任务
```

```text
Critical Issue = 2
  ↓
Issue 列表
  ↓
具体 Issue
  ↓
Root Cause / Action / Owner
```
