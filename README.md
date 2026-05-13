<p align="center">
  <img src="assets/logo.png" alt="Agent Code No.7" width="200"/>
</p>

<h1 align="center">🕵️ Agent Code No.7 — 你的AI特工局</h1>

<p align="center">
  <strong>专为律所 · 会所 · 咨询公司打造的AI特工团队</strong><br/>
  全天候执行高难度办公任务，7×24小时提效引擎
</p>

<p align="center">
  <a href="#快速开始">快速开始</a> •
  <a href="#特工档案">特工档案</a> •
  <a href="#架构设计">架构设计</a> •
  <a href="#演示视频">演示视频</a> •
  <a href="#技术栈">技术栈</a>
</p>

---

## 💡 项目简介

**Agent Code No.7** 是一个基于腾讯 ClawPro 平台构建的多智能体协作系统，以 "AI特工局" 为核心概念，为专业服务机构（律所、会计师事务所、咨询公司）提供一站式智能办公解决方案。

### 痛点洞察

| 行业 | 痛点 | 传统方案 | Agent Code No.7 方案 |
|------|------|----------|---------------------|
| 🏛 律所 | 合同审查耗时、法规检索低效 | 人工逐条对比 | **合同特工**秒级扫描 + 风险标注 |
| 🏢 会所 | 审计底稿繁琐、财报分析复杂 | Excel手工处理 | **审计特工**自动核验 + 异常预警 |
| 📊 咨询公司 | 行研报告周期长、数据散乱 | 多人协作拼凑 | **研究特工**一键生成深度报告 |

### 核心价值

- **🎯 精准执行** — 每位特工专精一个领域，准确率 > 95%
- **⚡ 极速响应** — 复杂任务分钟级完成，传统需数小时
- **🔄 协同作战** — 多特工联动，任务自动编排与分发
- **🔒 安全合规** — 数据不出域，符合专业服务保密要求
- **📈 持续进化** — 基于反馈自优化，越用越聪明

---

## 🕵️ 特工档案

### Agent-01: 合同卫士 (Contract Guardian)
> **专精**: 合同审查、条款风险识别、合规性检查

- 支持中英文合同智能解析
- 自动标注高风险条款（违约金、竞业限制、知识产权归属）
- 生成风险评估报告 + 修改建议
- 对标行业标准模板进行偏离度分析

### Agent-02: 法律猎手 (Legal Hunter)
> **专精**: 法规检索、案例分析、法律意见书生成

- 跨库检索法律法规、司法解释、指导案例
- 智能归纳裁判观点与趋势
- 辅助生成法律意见书框架
- 支持多轮追问式深度研究

### Agent-03: 审计鹰眼 (Audit Eagle)
> **专精**: 财务报表分析、审计底稿、异常检测

- 自动化财报数据提取与交叉验证
- 异常交易智能识别与标记
- 审计底稿模板自动生成
- 支持多会计准则（CAS/IFRS）切换

### Agent-04: 税务管家 (Tax Butler)
> **专精**: 税务筹划、合规审查、申报辅助

- 多税种综合筹划建议
- 税收优惠政策智能匹配
- 纳税申报数据预填与校验
- 跨境税务风险提示

### Agent-05: 研究探员 (Research Scout)
> **专精**: 行业研究、竞品分析、市场洞察

- 多源数据自动采集与清洗
- 行业趋势分析 + 可视化图表生成
- 竞品动态追踪与对标分析
- 深度研究报告一键输出

### Agent-06: 尽调特工 (Due Diligence Agent)
> **专精**: 尽职调查、背景核查、风险评估

- 企业工商/诉讼/知识产权全景扫描
- 关联关系图谱自动生成
- 尽调清单智能管理
- 风险评级与投资建议

### Agent-07: 总指挥 (Commander)
> **专精**: 任务编排、特工调度、质量把控

- 理解复杂需求，智能拆解子任务
- 动态分配最优特工组合
- 结果汇总与质量审核
- 全流程进度追踪与汇报

---

## 🏗 架构设计

```
┌─────────────────────────────────────────────────┐
│                   用户交互层                      │
│         ClawPro 平台 / Web UI / API              │
└──────────────────────┬──────────────────────────┘
                       │
┌──────────────────────▼──────────────────────────┐
│              🕵️ Agent-07 总指挥                   │
│         任务理解 → 拆解 → 分发 → 汇总             │
└──┬────┬────┬────┬────┬────┬─────────────────────┘
   │    │    │    │    │    │
   ▼    ▼    ▼    ▼    ▼    ▼
┌────┐┌────┐┌────┐┌────┐┌────┐┌────┐
│ 01 ││ 02 ││ 03 ││ 04 ││ 05 ││ 06 │  ← 专业特工
│合同││法律││审计││税务││研究││尽调│
└──┬─┘└──┬─┘└──┬─┘└──┬─┘└──┬─┘└──┬─┘
   │     │     │     │     │     │
┌──▼─────▼─────▼─────▼─────▼─────▼───┐
│              工具与知识层              │
│  📚 法规库  📊 财务工具  🔍 搜索引擎  │
│  📝 文档生成  📈 数据分析  🗂 模板库   │
└─────────────────────────────────────┘
```

### 技术架构

```
┌─────────────────────────────────────┐
│          ClawPro 平台层               │
│  ┌─────────┐  ┌──────────────────┐  │
│  │ Agent   │  │  Workflow Engine  │  │
│  │ Runtime │  │  (DAG 编排)       │  │
│  └────┬────┘  └────────┬─────────┘  │
│       │                │            │
│  ┌────▼────────────────▼─────────┐  │
│  │      Prompt Engineering       │  │
│  │   (CoT / ReAct / Reflection)  │  │
│  └────┬──────────────────────────┘  │
│       │                             │
│  ┌────▼────────────────────────┐    │
│  │    Tool Calling Layer       │    │
│  │  文档解析 │ 搜索 │ 计算     │    │
│  └─────────────────────────────┘    │
└─────────────────────────────────────┘
```

---

## 🎬 演示视频

> 📹 [点击观看演示视频](demo/video/)

演示场景：
1. **合同审查全流程** — 上传合同 → 风险扫描 → 生成报告（2分钟完成传统4小时工作）
2. **多特工协作尽调** — 输入公司名 → 6位特工并行调查 → 汇总完整尽调报告
3. **智能法律研究** — 提出法律问题 → 法规检索 → 案例分析 → 意见书生成

---

## 🚀 快速开始

### 在 ClawPro 平台使用

1. 下载安装 [ClawPro 桌面客户端](https://openclawpro.cn/)
2. 配置 AI 模型 API Key（支持 OpenAI / 通义千问 / DeepSeek 等）
3. 克隆本仓库，将 `skills/` 目录下的技能文件夹复制到 `~/.openclaw/skills/`
4. 将 `workspace/` 下的配置文件复制到 `~/.openclaw/workspace/`
5. 重启 ClawPro，开始使用！

### 本地安装

```bash
# 克隆仓库
git clone https://github.com/monarchmio/agent-code-no7.git
cd agent-code-no7

# 复制技能到 OpenClaw 目录（Windows）
xcopy skills\* %USERPROFILE%\.openclaw\skills\ /E /I

# 复制工作区配置
xcopy workspace\* %USERPROFILE%\.openclaw\workspace\ /E /I

# macOS/Linux
# cp -r skills/* ~/.openclaw/skills/
# cp -r workspace/* ~/.openclaw/workspace/
```

---

## 📁 项目结构

```
agent-code-no7/
├── README.md                       # 项目说明
├── LICENSE                         # MIT License
├── skills/                         # ⭐ OpenClaw 技能（SKILL.md 格式）
│   ├── commander/SKILL.md          # Agent-07 总指挥
│   ├── contract-guardian/SKILL.md  # Agent-01 合同卫士
│   ├── legal-hunter/SKILL.md       # Agent-02 法律猎手
│   ├── audit-eagle/SKILL.md        # Agent-03 审计鹰眼
│   ├── tax-butler/SKILL.md         # Agent-04 税务管家
│   ├── research-scout/SKILL.md     # Agent-05 研究探员
│   └── due-diligence/SKILL.md      # Agent-06 尽调特工
├── workspace/                      # ⭐ OpenClaw 工作区配置
│   ├── AGENTS.md                   # Agent 指令说明
│   ├── IDENTITY.md                 # 身份与人格
│   ├── USER.md                     # 用户偏好
│   └── MEMORY.md                   # 长期记忆
├── agents/                         # Agent 配置文件（JSON 格式）
│   ├── commander.json              # Agent-07 总指挥
│   ├── contract_guardian.json      # Agent-01 合同卫士
│   ├── legal_hunter.json           # Agent-02 法律猎手
│   ├── audit_eagle.json            # Agent-03 审计鹰眼
│   ├── tax_butler.json             # Agent-04 税务管家
│   ├── research_scout.json         # Agent-05 研究探员
│   └── due_diligence_agent.json    # Agent-06 尽调特工
├── prompts/                        # Prompt 模板
├── workflows/                      # 工作流定义（JSON）
├── knowledge/                      # 知识库配置
├── docs/                           # 文档
│   ├── architecture.md             # 架构设计文档
│   ├── user_guide.md               # 使用指南
│   └── demo_script.md              # 演示脚本
├── assets/                         # 静态资源
└── demo/                           # 演示材料
```

---

## 🛠 技术栈

| 组件 | 技术 |
|------|------|
| AI 平台 | [ClawPro](https://openclawpro.cn/) (OpenClaw 桌面客户端) |
| 大模型 | 腾讯混元 / DeepSeek / OpenAI / 通义千问 |
| Agent 框架 | OpenClaw Agent + SKILL.md 技能系统 |
| 技能生态 | ClawHub 技能市场 (55+ 内置技能) |
| Prompt 策略 | Chain-of-Thought + ReAct + Reflection |
| 多通道接入 | 飞书 / 企业微信 / Telegram / Discord |
| 文档处理 | PDF/DOCX/XLSX 解析 |
| 知识库 | RAG (检索增强生成) |

---

## 🏆 竞赛信息

- **赛事**: 腾讯黑客松
- **作品名**: Agent Code No.7
- **赛道**: ClawPro 平台应用
- **团队理念**: 用 AI 特工团队重新定义专业服务效率

---

## 📞 联系我们

如有问题或合作意向，请通过 Issues 联系。

---

<p align="center">
  <strong>🕵️ Agent Code No.7 — 每一次任务，使命必达</strong>
</p>
