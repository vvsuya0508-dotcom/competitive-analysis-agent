# 智能竞品分析多 Agent 系统

基于 Dify Workflow 构建的竞品分析自动化系统，
输入产品名称，自动输出结构化竞品分析报告。

## 系统架构
- Phase 1：竞品发现（关键词生成 + 搜索筛选）
- Phase 2：数据采集（迭代节点逐竞品深度采集）
- Phase 3：并行三路分析（产品 / 定价 / 市场）
- Phase 4：策略建议 + Markdown 报告渲染

## 技术栈
- 工作流平台：Dify
- 搜索工具：Tavily Search API
- LLM：（填你用的模型名称）
- 数据格式：JSON（Agent 间传递）

## 使用方法
1. 下载 `workflow.yml`
2. 在 Dify 中导入 DSL 文件
3. 配置 Tavily API Key 和 LLM
4. 输入产品名称运行

## 输出示例
报告包含七个章节：
战略定位 / 功能矩阵 / 定价对比 / 
市场格局 / 行动计划 / 风险评估 / 综合建议

## 效果截图
<img width="2574" height="1162" alt="image" src="https://github.com/user-attachments/assets/4c683b11-cbba-4fc5-abec-1a1ebc194dc7" />
