\# Company Review Checklist



Version: 1.0



Status: Active



Owner: Project Atlas



Created: 2026-07-13



\---



\# 一、Purpose（目的）



Company Review Checklist 是 Atlas Company Asset 的统一审核清单。



作用：



\- 统一 Company Review 标准

\- 保证不同 Company 使用相同审核规则

\- 验证 Company Asset 是否符合 Atlas Standards

\- 为 Human Review 提供统一依据



Checklist：



只负责检查。



不负责修改。



Review 发现的问题应记录到：



Company Review Report。



\---



\# 二、Review Scope（审核范围）



本 Checklist 适用于：



\- Company Lifecycle Version 0.1

\- Company Lifecycle Version 0.5

\- Company Lifecycle Version 1.0

\- Company Lifecycle Version 2.0



当前默认：



Version 0.1。



\---



\# 三、Review Result（审核结果）



允许结果：



PASS



CHANGES REQUESTED



FAIL



说明：



PASS：



符合当前生命周期要求。



CHANGES REQUESTED：



存在问题。



修改后重新 Review。



FAIL：



存在重大结构错误。



不得进入 Repository。



\---

\# 四、Metadata Review（元数据检查）



确认以下 Metadata 是否符合 AS-006。



\---



\## Lifecycle Metadata



□ Version 正确



□ Lifecycle Status 正确



□ Lifecycle Stage 正确



□ Data Status 正确



□ Verified 字段存在



\---



\## Asset Metadata



□ Company ID 正确



□ Created 存在



□ Last Updated 存在



□ Verified At 存在



\---



\## Metadata Consistency



确认：



□ Metadata 与 Company Lifecycle Version 一致



□ Lifecycle Status 与 Data Status 未混用



□ Metadata 字段名称符合 AS-006



Review Result：



PASS / CHANGES REQUESTED / FAIL



\---



\# 五、Structure Review（结构检查）



确认 Company Asset 是否符合 TEMPLATE-Company.md。



\---



\## Markdown Structure



□ 一级标题正确



□ 二级标题正确



□ 三级标题正确



□ 标题层级一致



\---



\## Section Order



确认章节顺序正确：



□ Metadata



□ 公司基本信息



□ 主营业务



□ 行业信息



□ 公司简介



□ 来源



\---



\## Field Naming



确认字段名称符合 DM-002：



□ 成立日期



□ 主行业



□ 细分行业



□ 市场概念



□ 产业角色



不得出现：



□ 成立时间



□ 一级行业



□ 二级行业



□ 所属概念



Review Result：



PASS / CHANGES REQUESTED / FAIL



\---

\# 六、Field Review（字段检查）



确认 Company Asset 是否符合 DM-002 Company Schema。



\---



\## Identity



□ Company ID



□ 股票代码



□ 公司简称



□ 公司全称



□ 英文名称



□ 上市交易所



□ 上市状态



\---



\## Company Information



□ 成立日期



□ 注册地址



□ 总部所在地



□ 法定代表人



□ 企业性质



\---



\## Business



□ 主营业务



□ 核心产品



□ Atlas 公司简介



\---



\## Industry



□ 主行业



□ 细分行业



□ 市场概念



□ 产业角色



\---



\## Placeholder Rule



所有无法确认字段：



统一使用：



□ 待核实



不得出现：



□ 空白



□ -



□ 暂无



□ 以后补充



□ Unknown



\---



Review Result：



PASS / CHANGES REQUESTED / FAIL



\---



\# 七、Source Review（来源检查）



所有正式事实必须具有可靠来源。



\---



\## Official Sources



优先来源：



□ 公司官网



□ 上市公司公告



□ 年报



□ 招股说明书



□ 深圳证券交易所



□ 上海证券交易所



\---



\## Source Quality



确认：



□ 来源真实



□ 来源可访问



□ 来源能够验证对应事实



□ 来源与字段一致



\---



\## Source Coverage



检查：



□ 所有已确认字段均具有来源



□ 无无来源事实



□ 无 AI 推测内容



\---



\## Trust Review



确认：



□ 不存在投资建议



□ 不存在股价预测



□ 不存在盈利预测



□ 不存在 SWOT



□ 不存在主观评价



Atlas 只记录：



可信事实。



Review Result：



PASS / CHANGES REQUESTED / FAIL



\---

\# 八、Production Compliance（生产规范检查）



确认 Company Asset 是否符合 Atlas Production Pipeline。



\---



\## Production Rules



确认：



□ 已按照 TASK 执行



□ 已按照 TEMPLATE 创建



□ 已按照 DM-002 填写字段



□ 已按照 AS-006 管理生命周期



□ 已按照 AS-007 Repository Governance 执行



\---



\## Production Boundary



确认：



未生成：



□ 财务分析



□ 投资建议



□ 股价预测



□ 盈利预测



□ SWOT 分析



□ 主观判断



\---



\## Production Report



确认：



□ Company Production Report 已生成



□ Production Metrics 已填写



□ Standard Compliance 已填写



□ Review Result 已填写



\---



\## Benchmark Validation



如存在 Benchmark：



确认：



□ Metadata 保持一致



□ Markdown 结构保持一致



□ 字段顺序保持一致



□ Production Report 格式保持一致



不得复制：



Benchmark 业务内容。



\---



Review Result：



PASS / CHANGES REQUESTED / FAIL



\---



\# 九、Final Review Decision（最终审核结论）



完成所有 Review 后，



汇总以下结果：



| Review Item | Result |

|-------------|--------|

| Metadata Review | PASS / CHANGES REQUESTED / FAIL |

| Structure Review | PASS / CHANGES REQUESTED / FAIL |

| Field Review | PASS / CHANGES REQUESTED / FAIL |

| Source Review | PASS / CHANGES REQUESTED / FAIL |

| Production Compliance | PASS / CHANGES REQUESTED / FAIL |



\---



最终结论：



□ PASS



□ CHANGES REQUESTED



□ FAIL



\---



\# 十、Review Summary（审核总结）



Reviewer：



\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_



Review Date：



\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_



Company：



\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_



Lifecycle Version：



\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_



Review Result：



\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_



Major Issues：



\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_



\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_



\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_



Suggestions：



\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_



\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_



\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_



\---



\# 十一、Checklist Version



Version：



1.0



Applicable Standard：



\- AS-006 Company Lifecycle Standard

\- AS-007 Repository Governance Standard

\- DM-002 Company Schema

\- TEMPLATE-Company.md



\---



End.

