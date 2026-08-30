# 信息架构与展示设计

## 1. 原则

原始数据不是主要阅读对象。系统应通过分析和展示把业务事实转换成人可以快速理解的状态、趋势、异常和决策信息。

```text
业务数据
  ↓
指标计算 / 分析
  ↓
Dashboard / Roadmap / Timeline / Kanban / Matrix
  ↓
管理决策
```

## 2. Executive Dashboard

回答：公司整体现在怎么样？

### KPI

- 产品总数
- 开发项目数
- 进行中项目数
- 高风险项目数
- Critical Issue 数
- 需求完成率
- 验证通过率
- 项目按期率
- Release Readiness

### 主要区域

1. Product Roadmap
2. Project Health
3. Upcoming Milestones
4. Top Risks
5. Critical Issues
6. 近期重大 Change

## 3. Product Dashboard

回答：这个产品怎么样？

展示：

- Product Status
- Lifecycle Stage
- Current Version
- Target Release
- Product Owner
- Target Market
- Requirement Completion
- Specification Status
- Verification Status
- Related Projects
- Version History
- Release Status

## 4. Project Dashboard

回答：这个项目现在怎么样？

顶部重点展示：

- Project Health
- Overall Progress
- Schedule Variance
- Open Issue
- High Risk
- Upcoming Milestone

主体展示：

- Project Timeline
- Phase Progress
- Milestone Timeline
- Task Progress
- Critical Dependencies
- Top Risks
- Top Issues
- Recent Changes

## 5. Requirement / Traceability Dashboard

回答：产品定义的东西到底有没有实现并验证？

展示：

- Total Requirement
- Approved
- Implemented
- Verified
- Open
- Requirement → Specification → Verification → Version → Release 追踪链

## 6. Verification Dashboard

回答：验证到底做得怎么样？

展示：

- Total Tests
- PASS
- FAIL
- BLOCKED
- NOT RUN
- Pass Rate
- Coverage
- Regression 状态
- 按模块/功能的验证结果

## 7. Risk Dashboard

回答：现在最危险的事情是什么？

展示：

- Risk Heatmap
- Top Risks
- Probability
- Impact
- Risk Level
- Owner
- Mitigation
- Due Date

异常优先，不需要默认展示全部风险原始记录。

## 8. Issue Dashboard

回答：现在有哪些严重问题？

展示：

- Critical / Major / Minor
- Open / Fixing / Verification / Closed
- Issue Age
- Owner
- Affected Milestone
- Affected Version
- Top Critical Issues

## 9. Change Dashboard

回答：这次变更会带来多大影响？

展示 Change Impact：

- 影响 Requirement 数
- 影响 Specification 数
- 影响 Task 数
- 影响 Verification 数
- 影响 Milestone 数
- Schedule Impact
- Risk Impact
- Approval Status

## 10. Release Readiness

回答：当前版本能不能正式发布？

建议从以下维度形成综合判断：

- Requirement
- Verification
- Critical Issue
- Qualification
- Documentation
- Approval

最终显示：READY / CONDITIONALLY READY / NOT READY，并列出阻塞原因。

## 11. Execution Board

回答：工程师现在做什么？

采用任务状态视图：

```text
TO DO | DOING | BLOCKED | DONE
```

重点突出：

- 我的任务
- 临近截止任务
- Blocked Task
- 高优先级任务

## 12. 页面设计原则

### 从总到细

Executive → Product → Project → Object Detail。

### 异常优先

红色/黄色异常应优先于正常数据。

### 指标必须可追溯

Dashboard 上的数字必须能够下钻到原始业务记录。

### 页面不复制数据库

不要把所有字段直接堆在页面上；页面应根据角色和业务问题选择信息。
