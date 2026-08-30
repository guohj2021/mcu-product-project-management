# 核心数据字典

> 本文档定义业务字段基线。具体数据库类型、平台字段命名方式可以在实施阶段映射，不改变业务含义。

## Market

| 字段 | 含义 |
|---|---|
| Market ID | 市场唯一编号 |
| Name | 市场名称 |
| Description | 市场描述 |
| Trend | 市场趋势 |
| Priority | 市场优先级 |
| Owner | 负责人 |
| Status | 状态 |

## Customer

| 字段 | 含义 |
|---|---|
| Customer ID | 客户编号 |
| Name | 客户名称 |
| Market | 所属市场 |
| Segment | 客户类型/细分 |
| Importance | 客户重要度 |
| Owner | 客户负责人 |
| Status | 状态 |

## Opportunity

| 字段 | 含义 |
|---|---|
| Opportunity ID | 机会编号 |
| Name | 机会名称 |
| Customer | 来源客户 |
| Market | 来源市场 |
| Background | 背景 |
| Business Value | 商业价值 |
| Priority | 优先级 |
| Owner | 负责人 |
| Status | 状态 |

## Roadmap

| 字段 | 含义 |
|---|---|
| Roadmap ID | 路线图编号 |
| Product | 规划产品 |
| Target Market | 目标市场 |
| Target Release | 目标发布时间 |
| Priority | 优先级 |
| Status | 状态 |
| Owner | 负责人 |

## Product

| 字段 | 含义 |
|---|---|
| Product ID | 产品唯一编号 |
| Product Name | 产品名称 |
| Product Family | 产品系列 |
| Roadmap | 所属路线图 |
| Market | 目标市场 |
| Core Features | 核心特性 |
| Product Owner | 产品负责人 |
| Current Version | 当前版本 |
| Target Release | 目标发布 |
| Status | 产品状态 |
| Lifecycle Stage | 生命周期阶段 |

## Requirement

| 字段 | 含义 |
|---|---|
| Requirement ID | 需求编号 |
| Product | 所属产品 |
| Source | 来源 |
| Customer | 来源客户 |
| Type | 需求类型 |
| Description | 需求描述 |
| Priority | 优先级 |
| Owner | 负责人 |
| Status | 状态 |
| Baseline | 需求基线 |
| Target Version | 目标版本 |

## Specification

| 字段 | 含义 |
|---|---|
| Specification ID | 规格编号 |
| Product | 所属产品 |
| Requirement | 来源需求 |
| Item | 规格项 |
| Target | 目标值 |
| Min / Max | 范围 |
| Unit | 单位 |
| Tolerance | 容差 |
| Status | 状态 |
| Owner | 负责人 |

## Project

| 字段 | 含义 |
|---|---|
| Project ID | 项目编号 |
| Product | 关联产品 |
| Objective | 项目目标 |
| PM | 项目经理 |
| Technical Lead | 技术负责人 |
| Start Date | 开始日期 |
| Baseline End | 基线结束日期 |
| Forecast End | 当前预测结束日期 |
| Actual End | 实际结束日期 |
| Progress | 项目进度 |
| Health | 健康度 |
| Status | 状态 |

## Phase

| 字段 | 含义 |
|---|---|
| Phase ID | 阶段编号 |
| Project | 所属项目 |
| Name | 阶段名称 |
| Sequence | 顺序 |
| Start Date | 开始日期 |
| Baseline End | 基线结束 |
| Forecast End | 预测结束 |
| Actual End | 实际结束 |
| Progress | 进度 |
| Status | 状态 |

## Milestone

| 字段 | 含义 |
|---|---|
| Milestone ID | 里程碑编号 |
| Project | 所属项目 |
| Phase | 所属阶段 |
| Name | 里程碑名称 |
| Baseline Date | 基线日期 |
| Forecast Date | 预测日期 |
| Actual Date | 实际日期 |
| Criticality | 重要程度 |
| Status | 状态 |

## Task

| 字段 | 含义 |
|---|---|
| Task ID | 任务编号 |
| Project | 所属项目 |
| Phase | 所属阶段 |
| Milestone | 关联里程碑 |
| Name | 任务名称 |
| Owner | 执行人 |
| Weight | 权重 |
| Start Date | 开始日期 |
| Due Date | 截止日期 |
| Progress | 完成度 |
| Status | 状态 |
| Blocked | 是否阻塞 |

## Verification

| 字段 | 含义 |
|---|---|
| Verification ID | 验证编号 |
| Requirement | 对应需求 |
| Specification | 对应规格 |
| Product Version | 产品版本 |
| Test Type | 测试类型 |
| Result | PASS / FAIL / BLOCKED / NOT RUN |
| Coverage | 覆盖率 |
| Owner | 负责人 |
| Execution Date | 执行日期 |

## Issue

| 字段 | 含义 |
|---|---|
| Issue ID | 问题编号 |
| Product / Project | 关联对象 |
| Title | 问题标题 |
| Severity | 严重程度 |
| Status | 状态 |
| Owner | 负责人 |
| Found Date | 发现日期 |
| Due Date | 计划关闭日期 |
| Affected Version | 影响版本 |
| Affected Milestone | 影响里程碑 |
| Root Cause | 根因 |
| Resolution | 解决方案 |

## Risk

| 字段 | 含义 |
|---|---|
| Risk ID | 风险编号 |
| Product / Project | 关联对象 |
| Description | 风险描述 |
| Probability | 发生概率 |
| Impact | 影响程度 |
| Risk Level | 风险等级 |
| Owner | 负责人 |
| Mitigation | 缓解措施 |
| Trigger | 触发条件 |
| Due Date | 处理期限 |
| Status | 状态 |

## Change

| 字段 | 含义 |
|---|---|
| Change ID | 变更编号 |
| Product / Project | 关联对象 |
| Request | 变更内容 |
| Reason | 变更原因 |
| Impact | 影响分析 |
| Schedule Impact | 计划影响 |
| Risk Impact | 风险影响 |
| Approval Status | 审批状态 |
| Owner | 负责人 |
| Status | 状态 |

## Decision

| 字段 | 含义 |
|---|---|
| Decision ID | 决策编号 |
| Context | 背景 |
| Options | 候选方案 |
| Decision | 最终决定 |
| Rationale | 决策依据 |
| Decision Maker | 决策人 |
| Date | 决策日期 |
| Related Review | 关联评审 |

## Review

| 字段 | 含义 |
|---|---|
| Review ID | 评审编号 |
| Type | 评审类型 |
| Subject | 评审对象 |
| Date | 评审日期 |
| Participants | 参与人 |
| Result | 评审结果 |
| Decision | 关键决定 |
| Action Items | 行动项 |
| Status | 状态 |

## Version

| 字段 | 含义 |
|---|---|
| Version ID | 版本编号 |
| Product | 所属产品 |
| Version Name | 版本名称 |
| Change Summary | 变化摘要 |
| Related Issue | 关联问题 |
| Related Change | 关联变更 |
| Verification Status | 验证状态 |
| Status | 版本状态 |

## Release

| 字段 | 含义 |
|---|---|
| Release ID | 发布编号 |
| Product | 所属产品 |
| Version | 发布版本 |
| Target Date | 目标日期 |
| Actual Date | 实际日期 |
| Readiness | 发布准备度 |
| Approval | 发布批准 |
| Status | 发布状态 |

## Lifecycle

| 字段 | 含义 |
|---|---|
| Product | 产品 |
| Stage | 生命周期阶段 |
| Entry Date | 进入日期 |
| Exit Date | 退出日期 |
| Status | 状态 |
| Owner | 负责人 |

## Baseline

| 字段 | 含义 |
|---|---|
| Baseline ID | 基线编号 |
| Object | 基线对象 |
| Version | 基线版本 |
| Approved Date | 批准日期 |
| Approver | 批准人 |
| Status | 状态 |

## Dependency

| 字段 | 含义 |
|---|---|
| Dependency ID | 依赖编号 |
| Source | 依赖发起对象 |
| Target | 被依赖对象 |
| Type | 依赖类型 |
| Criticality | 关键程度 |
| Owner | 负责人 |
| Status | 状态 |

## Action Item

| 字段 | 含义 |
|---|---|
| Action ID | 行动项编号 |
| Source | 来源评审/问题/决策 |
| Description | 行动内容 |
| Owner | 负责人 |
| Due Date | 截止日期 |
| Status | 状态 |
