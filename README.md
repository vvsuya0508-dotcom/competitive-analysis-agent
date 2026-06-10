# 智能竞品分析多 Agent 系统

> 输入产品名称，自动完成竞品发现、多源数据采集、
> 三维并行分析，输出七章结构化竞品报告

🔗 **在线体验**：https://udify.app/workflow/HMXQClIozD3KfseH
（输入"飞书"或任意产品名即可体验）

## 项目背景
聚焦企业竞品调研"信息碎片化、人工整理耗时"的痛点，
基于 Dify 完成从业务洞察到 MVP 的全栈落地。

## 系统架构
串行采集 → 并行分析 → 串行汇总的混合协作模式

| 阶段 | Agent | 职责 |
|---|---|---|
| Phase 1 | 竞品发现 Agent | 关键词生成 + 搜索筛选，识别3-8个核心竞品 |
| Phase 2 | 数据采集 Agent | 迭代逐竞品采集功能/定价/口碑/市场四维度 |
| Phase 3 | 产品分析 Agent | 输出功能对比矩阵（✅/🔶/❌） |
| Phase 3 | 定价分析 Agent | 定价模型对比与性价比排序 |
| Phase 3 | 市场分析 Agent | 市场份额、口碑、渠道策略分析 |
| Phase 4 | 策略建议 Agent | 三维融合，输出差异化定位与行动方案 |

## 技术亮点
- 后端预查询 + 动态上下文注入，LLM 只做语言生成，规避数据幻觉
- 迭代节点实现 1+N 采集，三路并行分析总耗时≈单路
- 代码节点处理 LLM 输出异常（think标签/JSON格式/Extra data）
- 全链路数据溯源，每条结论可追踪至原始搜索来源

## 输出示例
见 output.md

## 技术栈
Dify Workflow · Tavily Search API 
## 效果截图
<img width="2574" height="1162" alt="image" src="https://github.com/user-attachments/assets/4c683b11-cbba-4fc5-abec-1a1ebc194dc7" />

## 工作流架构
<img width="12840" height="1848" alt="竞品分析-whole-workflow" src="https://github.com/user-attachments/assets/bf9a92df-f009-435c-be9a-d30e5b2f3d0b" />

