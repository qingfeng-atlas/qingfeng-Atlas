\# SPR-009-TASK-003-Create-COMP-000002-CATL



Version: 1.0



Status: Active



Owner: Project Atlas



Sprint: 009



Created: 2026-07-13



\---



\# 一、任务目标（Objective）



根据 Atlas 最新标准体系，



创建：



companies/COMP-000002-CATL.md



本任务属于：



Create（首次创建）。



目标：



使用最新版：



\- AS-006 Company Lifecycle Standard v1.1

\- AS-007 Repository Governance Standard

\- DM-002 Company Schema

\- TEMPLATE-Company.md



创建 Atlas 第二份正式 Company Asset。



本任务用于验证：



Atlas Company Production Pipeline



是否能够稳定复用于不同上市公司。



生成后的 Company Asset 将与：



COMP-000001-BYD



进行 Benchmark 对比。



\---



\# 二、执行前必须阅读



AI Agent 必须严格按照以下顺序读取：



1\. AGENTS.md



2\. WORKFLOW.md



3\. TASK\_TEMPLATE.md



4\. tasks/README.md



5\. standards/AS-006-Company-Lifecycle-Standard.md



6\. standards/AS-007-Repository-Governance-Standard.md



7\. data-model/DM-002-Company-Schema.md



8\. templates/TEMPLATE-Company.md



9\. companies/COMP-000001-BYD.md（作为 Production Benchmark）



完成阅读后，



确认：



Company Lifecycle Version：



v0.1



默认不得自动升级至：



v0.5



v1.0



v2.0。



\---



\# 三、Production Benchmark



本任务必须以：



COMP-000001-BYD.md



作为 Atlas Company Production Benchmark。



Benchmark 的目的：



不是复制内容。



而是验证：



\- Metadata 是否一致

\- 字段命名是否一致

\- Markdown 结构是否一致

\- Lifecycle 是否一致

\- Production Report 是否一致



除 Company 自身业务信息外，



CATL 必须保持与 BYD 相同的生产标准。



\---

\# 四、修改范围（Scope）



本任务仅允许创建：



```text

companies/COMP-000002-CATL.md

```



允许：



\- 创建新的 Company Asset

\- 使用 TEMPLATE-Company.md 最新模板

\- 填写 Company Lifecycle v0.1 必填字段

\- 建立标准 Metadata

\- 补充可靠来源

\- 使用统一字段命名

\- 使用统一"待核实"占位规则



\---



禁止修改：



```text

constitution/



standards/



data-model/



templates/



tasks/



companies/COMP-000001-BYD.md



events/



relations/

```



禁止：



\- 修改 AS-006

\- 修改 AS-007

\- 修改 DM-002

\- 修改 TEMPLATE-Company

\- 修改 Benchmark（COMP-000001-BYD）

\- 自动 Commit

\- 自动 Push



\---



\# 五、Production Rules（生产规则）



本任务必须严格遵循：



Atlas Company Production Pipeline。



标准流程：



Task



↓



Read Standards



↓



Read Data Model



↓



Read Template



↓



Read Benchmark（BYD）



↓



Create Company



↓



Self Check



↓



Benchmark Check



↓



Production Report



↓



Human Review



\---



\## Company Lifecycle



固定：



Version：0.1



Lifecycle Stage：



Foundation



Lifecycle Status：



Draft



Data Status：



审核中



不得自动升级：



Version 0.5



Version 1.0



Version 2.0



\---



\## Metadata



必须完全采用：



AS-006 v1.1 推荐 Metadata。



包括：



\- Version

\- Lifecycle Status

\- Lifecycle Stage

\- Data Status

\- Verified

\- Company ID

\- Created

\- Last Updated

\- Verified At



Metadata 必须与：



COMP-000001-BYD



保持一致。



\---



\## Field Naming



所有字段名称必须与：



DM-002 Company Schema



完全一致。



不得使用历史字段名称。



统一使用：



\- 成立日期

\- 主行业

\- 细分行业

\- 市场概念

\- 产业角色



\---



\## Placeholder Rule



所有无法确认字段：



统一填写：



待核实



不得使用：



\-



空白



暂无



以后补充



未知（除标准允许）



保持 Atlas 全库一致。



\---



\## Benchmark Rule



CATL 不得复制 BYD 内容。



Benchmark 仅用于验证：



\- Markdown 结构

\- Metadata

\- 字段顺序

\- 生命周期

\- Production Report



业务数据必须全部来自：



CATL 官方公开资料。



不得沿用 BYD 内容。



\---

\# 六、数据来源（Data Sources）



Company Asset 的所有正式数据必须遵循：



AS-003《来源可信度标准》。



推荐来源优先级：



一级来源：



\- 宁德时代官方网站

\- 宁德时代投资者关系

\- 深圳证券交易所

\- 上市公司公告

\- 年报

\- 招股说明书



二级来源：



\- 中国证监会

\- 国务院

\- 国家统计局

\- 行业主管部门



三级来源：



\- 权威媒体

\- 行业协会

\- 国际组织

\- 权威数据库



禁止：



\- 自媒体

\- 论坛

\- 未验证网站

\- AI 推测

\- 无来源内容



所有正式字段必须能够追溯来源。



\---



\# 七、Production Boundary（生产边界）



本任务仅生产：



Company Lifecycle Version 0.1



目标：



建立可信 Company 节点。



不是：



完整研究报告。



\---



\## Version 0.1 必须完成



必须包含：



\- Company ID

\- 股票代码

\- 公司简称

\- 公司全称

\- 英文名称

\- 上市交易所

\- 上市状态

\- 上市日期

\- 成立日期

\- 注册地址

\- 总部所在地

\- 法定代表人

\- 主营业务

\- 核心产品

\- 主行业

\- Atlas 公司简介

\- 官方来源



所有字段必须符合：



DM-002 Company Schema。



\---



\## Version 0.1 允许保留



以下字段允许填写：



待核实



例如：



\- 董事长

\- CEO

\- 实际控制人

\- 控股股东

\- 企业性质

\- 收入来源

\- 客户类型

\- 商业模式

\- 产业链位置

\- 产业角色

\- 市场概念



不得为了完整性编造内容。



\---



\## Version 0.1 禁止生成



不得生成：



\- 财务分析

\- 投资分析

\- 股票推荐

\- 股价预测

\- SWOT 分析

\- 行业竞争分析

\- 盈利预测

\- AI 主观判断



Atlas Company Asset：



回答：



这家公司是谁？



做什么？



靠什么赚钱？



而不是：



这家公司值不值得买。



\---



\## Atlas 公司简介



简介控制在：



300 字以内。



回答：



1\. 公司是谁？



2\. 主要业务是什么？



3\. 核心产品是什么？



4\. 最近值得关注什么？



禁止：



情绪化表达。



禁止：



投资建议。



禁止：



预测未来。



\---



\# 八、Benchmark Validation（基准验证）



创建完成后，



AI Agent 必须对照：



COMP-000001-BYD.md



验证以下内容：



□ Metadata 一致



□ 标题层级一致



□ 字段顺序一致



□ 生命周期一致



□ 占位规则一致



□ Production Report 格式一致



Benchmark 仅验证：



生产质量。



不得复制：



任何业务内容。



Benchmark 不参与知识来源。



\---

\# 九、Self Check（生产自检）



Company Asset 创建完成后，



AI Agent 必须先完成 Self Check。



不得直接进入 Human Review。



\---



\## Structure Check



确认：



□ Metadata 完整



□ Markdown 标题层级正确



□ Company ID 正确



□ 文件命名正确



□ Lifecycle Version 正确



□ Lifecycle Status 正确



□ Data Status 正确



\---



\## DM-002 Check



确认：



□ 身份信息完整



□ 主营业务完整



□ 主行业完整



□ Atlas 公司简介完成



□ 官方来源存在



\---



\## Production Boundary Check



确认：



未生成：



□ 财务分析



□ 投资建议



□ 股价预测



□ SWOT



□ 主观判断



□ 无来源内容



\---



\## Placeholder Check



确认：



所有无法确认字段：



统一填写：



待核实



不得出现：



空白



\-



暂无



以后补充



未知（除标准允许）



\---



\# 十、Production KPI（生产质量指标）



每个 Company Asset 必须输出：



\## Field Completion



字段完成率。



统计：



Version 0.1 必填字段完成情况。



\---



\## Verified Fields



已确认字段数量。



仅统计：



拥有可靠来源的字段。



\---



\## Pending Fields



待核实字段数量。



允许存在。



不得视为错误。



\---



\## Source Coverage



来源覆盖率。



统计：



已确认字段中，



拥有可靠来源字段占比。



\---



\## Standard Compliance



检查：



□ DM-002



□ AS-006



□ AS-007



□ TEMPLATE



全部符合：



PASS



否则：



FAIL



\---



\# 十一、Benchmark KPI（基准一致性）



对照：



COMP-000001-BYD



检查：



□ Metadata 一致



□ 标题层级一致



□ 字段顺序一致



□ Lifecycle 一致



□ Placeholder 一致



□ Production Report 一致



Benchmark Result：



PASS



或



CHANGES REQUESTED



\---



\# 十二、Company Production Report



完成后必须输出：



《Company Production Report》



至少包括：



1\. 修改文件



2\. Production Version



3\. Lifecycle Version



4\. Lifecycle Status



5\. Data Status



6\. Field Completion



7\. Verified Fields



8\. Pending Fields



9\. Source Coverage



10\. Standard Compliance



11\. Benchmark Result



12\. Review Result



13\. 修改说明



14\. 后续建议



不得省略。



\---

\# 十三、Definition of Done（完成标准）



本任务完成后，必须同时满足以下条件：



\## Asset Quality



□ Company Asset 已按 TEMPLATE-Company.md 创建



□ 所有 Version 0.1 必填字段已完成或标记为"待核实"



□ Metadata 符合 AS-006 v1.1



□ 字段命名符合 DM-002



□ Markdown 结构规范



\---



\## Source Quality



□ 所有正式字段具有可靠来源



□ 来源符合 AS-003 来源可信度标准



□ 无无法验证事实



□ 无 AI 主观推测



\---



\## Standard Compliance



□ 符合 AS-006 Company Lifecycle Standard



□ 符合 AS-007 Repository Governance Standard



□ 符合 DM-002 Company Schema



□ 符合 TEMPLATE-Company.md



\---



\## Benchmark Compliance



□ 与 COMP-000001-BYD 保持一致的 Metadata 结构



□ 与 Benchmark 保持一致的 Markdown 层级



□ 与 Benchmark 保持一致的字段顺序



□ 与 Benchmark 保持一致的 Production Report 格式



不得复制：



任何 Benchmark 业务内容。



\---



\## Production Quality



□ 已完成 Self Check



□ 已完成 Benchmark Validation



□ 已输出 Company Production Report



□ 已完成 Human Review



□ 已完成 Review Fix（如需要）



\---



只有全部满足：



Definition of Done



任务才允许结束。



\---



\# 十四、Git Rules



本任务完成后：



禁止：



自动 Commit。



禁止：



自动 Push。



禁止：



自动 Merge。



完成 Review 后：



等待人工确认。



确认后：



Commit



↓



Push



↓



更新 Sprint 状态。



\---



\# 十五、版本记录（Change Log）



\## Version 1.0



首次建立 Atlas Company Create Task。



定义：



\- Company Create Workflow

\- Production Rules

\- Production Boundary

\- Benchmark Validation

\- Self Check

\- Production KPI

\- Benchmark KPI

\- Company Production Report

\- Definition of Done



作为 Atlas 新建 Company Asset 的标准生产任务模板。



\---



End.

