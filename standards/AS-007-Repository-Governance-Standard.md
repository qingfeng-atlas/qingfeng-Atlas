\# AS-007 Repository Governance Standard



Version: 1.0



Status: Draft



Owner: Project Atlas



Created: 2026-07-13



Last Updated: 2026-07-13



\---



\# 一、目的（Purpose）



本标准用于定义 Atlas Repository（仓库）的组织结构、治理原则、协作流程和维护规范。



随着 Atlas 从文档项目逐步发展为知识资产生产平台，仓库将持续增加新的标准、数据模型、模板、知识资产、AI Agent、自动化工具和生产任务。



为了保证长期可维护性、一致性和可扩展性，需要建立统一的 Repository Governance Standard。



本标准适用于：



\- 所有 Repository 目录

\- 所有 Markdown 文档

\- 所有标准（Standards）

\- 所有数据模型（Data Models）

\- 所有模板（Templates）

\- 所有知识资产（Knowledge Assets）

\- 所有 Task

\- 所有 AI Agent

\- 所有开发者



\---



\# 二、治理目标（Objectives）



AS-007 的目标包括：



1\. 明确每个目录的职责，避免目录用途混乱。



2\. 建立统一的文件生命周期管理机制。



3\. 建立统一的 Git Workflow。



4\. 建立统一的 Commit Policy。



5\. 建立统一的 AI Agent 权限模型。



6\. 建立统一的 Repository Review 流程。



7\. 保证 Atlas Repository 能够长期演进，而不会因规模扩大而失去可维护性。



\---



\# 三、核心治理原则（Governance Principles）



Atlas Repository 必须遵循以下原则：



\## 1. Structure First



目录结构必须先于内容扩展。



任何新增目录，都必须首先明确职责。



\---



\## 2. Asset First



Repository 的核心目标是生产知识资产，而不是积累文档。



标准、模板和任务，都是为知识资产服务。



\---



\## 3. Single Source of Truth（SSOT）



任何信息只能存在一个权威来源。



不得在多个文件中维护同一规则。



\---



\## 4. Review Before Merge



所有重要修改必须经过 Review。



未经 Review，不得进入正式版本。



\---



\## 5. Stability Before Expansion



优先保证现有结构稳定，再增加新的模块。



禁止为了新增功能破坏已有体系。



\---

\# 四、Repository Structure（仓库结构）



Atlas Repository 采用职责分离（Responsibility Separation）的组织方式。



每个目录只能承担一种主要职责。



不得出现多个目录承担相同职责。



\---



\## constitution/



职责：



Atlas 的最高治理文件。



包括：



\- Atlas Constitution

\- 核心理念

\- 长期使命

\- 基本原则



特点：



整个 Repository 最稳定的部分。



修改频率最低。



权限：



仅允许人工修改。



AI Agent 默认禁止修改。



\---



\## standards/



职责：



Atlas Standards（AS）。



定义：



\- 标准

\- 生命周期

\- 来源规范

\- Review 标准

\- Repository Governance



特点：



属于知识生产规则。



修改频率较低。



允许：



新增 Standard。



禁止：



根据单个 Company 修改 Standard。



\---



\## data-model/



职责：



Data Model（DM）。



定义：



Atlas 所有核心数据模型。



例如：



\- Company Schema

\- Event Schema

\- Relation Schema

\- Industry Schema



特点：



属于 Repository 核心结构。



修改影响整个知识图谱。



权限：



必须经过人工 Review。



不得直接修改正式版本。



\---



\## templates/



职责：



Template。



定义：



知识资产生产模板。



例如：



\- TEMPLATE-Company

\- TEMPLATE-Event

\- TEMPLATE-Relation



特点：



Template 是 AI Agent 默认使用的生产模板。



所有 Asset 必须基于 Template 创建。



禁止：



直接将 Template 当作知识资产保存。



\---



\## companies/



职责：



Company Asset。



保存：



上市公司正式知识资产。



例如：



COMP-000001-BYD.md



COMP-000002-CATL.md



特点：



Repository 的核心资产。



允许：



新增。



更新。



Review。



禁止：



随意删除。



\---



\## events/



职责：



Event Asset。



保存：



Atlas Event。



例如：



重大公告。



重大政策。



重大事故。



重大投资。



所有 Event 必须拥有唯一 Event ID。



\---



\## relations/



职责：



Relation Asset。



保存：



Company 与：



Company



Industry



Policy



Person



Event



之间的关系。



不得保存重复关系。



\---



\## tasks/



职责：



Task。



Task 是 AI Agent 的工作入口。



Task 负责：



告诉 AI：



今天应该完成什么。



Task 不属于长期知识资产。



Task 完成后进入历史记录。



不得作为正式知识资产引用。



\---



\## production/



状态：



Active



职责：



Production Center。



保存：



\- 当前 Sprint

\- 生产状态

\- 资产进度

\- Pipeline 状态

\- Quality Dashboard



Production Center 不保存正式知识资产。



Production Center 只展示生产状态。



\---



\## docs/



职责：



Project Documentation。



保存：



设计文档。



讨论记录。



方案说明。



架构设计。



Docs 不参与知识生产。



\---



\## research/



职责：



Research。



保存：



调研资料。



行业研究。



历史分析。



实验记录。



Research 属于参考资料。



不得直接作为正式知识来源。

说明：



docs/



负责：



Repository 设计文档。



research/



负责：



行业研究、实验记录和参考资料。



两者职责不得混用。



\---



\## personas/



职责：



Investor Persona。



保存：



投资者画像。



用户画像。



行为模型。



Persona 不属于知识资产。



用于产品设计、AI 交互和用户研究。



\---



\## product/



职责：



Product Design。



保存：



产品规划。



功能设计。



交互设计。



Roadmap。



Product 不保存正式知识资产。



\---



\## meeting/



职责：



Meeting Records。



保存：



会议纪要。



设计讨论。



重要决策。



Meeting 属于项目协作文档。



不得作为正式知识来源。



\---



\## prompts/



状态：



Planned



职责：



Production Prompt。



保存：



AI Prompt。



例如：



Company Production Prompt



Event Production Prompt



Review Prompt



未来：



Claude



GPT



Gemini



Codex



Cursor



统一使用 Prompt 生产知识资产。

说明：



Prompt



定义：



AI 如何完成任务。



Task



定义：



AI 今天需要完成什么任务。



Prompt 提供生产能力。



Task 提供执行授权。



Prompt 与 Task 不得互相替代。



\---





\## scripts/



状态：



Planned



职责：



Automation。



保存：



自动化脚本。



数据转换工具。



批量检查工具。



格式校验工具。



Scripts 不保存业务数据。



\---



\## Repository Design Principle



目录职责必须保持唯一。



新增目录前必须回答：



为什么需要新增？



是否已有目录可以承担？



是否影响现有结构？



任何新增一级目录，都必须同步更新：



AS-007 Repository Governance Standard。



\---

\# 五、File Lifecycle（文件生命周期）



Atlas Repository 中，不同类型文件拥有不同生命周期。



不得使用统一生命周期管理所有文件。



\---



\## Constitution



生命周期：



Draft



↓



Review



↓



Active



↓



Deprecated（极少发生）



特点：



Constitution 是 Repository 的最高治理文件。



原则上长期保持稳定。



\---



\## Standard（AS）



生命周期：



Draft



↓



Review



↓



Active



↓



Deprecated



特点：



Standard 定义生产规则。



允许持续迭代。



必须保留版本历史。



\---



\## Data Model（DM）



生命周期：



Draft



↓



Review



↓



Active



↓



Migration



↓



Deprecated



特点：



Data Model 影响整个知识体系。



修改必须兼容已有 Asset。



禁止随意删除字段。



\---



\## Template



生命周期：



Draft



↓



Review



↓



Active



↓



Superseded



↓



Deprecated



特点：



Template 属于生产模板。



新版本发布后：



旧版本允许保留。



不得覆盖历史版本。



\---



\## Knowledge Asset



包括：



Company



Event



Relation



Industry



Policy



Person



生命周期：



Draft



↓



Review



↓



Active



↓



Archived（如需要）



特点：



Knowledge Asset 是 Repository 最重要的数据。



允许持续完善。



不得删除历史事实。



\---



\## Task



生命周期：



Created



↓



Running



↓



Completed



↓



Archived



特点：



Task 属于生产过程。



不是正式知识资产。



Task 完成后：



进入历史记录。



不参与知识查询。



\---



\## Research



生命周期：



Draft



↓



Reference



↓



Archived



特点：



Research 属于参考资料。



不得直接引用为正式事实。



\---



\# 六、Git Workflow



Atlas Repository 采用：



Review First Workflow。



标准流程：



Task



↓



AI Agent Execute



↓



Execution Report



↓



Human Review



↓



Review Comment



↓



AI Fix



↓



Review Fix Report



↓



Approve



↓



Commit



↓



Push



\---



任何 Standard、



Template、



Data Model、



Knowledge Asset，



都必须经过：



Review



才能进入正式版本。



\---



禁止：



修改完成立即 Commit。



禁止：



未经 Review Push。



禁止：



绕过 Review 流程。



\---



Repository 所有 Git 历史必须保持可追溯。



不得：



删除 Git History。



不得：



强制覆盖历史版本。



不得：



修改已经发布的历史事实。



\---

\# 七、Commit Policy（提交规范）



Atlas Repository 的所有提交必须遵循统一的 Commit Policy。



Commit 的目标不是保存修改。



Commit 的目标是保存经过 Review 的知识资产。



\---



\## 可直接 Commit



以下类型允许在完成 Review 后提交：



\- Standard（AS）

\- Data Model（DM）

\- Template

\- Company Asset

\- Event Asset

\- Relation Asset

\- Industry Asset

\- Policy Asset



\---



\## 默认不 Commit



以下内容默认不进入正式版本：



\- 临时文件

\- Scratch

\- Draft Notes

\- 临时测试文件

\- IDE 配置文件

\- 系统缓存文件



如确需保留，应放入专门目录，并说明用途。



\---



\## Task 提交原则



Task 属于生产过程。



默认允许保留历史记录，但不得作为知识资产引用。



Task 的价值在于：



记录：



为什么执行。



执行了什么。



发现了什么。



不是 Repository 的最终成果。



\---



\## Commit Message



推荐格式：



Type: Summary



例如：



Standard: Update AS-007 Repository Governance



Template: Upgrade Company Template v1.1



Company: Create COMP-000002-CATL



Review: Fix AS-006 Review Comments



所有 Commit 应能够说明：



修改对象。



修改原因。



影响范围。



\---



\# 八、AI Agent Governance（AI Agent 治理）



Atlas Repository 默认遵循：



Least Privilege Principle（最小权限原则）。



AI Agent 只能执行 Task 授权范围内的工作。



\---



\## 默认允许



AI Agent 可以：



\- 创建 Company Asset

\- 更新 Template（Task 授权）

\- 在 Task 授权范围内更新 Task

\- 生成 Review Report

\- 生成 Analysis Report



\---



\## 默认禁止



AI Agent 不得：



\- 修改 Constitution

\- 删除 Company Asset

\- 删除 Event

\- 删除 Relation

\- 删除 Standard

\- 修改 Data Model

\- 修改 Repository Structure

\- 批量 Rename 文件

\- 自动 Commit

\- 自动 Push

\- 超出 Task 授权范围修改 Task



除非 Task 明确授权。



\---



\## 权限异常



当权限不足时：



AI Agent 必须：



停止执行。



输出异常报告。



等待人工确认。



禁止绕过权限限制。



AI Agent 不得自行扩大权限范围。



任何超出 Task 授权的操作，



必须等待人工确认。



\---





\# 九、Review Governance（Review 治理）



Review 是 Atlas Repository 的核心质量控制机制。



所有重要修改都必须经过 Review。



\---



\## Review 类型



包括：



Structure Review



Content Review



Source Review



Standard Review



Template Review



Repository Review



\---



\## Review Checklist



Review 至少检查：



□ Repository Structure



□ Markdown Structure



□ Standard Compliance



□ Data Model Compliance



□ Template Compliance



□ Source Reliability



□ Lifecycle Status



□ Data Status



□ Naming Convention



□ File Naming



□ Git Scope



\---



\## Review Outcome



Review 结果允许：



Approved



Changes Requested



Rejected



未经 Approved：



不得进入正式版本。



\---

\# 十、Repository Evolution（仓库演进）



Atlas Repository 是一个长期演进的知识工程。



Repository 的扩展必须遵循：



稳定优先（Stability First）。



任何新增模块，都必须回答以下问题：



1\. 为什么需要新增？



2\. 是否已有目录可以承担？



3\. 是否影响现有 Repository Structure？



4\. 是否需要新增 Standard？



5\. 是否需要新增 Template？



未经 Review：



不得新增一级目录。



任何一级目录新增后：



必须同步更新：



AS-007 Repository Governance Standard。



\---



\## Lightweight Review



以下修改可采用 Lightweight Review：



\- Markdown 排版优化

\- 拼写（Typo）修正

\- 标点修正

\- 链接修正

\- 非结构性说明优化



Lightweight Review：



仍需人工确认。



但可简化 Review Checklist。



禁止：



借助 Lightweight Review



修改：



\- Repository Structure

\- Standard

\- Data Model

\- Template 结构

\- Knowledge Asset 内容



\---





\# 十一、Deprecation Policy（废弃策略）



Repository 中的文件原则上不删除。



对于停止使用的标准、模板或资产：



应采用：



Deprecated



或



Archived



状态。



不得直接删除历史知识。



Repository 必须保留知识演进历史。



任何废弃都必须说明：



\- 废弃原因

\- 替代方案

\- 生效时间



\---



\# 十二、Repository Governance Philosophy（治理理念）



Atlas Repository 不追求：



最大的 Repository。



也不追求：



最多的 Markdown 文件。



Atlas Repository 追求：



长期可信。



结构稳定。



知识可追溯。



持续演进。



Repository 中的：



Standard



Data Model



Template



Task



Knowledge Asset



共同组成 Atlas Knowledge Production System。



所有规则都应服务于：



知识资产生产。



而不是增加管理成本。



\---



\# 十三、版本记录（Change Log）



\## Version 1.0



首次建立 Repository Governance Standard。



定义：



\- Repository Structure

\- File Lifecycle

\- Git Workflow

\- Commit Policy

\- AI Agent Governance

\- Review Governance

\- Repository Evolution

\- Deprecation Policy



作为 Atlas Repository 的工程治理标准。



\---



End.

