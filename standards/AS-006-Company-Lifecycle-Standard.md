# AS-006 Company Lifecycle Standard

Version: 1.1

Status: Active

Owner: Project Atlas

Created: 2026-07-13

Last Updated: 2026-07-13

---

# 一、目的

本标准用于定义 Atlas 中 Company（上市公司）知识资产的生命周期管理规则。

DM-002 定义 Company 的完整数据结构。

AS-006 定义 Company 从创建、完善、验证到持续维护的阶段规则。

Atlas 不追求一次性完成完整公司档案。

Atlas 采用：

> Progressive Knowledge Construction

（渐进式知识构建）

通过多个阶段不断完善公司知识资产。

---

# 二、核心原则

## 1. 先入库，再完善

Atlas 允许 Company Asset 分阶段建设。

最低可用信息满足要求后，即可进入 Atlas 的人工 Review 流程。

---

## 2. 不追求完整，但必须真实

允许：

- 信息缺失
- 字段待核实
- 后续阶段再补充

禁止：

- 错误信息
- 无来源事实
- 推测性结论

原则：

> 宁可缺失，不可错误。

---

## 3. 生命周期驱动

每家公司都有明确生命周期版本。

Company Asset 不是静态文件。

Company Asset 是持续演化的知识实体。

---

## 4. 数据模型不降级

DM-002 是 Company 的完整数据模型。

AS-006 只定义分阶段生产规则。

不得因为某个阶段暂不填写字段，而删除、弱化或改变 DM-002 的完整字段要求。

---

# 三、状态体系

Company Asset 必须区分：

- Lifecycle Status
- Data Status

禁止使用同一个 Status 同时表示生命周期状态和数据质量状态。

---

## 1. Lifecycle Status

Lifecycle Status 表示 Company Asset 的生命周期状态。

允许值：

- Draft
- Review
- Active
- Deprecated

---

### Draft

表示：

Company Asset 已创建，基础结构完成，尚未完成人工审核。

适用场景：

- AI Agent 初次创建 Company Asset
- 文件仍需人工检查字段、来源和结构

---

### Review

表示：

AI Agent 已完成生成或整理，进入人工验证阶段。

适用场景：

- 结构检查已完成
- 来源初步补齐
- 等待人工确认事实准确性

---

### Active

表示：

Company Asset 已经通过人工 Review，正式进入 Atlas 知识库。

---

### Deprecated

表示：

历史资产或失效资产，不再作为当前有效数据使用。

Deprecated 文件不得直接删除。

---

## 2. Data Status

Data Status 表示 Company 数据质量状态。

Data Status 只描述数据可靠程度。

Data Status 不能代表 Company Asset 生命周期。

允许值：

- 最新
- 部分过期
- 已过期
- 审核中
- 未知

---

### 最新

表示：

关键字段已根据当前可用来源完成验证。

---

### 部分过期

表示：

部分字段可能不再反映最新情况，但仍有历史参考价值。

---

### 已过期

表示：

主要字段已不适合作为当前事实使用，需要重新验证。

---

### 审核中

表示：

数据正在人工 Review 或来源核验过程中。

---

### 未知

表示：

当前无法判断数据质量状态。

---

# 四、Company 文件顶部状态标记

Company 文件顶部必须记录生命周期信息。

推荐格式：

```yaml
Company ID: COMP-000001
Company Lifecycle Version: 0.1
Lifecycle Status: Draft
Lifecycle Stage: Foundation
Data Status: 审核中
Created: 2026-07-13
Last Updated: 2026-07-13
Verified: 待核实
```

说明：

- Company Lifecycle Version 表示当前生命周期版本。
- Lifecycle Status 表示资产生命周期状态。
- Lifecycle Stage 表示生命周期阶段名称。
- Data Status 表示数据质量状态。
- Verified 表示最近一次人工验证时间。

禁止：

- 使用 Status 同时表示 Lifecycle Status 和 Data Status
- 将 Data Status 写成 Draft、Review、Active、Deprecated
- 将 Lifecycle Status 写成 最新、部分过期、已过期、审核中、未知

---

# 五、Company Lifecycle Version

Company Lifecycle Version 用于定义 Company Asset 的分阶段建设边界。

AI Agent 创建 Company Asset 时，必须先确认目标生命周期版本。

如任务未指定目标版本，默认创建：

Company Lifecycle Version 0.1

---

## Version 0.1：基础入库阶段

目标：

建立可信 Company 节点。

适用于：

- 首次创建 Company Asset
- 建立最小可验证公司身份
- 为后续业务认知和关系图谱建设提供基础

---

### 必须包含

Version 0.1 必须包含：

- Company ID
- 股票代码
- 公司简称
- 公司全称
- 上市交易所
- 上市状态
- 主营业务
- 主行业
- 官方来源

说明：

- 公司简称、公司全称、上市交易所必须保持与 DM-002 Company Schema 一致。
- 官方来源优先使用上市公司公告、交易所公告、公司官网、年度报告或招股说明书。

---

### 可以包含

Version 0.1 可以包含但不强制要求：

- 英文名称
- 上市日期
- 成立日期
- 注册地址
- 总部所在地
- 法定代表人
- 一句话公司介绍

前提：

必须有可追溯来源。

---

### 不要求

Version 0.1 不要求：

- 财务快照
- 风险分析
- 竞争分析
- 完整管理层记录
- 完整事件时间轴
- 完整关系网络
- 承诺兑现体系

---

### 禁止

Version 0.1 禁止：

- 无来源扩展
- 主观风险判断
- 投资建议
- 股价预测
- 将概念板块代替主营业务
- 一次性生成完整研究报告

---

## Version 0.5：企业认知阶段

目标：

让普通投资者理解这家公司如何经营。

在 Version 0.1 基础上增加：

- 商业模式
- 产品体系
- 客户类型
- 产业角色
- 核心管理层
- 重要事件关联

---

### 商业模式

回答：

公司如何赚钱？

要求：

- 使用普通投资者能够理解的语言
- 不生成投资建议
- 不预测未来业绩

---

### 产品体系

包括：

- 核心产品
- 服务
- 技术方向

---

### 行业定位

包括：

- 所属行业
- 产业链位置
- 产业角色
- 主要业务领域

---

### 核心管理层

记录：

- 董事长
- 总经理 / CEO
- 其他核心管理人员

管理层信息必须记录来源。

---

### 重要事件关联

仅关联 Event ID。

不得在 Company Asset 中复制完整事件内容。

---

## Version 1.0：完整 Company Asset

目标：

成为 Atlas 标准 Company Asset。

在 Version 0.5 基础上增加：

- 财务快照
- 风险记录
- 承诺兑现
- 发展时间轴

---

### 财务快照

包括：

- 营业收入
- 净利润
- 现金流
- 资产负债
- ROE
- 研发投入

所有财务数据必须记录：

- 财报周期
- 单位
- 数据来源
- 更新时间

---

### 风险记录

风险记录必须来源于可验证事实。

禁止将主观推测写成事实。

---

### 承诺兑现

记录：

- 公司承诺内容
- 关联事件
- 公告时间
- 完成时间
- 当前状态
- 结果
- 证据

---

### 发展时间轴

发展时间轴只保存 Event ID。

不得重复复制 Event 内容。

---

## Version 2.0：知识图谱阶段

目标：

成为 Atlas Knowledge Graph 节点。

在 Version 1.0 基础上增加：

- Relation 网络
- Event 因果关系
- 行业关系
- 政策关系

---

### Relation 网络

连接：

- 公司
- 行业
- 政策
- 人物
- 机构
- 事件
- 产业链

所有 Relation 必须符合 AS-005 Relationship Standard。

---

### Event 因果关系

回答：

- 为什么发生？
- 影响什么？
- 证据是什么？

禁止无来源推断。

---

# 六、版本升级规则

升级必须满足对应条件。

---

## v0.1 -> v0.5

条件：

- 基础信息验证完成
- 主营业务明确
- 主行业明确
- 至少一个可靠来源

---

## v0.5 -> v1.0

条件：

- 商业模式完成
- 产品体系完成
- 客户类型明确
- 产业角色明确
- 核心管理层完成
- 重要事件关联完成

---

## v1.0 -> v2.0

条件：

- 财务快照完成
- 风险记录建立
- 承诺兑现体系建立
- 发展时间轴建立
- Relation 网络建立
- Event 因果关系验证

---

# 七、AI Agent 执行规则

AI Agent 创建或更新 Company Asset 时，必须：

1. 阅读 AGENTS.md。
2. 阅读 WORKFLOW.md。
3. 阅读对应 Task 文件。
4. 阅读 AS-006。
5. 阅读 DM-002。
6. 阅读 TEMPLATE-Company。
7. 确认目标 Company Lifecycle Version。

如果任务未指定目标版本：

默认生成 Company Lifecycle Version 0.1。

---

## 允许

AI Agent 允许：

- 创建任务指定的 Company 文件
- 根据目标生命周期版本补充允许字段
- 将无法确认的信息标记为待核实
- 根据已确认来源修正错误信息

---

## 禁止

AI Agent 禁止：

- 修改 Constitution
- 修改 DM-002
- 修改无关 Standard
- 修改无关 Template
- 修改无关 Company Asset
- 根据单个公司案例降低标准
- 删除未来阶段定义
- 自动 Commit
- 自动 Push
- 编造事实
- 编造来源
- 生成投资建议
- 预测股票价格
- 一次性生成完整研究报告，除非 Task 明确要求目标版本为 v1.0 或以上

---

# 八、待核实字段规范

Company Asset 中所有无法确认的信息，统一填写：

待核实

禁止使用：

- 空白
- -
- 待填写

除非字段允许，否则禁止使用：

未知

---

## 待核实字段使用原则

待核实表示：

- 当前字段需要保留
- 当前事实尚未完成验证
- 后续需要人工或来源补充

待核实不表示：

- 字段不存在
- 字段不适用
- 可以忽略该字段

---

# 九、与 DM-002 的关系

DM-002 是 Company 的完整数据模型。

AS-006 是 Company 的生命周期生产标准。

两者关系：

- DM-002 定义应当记录什么。
- AS-006 定义在什么阶段记录到什么程度。
- TEMPLATE-Company 应根据 DM-002 字段和 AS-006 阶段边界生成。

禁止：

- 使用 AS-006 删除 DM-002 字段
- 使用 AS-006 改名 DM-002 字段
- 使用 AS-006 降低 DM-002 的长期完整性要求

---

# 十、质量优先级

Company Asset 质量排序：

1. 数据真实性
2. 来源可追溯
3. 数据结构正确
4. 可持续维护
5. 信息完整

Atlas 质量原则：

真实性 > 完整性

可验证 > 速度

长期价值 > 短期数量

---

# 十一、权限与修改规则

AI Agent 在处理 Company Asset 时：

允许：

- 创建任务指定的 Company 文件
- 根据标准补充允许字段
- 修正已确认错误信息

禁止：

- 修改 Constitution
- 修改 Standards（除非 Task 明确授权）
- 修改 Data Model（除非 Task 明确授权）
- 修改其他无关资产
- 删除历史数据

未经人工确认，禁止：

- Commit
- Push

所有重大结构变化必须经过人工 Review。

---

# 十二、权限异常处理

当 AI Agent 无法写入目标目录时：

第一步：

停止所有写入操作。

第二步：

输出权限异常报告。

报告必须包含：

- 目标文件路径
- 当前权限状态
- 已完成工作
- 未完成原因

第三步：

等待人工授权。

禁止：

- 绕过权限限制
- 修改系统权限
- 创建临时替代文件
- 复制到其他目录继续执行
- 自动修改 Git 配置

---

# 十三、Company 生命周期理念

Atlas 不建立一次性研究报告。

Atlas 建立持续成长的企业知识资产。

每家公司从：

一个事实节点

开始。

经过：

基础身份确认

↓

业务理解

↓

事件积累

↓

关系连接

↓

知识演化

最终成为：

资本市场知识图谱中的完整实体。

---

# 十四、版本记录（Change Log）

## Version 1.1

更新 Company 生命周期标准。

明确：

- Lifecycle Status 与 Data Status 的区别
- Company Lifecycle Version 0.1 / 0.5 / 1.0 / 2.0 的边界
- AI Agent 默认生成 v0.1 的执行规则
- 待核实字段统一规范
- AS-006 与 DM-002 的关系

---

## Version 1.0

首次建立 Company 生命周期标准。

定义：

- Company 生命周期阶段
- AI Agent 执行规则
- 版本升级机制
- 权限管理规则
- 质量控制标准

---

End.
