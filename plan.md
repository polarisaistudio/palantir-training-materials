# Palantir 实操教程系列规划

## 大方向

不再讲概念，直接录屏操作。每个视频5-8分钟，一个视频只教一个东西。
观众跟着做就能学会。中英双语or纯中文都可以。

环境：progressbootcamp.palantirfoundry.com（你公司的sandbox）

---

## 教程分组

### A组：数据工程（进数据、清洗、管道）

**A1. 怎么把数据导进Foundry**
- 手动上传CSV
- 在Foundry里看数据长什么样
- 5分钟搞定

**A2. 用Pipeline Builder清洗数据（无代码）**
- 拖拽式操作：过滤、改列名、join两张表
- 跑一次build，看结果
- 对应learn.palantir.com课程：Deep Dive: Building Your First Pipeline

**A3. 用Code Repository写Python transform**
- 同样的清洗逻辑，用代码做一遍
- 对比Pipeline Builder，什么时候用哪个
- 对应课程：Deep Dive: Transforming Data with Code Repositories

---

### B组：Ontology（建模、配置、探索）

**B1. 从零建一个Ontology**
- 拿清洗好的数据，创建Object Type
- 选主键、配Property、设display name
- 在Object Explorer里点进去看效果
- 对应课程：Deep Dive: Creating Your First Ontology

**B2. 建Link Types连接两个Object Type**
- 比如：Building → Work Order（一对多）
- 点进Building看到关联的所有Work Orders
- 讲清楚"反向链接"怎么配

**B3. 建Action Type**
- 创建一个简单的action：修改Work Order状态
- 配参数、规则、权限
- 在Object Explorer里执行一次，看Action Log

---

### C组：应用开发（Workshop搭应用）

**C1. 用Workshop搭一个简单仪表盘**
- Object List + Object Detail面板
- 点击一行看详情
- 对应课程：Deep Dive: Building Your First Application

**C2. 在Workshop里加Action按钮**
- 把B3建的Action Type拉进来
- 用户点按钮就能改状态
- 展示操作→审计日志的完整链路

**C3. 在Workshop里嵌入AIP Agent**
- 加一个Agent聊天面板
- 用户选一个对象，跟AI对话
- 这个视频会比较吸引人，因为有AI交互画面

---

### D组：AIP（AI功能）

**D1. AIP Threads基础**
- 打开Threads，拖入一个PDF或CSV
- 问几个问题，展示AI怎么回答
- 最简单的AIP体验，3分钟就完

**D2. 建一个AIP Agent**
- Agent Studio界面走一遍
- 写system prompt、配Ontology上下文、加一个工具
- 测试对话
- 对应课程：Speedrun: Your First Agentic AIP Workflow

**D3. 建一个AIP Logic函数**
- 输入一个Object，用LLM块做分类
- 看Debugger里的思维链
- 发布成Function

**D4. 用Automate跑Logic**
- 把D3的函数接到触发器上
- 新对象创建时自动跑
- 展示"暂存审核"模式

---

### E组：进阶（按兴趣选做）

**E1. 用Data Connection连外部数据库**
- 如果bootcamp环境支持的话，连一个外部PostgreSQL
- 对应课程：Deep Dive: Creating Your First Data Connection

**E2. 写一个Ontology Function（TypeScript）**
- 在Code Repository里写函数
- 读Object、做计算、返回结果
- 对应课程：Speedrun: Your First Ontology Function

**E3. 用Contour / Quiver做数据分析**
- 拖拽式图表、聚合、过滤
- 适合分析师受众

---

## 建议的录制顺序

先做最能出效果的，不用按A→B→C顺序来：

**第一批（先出这4个，快速积累内容）：**
1. D1 — AIP Threads（最简单，最直观，3分钟）
2. B1 — 从零建Ontology（基础操作，大家最想看的）
3. C1 — Workshop搭仪表盘（有画面感）
4. D2 — 建AIP Agent（AI+操作，最吸引人）

**第二批（补完基础链路）：**
5. A1 — 导入数据
6. A2 — Pipeline Builder清洗
7. B2 — Link Types
8. B3 — Action Type

**第三批（完整工作流）：**
9. C2 — Workshop加Action按钮
10. D3 — AIP Logic
11. D4 — Automate
12. C3 — Workshop嵌入Agent

---

## 造数据建议

简单造一套通用的demo数据就行，不用太复杂：

**buildings.csv**
building_id, address, city, type, year_built, sqft, status
（20-30行就够）

**work_orders.csv**
wo_id, building_id, category, description, priority, status, created_date, completed_date, cost
（50-100行，category包括：Plumbing, HVAC, Electrical, Roofing, Appliance等）

**technicians.csv**
tech_id, name, specialty, phone, active
（10行）

这套数据能覆盖所有教程：Object Types（Building, Work Order, Technician）、Links（Building→WO, Technician→WO）、Actions（更新WO状态）、AIP（根据描述分类优先级）。

跟你在Progress Residential的工作相关，但完全是虚构数据，没有合规问题。

---

## 每个视频的固定格式

1. 开头5秒：今天做什么（一句话）
2. 操作录屏：边做边讲，不废话
3. 结尾5秒：做完了，效果是什么

不需要概念介绍、不需要跟官方文档对照、不需要总结回顾。
就是"打开→操作→搞定"。
