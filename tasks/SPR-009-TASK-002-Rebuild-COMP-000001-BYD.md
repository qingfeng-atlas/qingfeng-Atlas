\# SPR-009-TASK-002-Rebuild-COMP-000001-BYD



Version: 1.0



Status: Active



Owner: Project Atlas



Sprint: 009



Created: 2026-07-13



\---



\# 一、任务目标（Objective）



根据 Atlas 最新标准体系，



重新生产：



companies/COMP-000001-BYD.md



本任务不是修订（Update）。



本任务是：



Rebuild（重新生产）。



目标：



使用最新版：



\- AS-006 Company Lifecycle Standard v1.1

\- AS-007 Repository Governance Standard

\- DM-002 Company Schema

\- TEMPLATE-Company.md



重新生成：



Atlas 第一份正式 Company Asset。



生成后的 Company Asset 将作为：



Atlas Company Production Benchmark（生产基准）。



后续所有上市公司资产均应参考该文件。



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



9\. companies/COMP-000001-BYD.md（现有版本，仅用于对比，不得直接复制）



完成阅读后，



确认：



Company Lifecycle Version：



v0.1



默认不得自动升级至：



v0.5



v1.0



v2.0。



\---

\# 三、修改范围（Scope）



本任务仅允许修改：



```text

companies/COMP-000001-BYD.md

```



允许：



\- 重建 Company Asset

\- 调整 Markdown 结构

\- 更新 Metadata

\- 修正字段命名

\- 按 TEMPLATE-Company.md 重新组织内容

\- 补充 v0.1 必填字段

\- 补充可靠来源

\- 统一"待核实"占位规则



\---



禁止修改：



```text

constitution/



standards/



data-model/



templates/



tasks/



events/



relations/

```



禁止：



\- 修改 AS-006

\- 修改 AS-007

\- 修改 DM-002

\- 修改 TEMPLATE-Company

\- 修改 Company ID

\- 修改文件命名规范

\- 自动 Commit

\- 自动 Push



\---



\# 四、Production Rules（生产规则）



本次任务必须按照 Atlas Company Production Pipeline 执行。



标准流程：



Task



↓



Read Standards



↓



Read Data Model



↓



Read Template



↓



Read Existing Company



↓



Rebuild Company



↓



Self Check



↓



Production Report



↓



Human Review



\---



\## Company Lifecycle



本次固定：



Version：0.1



Lifecycle Stage：



Foundation



不得：



自动升级：



Version 0.5



Version 1.0



Version 2.0



\---



\## Metadata



必须使用：



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



不得继续使用旧版 Metadata。



\---



\## Field Naming



所有字段名称必须与：



DM-002 Company Schema



保持一致。



禁止：



成立时间



一级行业



二级行业



所属概念



等历史字段名称。



统一使用：



成立日期



主行业



细分行业



市场概念



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

\# 五、数据来源（Data Sources）



Company Asset 的所有正式数据必须遵循：



AS-003《来源可信度标准》。



推荐来源优先级：



一级来源：



\- 上市公司公告

\- 深圳证券交易所

\- 上海证券交易所

\- 香港交易所

\- 公司官网

\- 年报

\- 招股说明书



二级来源：



\- 国务院

\- 中国证监会

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



\# 六、Production Boundary（生产边界）



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

\- 客户类型

\- 商业模式

\- 产业角色



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



简介应控制在：



300 字以内。



回答：



1\. 公司是谁？



2\. 主要业务是什么？



3\. 核心竞争方向是什么？



4\. 最近值得关注什么？



禁止：



情绪化表达。



禁止：



投资建议。



禁止：



预测未来。



\---

\# 七、Self Check（生产自检）



Company Asset 完成后，



AI Agent 必须先完成自检。



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



没有生成：



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



\# 八、Production KPI（生产质量指标）



每个 Company Asset 都必须输出以下指标：



\## 字段完成率（Field Completion）



计算：



已完成字段 ÷ v0.1 必填字段 ×100%



例如：



94%



\---



\## 来源覆盖率（Source Coverage）



计算：



拥有可靠来源字段 ÷ 已完成字段 ×100%



例如：



100%



\---



\## 待核实字段数量



例如：



7



说明：



待核实不是错误。



Atlas 允许保留未知事实。



\---



\## Standard Compliance



检查：



DM-002



AS-006



Template



全部通过：



PASS



否则：



FAIL



\---



\## Review Result



允许值：



PASS



CHANGES REQUESTED



FAIL



\---



\# 九、Company Production Report



完成后必须输出：



《Company Production Report》



至少包括：



1\. 修改文件



2\. Production Version



3\. Lifecycle Version



4\. Lifecycle Status



5\. Data Status



6\. 字段完成率



7\. 来源覆盖率



8\. 待核实字段数量



9\. Standard Compliance



10\. Review Result



11\. 修改说明



12\. 后续建议



不得省略。



\---

\# 十、Definition of Done（完成标准）



本任务完成后，必须同时满足以下条件：



\## Asset Quality



□ Company Asset 已按 TEMPLATE-Company.md 重建



□ 所有 v0.1 必填字段已完成或标记为“待核实”



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



\## Production Quality



□ 已完成 Self Check



□ 已输出 Company Production Report



□ 已完成 Human Review



□ 已完成 Review Fix（如需要）



\---



只有全部满足：



Definition of Done



任务才允许结束。



\---



\# 十一、Git Rules



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



\# 十二、版本记录（Change Log）



\## Version 1.0



首次建立 Atlas Company Production Task。



定义：



\- Company Rebuild Workflow

\- Production Rules

\- Production Boundary

\- Self Check

\- Production KPI

\- Company Production Report

\- Definition of Done



作为 Atlas Company Asset 的标准生产任务模板。



\---



End.

