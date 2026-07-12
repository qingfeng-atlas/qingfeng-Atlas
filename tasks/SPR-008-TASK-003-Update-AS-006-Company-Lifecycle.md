\# SPR-008-TASK-003-Update-AS-006-Company-Lifecycle



Version: 1.0



Status: Active



Owner: Project Atlas



Sprint: 008



Created: 2026-07-13



\---



\# 一、任务目标（Objective）



根据：



COMP-000001-BYD Structure Review Report



以及：



Atlas Company Standard Optimization Analysis Report





优化：



standards/AS-006-Company-Lifecycle-Standard.md





目标：



明确 Company 生命周期规则。





解决：



\- Lifecycle Status 与 Data Status 混淆问题



\- Company 生命周期版本边界不清问题



\- AI Agent 创建 Company 范围不明确问题





\---



\# 二、执行前必须阅读





AI Agent 必须按照以下顺序读取：





1\. AGENTS.md





2\. WORKFLOW.md





3\. TASK\_TEMPLATE.md





4\. standards/AS-006-Company-Lifecycle-Standard.md





5\. data-model/DM-002-Company-Schema.md





6\. COMP-000001-BYD Structure Review Report





7\. Atlas Company Standard Optimization Analysis Report





\---



\# 三、修改范围





允许修改：



standards/AS-006-Company-Lifecycle-Standard.md





禁止修改：



constitution/



data-model/



templates/



companies/



events/



relations/





禁止：



\- 修改 DM-002



\- 修改 COMP-000001-BYD.md



\- 修改 TEMPLATE-Company.md





\---



\# 四、优化内容





\## 目标一：明确状态体系





当前问题：





AS-006 使用 Status 表示生命周期。





DM-002 使用数据状态表示数据质量。





优化后必须区分：





\---



\# Lifecycle Status





表示：



Company 资产生命周期状态。





允许值：





\- Draft



\- Review



\- Active



\- Deprecated





说明：





Draft：



Company Asset 已创建，基础结构完成，等待人工审核。





Review：



AI Agent 已完成生成，进入人工验证阶段。





Active：



已经通过人工 Review，正式进入 Atlas 知识库。





Deprecated：



历史资产，不再作为当前有效数据使用。





\---



\# Data Status





表示：



Company 数据质量状态。





允许值：





\- 最新



\- 部分过期



\- 已过期



\- 审核中



\- 未知





说明：





Data Status 只描述数据可靠程度。





不能代表 Company Asset 生命周期。





禁止：



使用 Status 同时表示 Lifecycle Status 和 Data Status。





\---



\# 五、Company Lifecycle Version





AS-006 必须明确 Company Asset 分阶段建设。





\---



\## Version 0.1





基础入库阶段。





目标：



建立可信 Company 节点。





必须包含：





\- Company ID



\- 股票代码



\- 公司名称



\- 上市状态



\- 主营业务



\- 主行业



\- 官方来源





不要求：





\- 财务快照



\- 风险分析



\- 完整事件时间轴



\- 完整关系网络





\---



\## Version 0.5





企业认知阶段。





增加：





\- 商业模式



\- 产品体系



\- 客户类型



\- 产业角色



\- 核心管理层



\- 重要事件关联





\---



\## Version 1.0





完整 Company Asset。





增加：





\- 财务快照



\- 风险记录



\- 承诺兑现



\- 发展时间轴





\---



\## Version 2.0





知识图谱阶段。





增加：





\- Relation 网络



\- Event 因果关系



\- 行业关系



\- 政策关系





\---



\# 六、AI Agent 执行规则





AI Agent 修改 AS-006 时：





必须：



1\. 读取当前 AS-006 文件



2\. 理解 DM-002 字段定义



3\. 保持与 Atlas 宪法一致





禁止：



\- 修改 DM-002



\- 修改 Company Asset



\- 根据单个公司案例降低标准



\- 删除未来阶段定义





\---



\# 七、待核实字段规范





Company Asset 中：



所有无法确认的信息：





统一填写：



待核实





禁止使用：





\- 空白



\- -



\- 待填写





除非字段允许，否则禁止使用：



未知





\---



\# 八、验收标准（Definition of Done）





任务完成必须满足：





□ Lifecycle Status 与 Data Status 已分离





□ Company Version 0.1 / 0.5 / 1.0 / 2.0 已定义





□ AI Agent 默认生成 v0.1





□ 待核实规则明确





□ 未修改 DM-002





□ 未修改 COMP-000001-BYD.md





□ 未修改 TEMPLATE-Company.md





□ 输出 AS-006 Update Report





\---



\# 九、输出要求





完成后输出：





《AS-006 Company Lifecycle Update Report》





报告包含：





1\. 修改文件



2\. 修改内容



3\. 修改原因



4\. 与 DM-002 的关系



5\. 对未来 Company Asset 的影响





\---



\# 十、Git要求





完成修改后：



禁止自动 Commit。



禁止自动 Push。





等待人工 Review。





\---



End.

