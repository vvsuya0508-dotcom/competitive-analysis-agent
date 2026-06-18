# 智能竞品分析多 Agent 系统

> 输入产品名称，自动完成竞品发现、多源数据采集、
> 三维并行分析，输出七章结构化竞品报告

🔗 **在线体验workflow**：https://udify.app/workflow/HMXQClIozD3KfseH 
（输入"飞书"或任意产品名即可体验）
🔗 **在线体验chatflow**：https://vvsuya0508-dotcom.github.io/competitive-analysis-agent/  
## 项目背景
针对竞品调研过程中信息分散、人工整理耗时的痛点，系统拆解竞品分析全流程，抽象出竞品发现、信息采集、产品分析、定价分析、市场分析、策略建议六大核心任务，完成 Agent 产品方案设计与 MVP 规划，验证 LLM 在复杂调研场景中的应用价值。
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
<img width="3180" height="1904" alt="047eb52fd10e3326a5526c588364fa2b" src="https://github.com/user-attachments/assets/f8841167-6518-4907-a1d7-f501561f9954" />
<img width="2596" height="1790" alt="image" src="https://github.com/user-attachments/assets/10061676-bf4a-42f9-9dd5-5397de26c056" />

## 工作流架构
<img width="12840" height="1848" alt="竞品分析-whole-workflow" src="https://github.com/user-attachments/assets/bf9a92df-f009-435c-be9a-d30e5b2f3d0b" />
<img width="16384" height="1554" alt="327b26044c038aa6e7852d9f1b7d3396" src="https://github.com/user-attachments/assets/53d23a39-a84f-43c3-b3e9-05518897a71b" />

## 使用方法

**方式一：直接体验**
点击上方 Demo 链接，输入产品名称即可

**方式二：导入 Dify**
1. 下载 chatflow/chatflow.yml
2. Dify 工作室 → 导入 DSL 文件
3. 配置 Tavily API Key 和 LLM
4. 发布运行

**方式三：本地部署网页**
1. 下载 web/index.html
2. 填入你的 Dify API Key
3. 浏览器直接打开
