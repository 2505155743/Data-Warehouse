# Data-Warehouse
基于 Hadoop + Hive 的离线数据仓库项目，实现电商业务数据的采集、清洗、转换和汇总分析。
# 项目流程设计
<img width="1815" height="937" alt="image" src="https://github.com/user-attachments/assets/d8b2a923-218d-44dc-97b4-16730201c134" />


# 技术选型
<img width="459" height="486" alt="image" src="https://github.com/user-attachments/assets/35db35f7-420c-4119-98be-f6732d73202b" />


# 集群规划
<img width="526" height="594" alt="image" src="https://github.com/user-attachments/assets/b8329897-9d0c-473f-8425-086b136ffe01" />

# 数据仓库架构
<img width="1245" height="346" alt="image" src="https://github.com/user-attachments/assets/11c5876e-0af3-4d23-86b5-282b260f690b" />
# 核心功能

# 1. 数据采集
批量采集：DataX 实现多数据源全量/增量同步
离线批处理：纯离线数据同步，每日定时执行

# 2. 维度建模
雪花模型：多层级维度关联，如商品→品类→品牌
SCD缓慢变化维：支持 SCD1（覆盖更新）、SCD2（拉链表）、SCD3（多版本列）三种模式
多类型维度表：普通维度、分层维度、拉链表、快照表、累计快照表

# 3. ETL 流程
数据清洗：去重、过滤脏数据、格式统一
数据脱敏：手机号、邮箱、身份证等敏感信息脱敏
指标计算：GMV、订单量、用户留存等核心指标

# 4. 指标体系
原子指标：基础度量指标
衍生指标：基于原子指标计算
复合指标：多指标组合计算
指标血缘：完整的指标依赖链路

# 5. 任务调度与运维
DolphinScheduler：复杂工作流编排、跨周期依赖、批量任务运维
监控告警：任务超时告警、失败自愈、批量重跑机制

# 6. Hive 深度优化
分区裁剪：高效的数据过滤
索引优化：提升查询性能
大表Join优化：MapJoin、BucketJoin等优化策略
数据生命周期管理：冷热数据分离

# 7. 数据可视化
Superset 报表：GMV日报、周报、月报，转化率分析、商品销售排行
自助报表：支持业务人员自主查询分析

# 数据说明
<img width="1227" height="583" alt="image" src="https://github.com/user-attachments/assets/885d2e3f-b1a8-4fd5-9017-b847bb98d750" />
<img width="1826" height="861" alt="image" src="https://github.com/user-attachments/assets/2eb1a30c-6549-4fd1-9e6c-3e4f6616fe9f" />
