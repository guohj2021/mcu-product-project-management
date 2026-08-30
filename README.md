# MCU Product & Project Management Methodology

面向 MCU / 芯片企业的产品与项目全生命周期管理方法论。

## 项目定位

本项目不是某一种表格工具的模板，而是一套独立于具体工具的业务体系，用于把 MCU 产品从市场机会、产品规划、产品定义、研发项目、验证、质量、风险、变更、版本、发布一直连接到产品生命周期结束。

核心目标：

> 将 MCU 产品研发过程变成一套可追踪、可度量、可预警、可决策、可复盘的数字化业务体系。

## 核心业务链

```text
Market / Customer
        ↓
Opportunity
        ↓
Roadmap
        ↓
Product
        ↓
Requirement
        ↓
Specification
        ↓
Project
        ↓
Phase / Milestone / Task
        ↓
Verification
        ↓
Risk / Issue / Change
        ↓
Version
        ↓
Release
        ↓
Product Lifecycle
        ↓
EOL
```

## 文档结构

- `docs/00-system-overview.md`：系统总体说明
- `docs/01-business-requirements.md`：最终业务需求
- `docs/02-business-process-and-lifecycle.md`：业务流程与生命周期
- `docs/03-data-model.md`：业务数据模型
- `docs/04-data-dictionary.md`：核心数据字典
- `docs/05-information-architecture-and-display.md`：信息架构与展示设计
- `docs/06-roles-and-permissions.md`：角色与权限
- `docs/07-metrics-and-business-rules.md`：指标与业务规则
- `review/01-requirement-review.md`：需求评审与演进记录
- `review/02-data-model-review.md`：数据模型评审记录
- `review/03-display-review.md`：展示方案评审记录
- `examples/mcu-product-example.md`：示例产品数据与展示场景

## 设计原则

1. **业务先于工具**：业务需求不绑定飞书、数据库或其他具体平台。
2. **原始数据与展示分离**：表格/数据结构负责保存事实，Dashboard 负责把事实转换成人可以理解的信息。
3. **围绕决策设计**：页面优先回答“现在怎么样、哪里异常、为什么、谁负责、什么时候解决”。
4. **全链路追溯**：建立 Product → Requirement → Specification → Verification → Version → Release 的追踪链。
5. **计划与实际分离**：保留 Baseline、Current Forecast、Actual，支持延期和偏差分析。
6. **异常优先**：Risk、Issue、Dependency、Change 等异常应在管理页面中优先呈现。
7. **可复盘**：保留 Review、Decision、Change 和历史版本，能够解释关键决策与变化原因。

## 当前状态

业务概念、数据模型、展示层和角色视角正在统一收敛。本仓库作为后续系统实施前的业务基线与评审资料库。