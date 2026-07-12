\# AGENTS.md



\# Project Atlas - AI Agent 工作规范



Version：1.0



Status：Active



Owner：Project Atlas



Last Updated：2026-07-13



\---



\# 一、Project Atlas 是什么？



Project Atlas 是一个面向中国普通投资者的长期知识工程。



Atlas 的目标不是预测市场，也不是提供投资建议。



Atlas 的目标是：



> 建立可信、可追溯、可持续演进的资本市场知识系统，帮助普通投资者降低信息焦虑，提高认知效率。



所有 AI Agent 都必须遵守这一目标。



\---



\# 二、Atlas Mission（使命）



Atlas exists to reduce decision anxiety through trusted knowledge.



Atlas 存在的意义，是通过可信知识降低普通投资者的决策焦虑。



不是帮助赚钱。



不是预测股价。



不是推荐股票。



而是帮助用户理解。



\---



\# 三、Atlas 第一原则



所有内容必须：



真实（Truth）



可追溯（Traceable）



可验证（Verifiable）



可持续更新（Continuously Evolving）



任何无法验证的信息不得作为事实写入 Atlas。



\---



\# 四、Single Source of Truth



Atlas 采用 Single Source of Truth（唯一事实来源）原则。



所有知识首先以 Markdown 保存。



Markdown 是唯一官方数据源。



所有页面、数据库、JSON、API、AI 回复均来源于 Markdown。



禁止多个版本同时维护。



\---



\# 五、目录规范



constitution/



Atlas 宪法



standards/



所有标准



data-model/



数据模型



templates/



模板



companies/



公司资产



events/



事件资产



relations/



关系资产



personas/



投资者画像



research/



研究



product/



产品设计



meeting/



会议记录



tasks/



Codex 工作任务



\---



\# 六、文件命名规范



Company



COMP-000001-BYD.md



Event



EVT-000001.md



Relation



REL-000001.md



Persona



PER-000001.md



Research



RES-000001.md



Policy



POL-000001.md



Industry



IND-000001.md



禁止修改编号。



编号永远唯一。



\---



\# 七、Company 规则



所有 Company 必须：



遵守 DM-002。



不得修改字段名称。



不得新增未经批准字段。



未知字段统一填写：



待核实



不得猜测。



不得编造。



\---



\# 八、Event 规则



所有事件必须：



有来源。



有时间。



有主体。



有影响对象。



能够追溯。



禁止：



"据说"



"网传"



"可能"



等无法验证内容。



\---



\# 九、Relation 规则



所有 Relation 必须：



连接两个明确实体。



说明关系类型。



说明证据来源。



\---



\# 十、数据来源



优先级：



一级：



上市公司公告



交易所公告



政府文件



二级：



公司官网



年度报告



招股说明书



三级：



权威媒体



行业协会



四级：



研究机构



未经验证的信息不得进入 Atlas。



\---



\# 十一、禁止事项



AI Agent 禁止：



编造数据



编造来源



修改历史事实



提供投资建议



预测股价



制造结论



输出无法验证的信息



\---



\# 十二、Git 工作流



修改前：



阅读相关标准。



修改后：



检查 Markdown。



检查编号。



检查引用。



检查目录。



生成 Commit Summary。



生成 Commit Description。



不得自动 Push。



不得自动删除文件。



\---



\# 十三、工作流程



开始任务：



↓



阅读 AGENTS.md



↓



阅读相关标准



↓



执行 Task



↓



检查规范



↓



生成修改报告



↓



等待人工 Review



↓



Commit



↓



Push



\---



\# 十四、质量标准



每一个 Markdown 都必须回答：



它是否真实？



是否有来源？



是否容易理解？



是否符合 Atlas 标准？



如果任何一项答案是否。



不得提交。



\---



\# 十五、Atlas 产品原则



Atlas 不是信息平台。



Atlas 是认知平台。



Atlas 不追求信息最多。



Atlas 追求理解最深。



Atlas 不回答：



"买不买？"



Atlas 回答：



"发生了什么？"



"为什么重要？"



"它影响什么？"



\---



\# 十六、AI Agent 行为准则



AI Agent 应始终：



保持客观。



保持谨慎。



优先事实。



优先来源。



优先标准。



优先长期价值。



任何情况下不得为了完成任务而编造内容。





\# 十七、工程哲学（Engineering Philosophy）



Atlas 是一项持续十年以上的知识工程。



短期效率不能破坏长期质量。



任何自动化都必须服务于知识质量，而不是数量。



任何 AI Agent 都应优先维护 Atlas 的可信度，而不是完成速度。



如果事实无法确认，应明确标记"待核实"，而不是推测。



宁可缺失，不可错误。



\---



End of AGENTS.md

