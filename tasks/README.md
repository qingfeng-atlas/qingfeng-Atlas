\# Atlas Task System



Version: 1.0



Status: Active



Owner: Project Atlas



Created: 2026-07-13



\---



\# 一、目的



Tasks 是 Project Atlas 中 AI Agent 唯一允许执行工作的入口。



所有 AI Agent 的修改、创建、分析任务，必须通过 Task 文件进行定义。



Task 是连接：



Human Intent（人类意图）



与



AI Execution（AI 执行）



之间的标准接口。



\---



\# 二、核心原则



Atlas Task System 遵循以下原则：



\## 1. 任务驱动



AI Agent 不直接修改仓库。



所有工作必须来源于明确 Task。



\---



\## 2. 范围控制



每个 Task 必须明确：



\- 修改范围

\- 禁止修改范围

\- 执行目标

\- 验收标准



AI Agent 不得主动扩大任务范围。



\---



\## 3. 可追溯



每一次修改必须能够回答：



为什么修改？



修改了什么？



依据是什么？



结果是什么？



\---



\## 4. 人工审核



AI Agent 负责：



\- 分析

\- 创建

\- 修改建议

\- 生成报告



最终：



Commit



和



Push



必须经过人工确认。



\---

\# 三、Task 文件作用





Task 用于定义：



\- 为什么执行任务

\- 任务目标是什么

\- 需要读取哪些规范

\- 允许修改哪些文件

\- 禁止修改哪些文件

\- 执行步骤

\- 验收标准

\- 输出报告格式





Task 不只是任务记录。



Task 是 AI Agent 执行 Atlas 工程工作的唯一授权文件。





\---



\# 四、Task 生命周期





标准流程如下：



Task Created



↓



AI Agent Read Task



↓



Read Required Standards



↓



Execute Task



↓



Generate Execution Report



↓



Human Review



↓



Approve



↓



Commit



↓



Push







\---



\# 五、Task 状态管理





Task 状态允许值：





\## Draft



任务已创建。



尚未执行。





\---





\## Active



任务正在执行。





\---





\## Review



AI Agent 已完成执行。



等待人工审核。





\---





\## Completed



任务已经完成。



并完成必要 Git 操作。





\---





\## Deprecated



任务废弃。



不再继续执行。





\---



\# 六、Task 文件命名规范





所有 Task 文件必须遵循统一命名规则。





格式：





SPR-{Sprint编号}-TASK-{任务编号}-{任务名称}.md





例如：





SPR-008-TASK-001-BYD.md





说明：





SPR：



表示 Sprint 迭代周期。





TASK：



表示任务类型。





编号：



表示当前 Sprint 内任务序号。





名称：



表示任务目标简称。





\---





\# 七、Task 必须包含结构





每个正式 Task 文件必须包含以下章节：





\## 1. 基础信息





包括：





Version



Status



Owner



Sprint



Created



Updated





\---





\## 2. 任务目标（Objective）





说明：





为什么执行该任务。





需要解决什么问题。





最终希望达到什么状态。





\---





\## 3. 执行前阅读（Required Reading）





明确 AI Agent 执行前必须读取的文件。





例如：





AGENTS.md



WORKFLOW.md



TASK\_TEMPLATE.md



相关 Standard



相关 Data Model



相关 Template





\---





\## 4. 修改范围（Scope）





必须明确：





允许修改：





哪些文件可以修改。





禁止修改：





哪些目录和文件不能修改。





\---



\## 5. 执行步骤（Execution Steps）





Task 必须定义明确执行流程。





标准格式：





Step 1



检查当前状态。





Step 2



读取相关标准。





Step 3



执行目标修改。





Step 4



进行结构验证。





Step 5



生成执行报告。





AI Agent 不得跳过关键步骤。





\---





\## 6. 验收标准（Acceptance Criteria）





每个 Task 必须定义完成条件。





例如：





□ 文件结构符合要求



□ 字段命名统一



□ 数据来源可追溯



□ 未修改禁止文件



□ 未违反 Atlas Constitution



□ 生成 Review Report





只有全部满足后：



Task 才能进入 Review 状态。





\---





\## 7. 输出要求（Output Requirements）





AI Agent 完成 Task 后必须输出报告。





报告至少包括：





任务名称





执行状态





读取文件





修改文件





未修改文件





发现问题





验证结果





下一步建议





\---





\# 八、AI Agent 执行规则





执行任何 Task 前：



必须先阅读：



1\. AGENTS.md



2\. WORKFLOW.md



3\. TASK\_TEMPLATE.md



4\. Task 指定文件





\---





AI Agent 必须遵守：





事实优先。



证据优先。



结构优先。



长期价值优先。





禁止：



编造数据。



编造来源。



修改历史事实。



提供投资建议。



预测股票价格。



扩大任务范围。





\---



\# 九、Task 与 Atlas 规范体系关系





Task 不是独立存在的文件。



Task 必须服从 Atlas 整体规范体系。





执行优先级：





1\. ATLAS CONSTITUTION





2\. AGENTS.md





3\. WORKFLOW.md





4\. TASK\_TEMPLATE.md





5\. Task 文件





6\. Standard 文件





7\. Data Model





8\. Template 文件







任何 Task：



不得违反上层规范。





如果 Task 与 Standard 存在冲突：



必须停止执行。



生成问题报告。



等待人工确认。





\---



\# 十、Git 操作规则





默认情况下：





AI Agent：



禁止自动 Commit。





禁止自动 Push。





禁止删除 Git 历史。





任务完成后：



必须等待人工 Review。





人工确认后：



才可以执行 Git 操作。





\---





\# 十一、异常处理规则





当 AI Agent 遇到以下情况：





\- 权限不足



\- 标准缺失



\- 数据来源不足



\- 文件结构冲突



\- 任务目标不明确





必须：





1\. 停止继续修改。





2\. 输出异常报告。





3\. 说明问题原因。





4\. 等待人工确认。





禁止：





\- 自行猜测解决方案



\- 绕过权限限制



\- 创建未授权文件



\- 修改无关资产





\---





\# 十二、Task 系统理念





Atlas 不依靠临时指令驱动。





Atlas 依靠：



标准化 Task



驱动：



AI Agent



生产：



可信知识资产。





Task 是 Atlas 知识生产系统中的执行单元。





通过：



任务定义



↓



AI 执行



↓



人工审核



↓



版本管理





不断形成可持续演化的资本市场知识基础设施。





\---



\# 十三、版本记录（Change Log）





\## Version 1.0





首次建立 Atlas Task System 规范。





定义：



\- Task 文件作用



\- Task 生命周期



\- 命名规范



\- 执行流程



\- AI Agent 规则



\- Git 管理规则



\- 异常处理流程





\---



End.



