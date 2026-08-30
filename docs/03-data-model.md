# 业务数据模型

## 1. 设计原则

数据模型描述业务事实，不等同于页面。页面应从这些事实计算和组织信息后再展示。

## 2. 核心实体

### 产品业务

- Market：市场
- Customer：客户
- Opportunity：产品机会
- Roadmap：产品路线图
- Product：产品
- Requirement：需求
- Specification：规格
- Version：产品版本
- Release：正式发布
- Lifecycle：产品生命周期

### 项目业务

- Project：项目
- Phase：项目阶段
- Milestone：里程碑
- Task：任务
- Dependency：依赖
- Baseline：计划基线

### 研发治理

- Verification：验证
- Risk：风险
- Issue：问题
- Change：变更
- Decision：决策
- Review：评审
- Action Item：行动项

### 组织辅助

- Organization：组织/团队
- Person：人员
- Document：文档

## 3. 核心关系

```text
Market ──┐
         ├→ Opportunity → Roadmap → Product
Customer ┘                         │
                                   ├→ Requirement → Specification
                                   │                    │
                                   │                    ↓
                                   │              Verification
                                   │                    │
                                   │                    ↓
                                   │                  Issue
                                   │
                                   └→ Project → Phase → Milestone → Task
                                                │          │
                                                └→ Dependency

Project / Product
       ├→ Risk
       ├→ Change → Impact Analysis → Review → Decision
       └→ Version → Release → Lifecycle
```

## 4. 关键追踪链

### 产品价值链

`Market → Customer → Opportunity → Roadmap → Product`

### 需求实现链

`Requirement → Specification → Project → Verification`

### 质量闭环

`Verification → Issue → Fix → Regression → Closure`

### 变更影响链

`Change → Requirement / Specification / Task / Milestone / Risk / Version`

### 发布链

`Requirement → Verification → Version → Release`

## 5. 数据与页面的关系

原始实体用于保存事实；分析层将事实转换为进度、偏差、健康度、风险等级、通过率等指标；展示层再将指标组织成 Dashboard、Roadmap、Timeline、Kanban、Risk Matrix、Traceability 和 Release Readiness。

## 6. 建模边界

- Product 与 Project 必须分离：Product 是要造的东西，Project 是实现它的工作。
- Risk 与 Issue 必须分离：Risk 是可能发生，Issue 是已经发生。
- Version 与 Release 必须分离：Version 描述版本，Release 描述正式发布行为。
- Requirement 与 Specification 必须分离：Requirement 表达需要什么，Specification 表达可执行的产品规格。
- Baseline 与 Forecast 必须分离：Baseline 保存批准计划，Forecast 表示当前预测。
