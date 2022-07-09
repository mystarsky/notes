# 软件生存周期和过程管理基本概念
1. 软件过程：开发维护相关产品，包括
   1. 项目计划
   2. 设计文档
   3. 代码
   4. 测试用例
   5. 用户手册
2. 软件生存周期过程：开发、运行、维护
   1. ISO/IEC 12207
3. 敏捷开发
   + 人月神话
   1. Scrum: Scrum Guide
      1. Time box 时间盒
      2. PSPI 潜在的可交付增量
      3. Adaptive development 演进式开发
   2. DevOps
      > [What is DevOps](https://theagileadmin.com/what-is-devops/)
      > [A DevOps Manifesto](https://theagileadmin.com/2010/10/15/a-devops-manifesto/)
   + Scrum and DevOps
      > [Scrum And DevOps](https://www.scrum.org/resources/blog/scrum-and-devops)
4. 过程改进
   + 传统行业：PDCA循环
      1. Plan: 
         1. 分析现状找出问题
         2. 分析影响质量的问题
         3. 找出措施
         4. 拟定措施计划
      2. Do: 执行措施、计划 
      3. Check: 检查效果，发现问题
      4. Action: 
         1. 总结经验纳入标准
         2. 遗留问题转入下期
   + 软件行业：IDEAL
      1. 启动 Initiating（不参与循环）
         1. 激励改进
         2. 设定环境和获得支持
         3. 建立改进框架
      2. 诊断 Diagnosing
         1. 建立改进框架
         2. 评估和描述当前实践
         3. 提炼意见和记录阶段性成果
      3. 建立 Establishing
         1. 制定策略和优先级
         2. 建立过程执行组，计划执行
         3. 定义过程和度量，计划和执行指导，建立计划、执行和追踪
         4. 文档化、分析教训
         5. 修正组织的方法
      4. 执行 Acting
      5. 调整 Leveraging
   + 参考模型与标准
      1. CMM / CMMI 能力成熟度模型/能力成熟度模型集成
      2. SPICE / ISO/IEC 15504
         + SPICE 软件过程改进和能力鉴定
         + ISO/IEC 15504 软件过程评估
      3. ISO/IEC 12207 软件生存周期过程
      4. ISO 9000 质量管理体系
# Scrum
+ 4 stages in each Sprint
   1. Plan
   2. Build
   3. Test
   4. Review
+ 3 roles
   1. 产品经理 Product Owner
   2. 团队负责人 Scrum Master
   3. 团队 Team
+ 3 artifacts
   1. 产品需求列表 Product Backlog: 用户故事在这里按优先级排序
      + User Story在这里被写出来
   2. Sprint Backlog: 最优先的用户故事进入Sprint Backlog，其他的等待下次Sprint
   3. Burndown Chart: 展示Sprint Backlog上任务进度，达到0说明都完成了
+ 3 Ceremonies
   1. Sprint Planning: Sprint开始时，讨论用户故事优先级，估计工作量
   2. Daily Scrum: 团队日常简述进度，讨论是否有任务需要搁置或加派人手
   3. Sprint Review: Sprint结束时，汇报展示，讨论改进
+ 整个流程
   1. 产品经理创建Product Backlog，把需要的用户故事写在上面
   2. 所有人一起讨论Sprint Planning，确定接下来Sprint要做的用户故事
   3. 创建Sprint Backlog
   4. 整个团队在一到三周内开发完成Sprint Backlog中的用户需求，期间例行Daily Scrum
   5. Potentially Shippable Product诞生
   6. 举行Sprint Review，团队向产品经理做展示，一起讨论改进
   7. 重复2-6的Sprint过程