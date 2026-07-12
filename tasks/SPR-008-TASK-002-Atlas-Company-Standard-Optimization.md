\# SPR-008-TASK-002-Atlas-Company-Standard-Optimization



Version: 1.0



Status: Active



Owner: Project Atlas



Sprint: 008



Created: 2026-07-13



\---



\# 一、任务目的



本任务用于优化 Atlas Company（上市公司）资产生产流程。





在完成：



COMP-000001-BYD



第一家公司资产创建与 Review 后，发现：





\- DM-002 Company Schema



\- AS-006 Company Lifecycle Standard



\- TEMPLATE-Company.md



\- AI Agent 执行流程





之间存在部分结构不一致。





本任务目标：



分析问题。



制定优化方案。



提高未来 Company Asset 创建的一致性。





\---



\# 二、任务定位





本任务属于：



Atlas Company Production Optimization





阶段：





问题分析与方案设计阶段。





本任务：



不直接修改生产文件。





实际标准修改：



由后续专项 Task 执行。





\---



\# 三、背景





Atlas 第一个 Company Asset：





companies/COMP-000001-BYD.md





经过 Structure Review 后发现：





\## 已发现问题：





1\. 生命周期状态与数据状态命名冲突。





2\. Company 模板标题层级不统一。





3\. v0.1 基础资产范围不够明确。





4\. AI Agent 创建任务范围需要进一步限制。





5\. DM-002、AS-006、TEMPLATE 三者职责边界需要明确。





\---

\# 四、优化分析范围





本任务分析以下文件：





\## 数据模型层





data-model/DM-002-Company-Schema.md





作用：



定义 Company 完整数据结构。





\---



\## 生命周期层





standards/AS-006-Company-Lifecycle-Standard.md





作用：



定义 Company Asset 演化过程。





\---



\## 模板层





templates/TEMPLATE-Company.md





作用：



定义 Company 文件生产格式。





\---



\## Agent执行层





tasks/TASK\_TEMPLATE.md





作用：



定义 AI Agent 执行任务流程。





\---



\# 五、优化目标





\## 目标一：统一 Company 文件结构





分析：



TEMPLATE-Company.md





优化方向：





统一：



\- 文件标题



\- Markdown章节层级



\- 字段名称





目标结构：





\# COMP-ID-Company





\## 公司基本信息





\### Company ID





\### 股票代码





\### 公司名称





避免：



公司名称作为一级标题导致结构下沉。





\---



\# 目标二：区分状态体系





当前问题：





AS-006:



Status





DM-002:



数据状态





两个概念容易混淆。





优化方向：





明确：



Lifecycle Status





与





Data Status





两个独立概念。





\---

\# 六、状态体系优化方向





\## Lifecycle Status





表示：



Company Asset 生命周期状态。





例如：





\- Draft



\- Review



\- Active



\- Deprecated





\---





\## Data Status





表示：



Company 数据质量状态。





例如：





\- 最新



\- 部分过期



\- 已过期



\- 审核中



\- 未知





禁止：



使用同一个 Status 字段表达两个含义。





\---



\# 目标三：明确 Company 生命周期范围





重新确认：





\## Version 0.1



基础入库。





必须：



\- Company ID



\- 股票代码



\- 公司名称



\- 上市状态



\- 主营业务



\- 主行业



\- 官方来源





\---



\## Version 0.5





企业认知。





增加：



\- 商业模式



\- 产品体系



\- 客户类型



\- 产业角色



\- 管理层





\---



\## Version 1.0





完整资产。





增加：



\- 财务快照



\- 风险记录



\- 承诺兑现



\- 时间轴





\---



\# 目标四：优化 AI Agent 执行规则





AI Agent 创建 Company 时：





必须：



1\. 读取 AGENTS.md



2\. 读取 AS-006



3\. 读取 DM-002



4\. 读取 TEMPLATE-Company





然后确认：



目标生命周期版本。





默认：



Company Lifecycle v0.1





禁止：



一次性生成完整研究报告。





\---

\# 七、禁止事项





本任务特别禁止：





\- 修改 COMP-000001-BYD.md



\- 根据单家公司情况降低 Atlas 标准



\- 删除未来阶段字段定义



\- 修改 DM-002 核心结构



\- 为快速生成资产减少数据模型要求





\---



\# 八、执行步骤





\## Step 1





检查：



DM-002



AS-006



TEMPLATE-Company



TASK\_TEMPLATE





之间的关系。





\---



\## Step 2





输出问题分析。





\---



\## Step 3





制定优化方案。





\---



\## Step 4





等待人工 Review。





\---



\# 九、验收标准





任务完成必须满足：





□ 明确 DM-002、AS-006、TEMPLATE职责边界





□ 明确生命周期版本范围





□ 明确状态体系区别





□ 明确 AI Agent 执行规则





□ 不修改 Company Asset





□ 输出优化分析报告





\---



\# 十、输出要求





完成后输出：





《Atlas Company Standard Optimization Report》





报告包括：





\- 当前问题



\- 分析结果



\- 建议修改方案



\- 涉及文件



\- 对未来 Company Asset 的影响





\---



\# 十一、Git要求





本任务：



禁止自动 Commit。





禁止自动 Push。





等待人工 Review。





\---



End.

