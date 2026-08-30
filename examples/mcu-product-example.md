# MCU 产品示例

> 以下数据仅用于演示业务模型，不代表真实产品规格。

## 示例产品

**XXXF407**

- Product Family：XXXF4
- Target Market：Industrial Control
- Lifecycle：Development / Qualification
- Current Version：Rev.B
- Target Release：2026 Q4

## 示例需求

`REQ-USB-001`：产品支持 USB OTG HS。

对应规格包括高速传输能力、Host、Device、OTG 等要求。

## 示例项目

`PRJ-XXXF407`：XXXF407 新产品开发。

主要阶段：

```text
Product Definition
Architecture
RTL Design
Verification
Tape-out
Bring-up
Qualification
Release
```

## 示例风险

`RISK-001`：USB PHY 高温稳定性存在风险。

- Probability：High
- Impact：High
- Level：Critical
- Mitigation：高温条件专项验证

## 示例问题

`ISS-001`：USB HS 在高温测试中出现异常。

状态：Verification。

## 示例变更

`CHG-001`：新增 USB LPM 支持。

影响：Requirement、Specification、RTL、Verification 和 Milestone。

## 示例版本

- Rev.A：初始版本
- Rev.B：修复 USB 相关问题并增加功能

## 示例发布判断

Release Readiness：91%

阻塞条件示例：Critical Issue 未关闭时，即使综合评分较高，也不能直接判定 READY。
