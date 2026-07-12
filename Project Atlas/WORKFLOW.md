\# WORKFLOW.md



\# Project Atlas - 工作流程规范



Version：1.0



Status：Active



Owner：Project Atlas



Last Updated：2026-07-13



\---



\# 一、目的



本文件定义 Project Atlas 的标准工作流程。



任何新增知识、修改知识、产品开发、AI 自动化任务，都必须遵循本流程。



目标：



保证：



\- 可持续

\- 可追溯

\- 可审核

\- 可自动化

\- 可长期维护



\---



\# 二、Atlas 开发流程



所有工作必须遵循以下顺序：



产品需求



↓



标准制定



↓



数据模型



↓



模板设计



↓



AI 自动生成



↓



人工审核



↓



Git Commit



↓



Git Push



↓



进入正式知识库



禁止跳过任何步骤。



\---



\# 三、每日工作流程（Daily Workflow）



每天按照以下节奏开展工作：



\## 上午



产品设计



讨论需求



完善标准



确定任务



输出 Task



\---



\## 下午



AI Agent（Codex）执行任务



创建文件



修改文件



检查格式



生成修改报告



\---



\## 晚上



人工 Review



检查事实



检查来源



确认质量



Commit



Push



总结 Sprint



\---



\# 四、知识创建流程（Knowledge Creation Workflow）



任何知识创建必须遵循：



Step 1



确认是否已有同类知识。



↓



Step 2



阅读：



AGENTS.md



相关 Standard



相关 Data Model



Template



↓



Step 3



创建 Markdown



↓



Step 4



填写事实



↓



Step 5



填写来源



↓



Step 6



检查格式



↓



Step 7



等待人工审核



↓



Step 8



Commit



↓



Step 9



Push



\---



\# 五、AI Agent 工作流程



AI Agent 接到任务后：



① 阅读 AGENTS.md



↓



② 阅读对应 Standard



↓



③ 阅读 Data Model



↓



④ 阅读 Template



↓



⑤ 执行 Task



↓



⑥ 输出修改报告



↓



⑦ 等待人工确认



AI Agent 不得自动 Push。



\---



\# 六、Git 工作流程



每天建议：



一个 Sprint



一次 Commit



一次 Push



Commit Message：



Sprint XXX：任务名称



例如：



Sprint 007：Create First Company Asset



\---



Commit Description：



完成内容



修改文件



新增文件



待确认事项



存在风险



\---



\# 七、Markdown 生命周期



Draft（草稿）



↓



Review（审核）



↓



Approved（通过）



↓



Published（正式）



↓



Updated（更新）



↓



Archived（归档）



任何文件都必须标明当前状态。



\---



\# 八、质量检查（Quality Checklist）



Commit 前必须检查：



☐ 文件命名正确



☐ 编号唯一



☐ Markdown 格式正确



☐ 来源完整



☐ 字段符合 Data Model



☐ 无重复内容



☐ 无编造事实



☐ 无投资建议



全部通过后才能 Commit。



\---



\# 九、Sprint 工作方式



每个 Sprint：



必须有：



目标



输出



Commit



总结



例如：



Sprint 007



目标：



建立第一家公司资产



输出：



COMP-000001-BYD.md



Commit：



Sprint 007：Create First Company Asset



总结：



完成第一家公司模板



\---



\# 十、长期开发原则



Atlas 不追求：



速度。



Atlas 追求：



持续积累。



每天增加一点可信知识。



每一次 Commit 都应提升 Atlas 的长期价值。



\---



\# 十一、版本管理



所有重要文档：



Version



Created



Updated



Status



必须维护。



不得删除历史。



重大修改：



Version +0.1



重大重构：



Version +1.0



\---



\# 十二、知识资产原则



Atlas 的核心资产不是代码。



不是数据库。



而是知识。



每一个 Markdown 都是一项长期资产。



每一次修改都应提升知识质量。



\---



\# 十三、Project Atlas 工作信条



先理解。



再记录。



先事实。



后观点。



先标准。



后自动化。



先质量。



后数量。



宁可缺失。



不可错误。





\# 十四、Knowledge First



任何自动化都必须服务于知识。



任何代码都必须服务于产品。



任何产品都必须服务于用户。



任何知识都必须来源于事实。



Atlas 永远遵循：



Knowledge First.



Automation Second.



\---



End of WORKFLOW.md

