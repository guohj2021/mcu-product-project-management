# 业务流程与生命周期

## 1. 产品生命周期

```text
Concept
  ↓
Product Definition
  ↓
Development
  ↓
Sampling
  ↓
Qualification
  ↓
Mass Production
  ↓
Maintenance
  ↓
EOL
```

## 2. 产品开发主流程

```text
Market / Customer
  ↓
Opportunity
  ↓
Roadmap
  ↓
Product Definition
  ↓
Requirement
  ↓
Specification
  ↓
Architecture
  ↓
Design
  ↓
Verification
  ↓
Tape-out
  ↓
Silicon Bring-up
  ↓
Qualification
  ↓
Release
  ↓
Mass Production
```

## 3. 项目执行流程

```text
Project
  ↓
Phase
  ↓
Milestone
  ↓
Task
  ↓
Dependency
  ↓
Completion
```

## 4. 质量闭环

```text
Requirement
  ↓
Specification
  ↓
Verification
  ↓
PASS / FAIL / BLOCKED
  ↓
Issue
  ↓
Fix
  ↓
Regression
  ↓
Release
```

## 5. 风险闭环

```text
Risk
  ↓
Monitoring / Trigger
  ↓
Issue（如果风险实际发生）
  ↓
Action / Mitigation
  ↓
Close
```

Risk 与 Issue 不等价：Risk 表示可能发生，Issue 表示已经发生。

## 6. 变更闭环

```text
Change Request
  ↓
Impact Analysis
  ↓
Review
  ↓
Approval
  ↓
Implementation
  ↓
Verification
  ↓
Version / Release
```

## 7. 评审流程

```text
Prepare
  ↓
Review
  ↓
Decision
  ↓
Action Items
  ↓
Closure
```

典型评审点包括 PRD Review、Architecture Review、Design Review、Verification Review、Tape-out Review、Release Review。

## 8. 计划基线

关键计划应形成 Baseline。执行过程中同时保存：

- Baseline：批准后的原始计划
- Current Forecast：当前预测
- Actual：实际结果

用于识别 Schedule Variance，并避免通过不断修改计划掩盖历史延期。
