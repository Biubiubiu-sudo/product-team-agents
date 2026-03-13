# Product Team Agents

基于 Qoder 的**产品需求小组多智能体协作框架**，一键生成专业级 PRD 文档和 UI 设计提示词。

## 特点

- **5 角色协作**：产品负责人 + 需求分析师 + PRD专家 + UI设计师 + 评审专家
- **自动化流程**：从需求澄清到文档交付，全程自动协作
- **质量保障**：内置评审机制，确保输出质量
- **知识沉淀**：越用越了解你的偏好和项目规则

## 角色介绍

| 角色 | 职责 |
| ---- | ---- |
| **Product Owner** | 协调整个团队，调度各专家完成任务 |
| **Requirement Analyst** | 拆解功能模块，编写用户故事，梳理业务流程 |
| **PRD Writer** | 撰写详细的产品需求文档 |
| **UI Designer** | 输出可用于 AI 绘图工具的 UI 提示词 |
| **PRD Reviewer** | 独立评审 PRD 质量，确保可执行性 |

## 安装

### 1. 复制智能体文件

将 `agents/` 目录下的所有 `.md` 文件复制到：

```bash
# 全局安装（推荐）
cp agents/*.md ~/.qoder/agents/

# 或项目级安装
cp agents/*.md .qoder/agents/
```

### 2. 复制知识文件

```bash
# 全局安装
cp knowledge/*.md ~/.qoder/knowledge/

# 或项目级安装
cp knowledge/*.md .qoder/knowledge/
```

### 3. 安装可选 Skills（增强能力）

```bash
npx skills add context7 read-github docx pdf planner
```

详见 [skills/README.md](skills/README.md)

## 使用方法

在 Qoder 中直接调用产品负责人：

```
/product-owner 我需要做一个xxx系统
```

产品负责人会自动协调团队完成：
1. 需求澄清（不限次数追问，直到完全理解）
2. 需求分析（输出结构化分析文档）
3. PRD 撰写（每个功能模块独立文档）
4. UI 设计（每个页面独立提示词）
5. 质量评审（独立评审，确保可执行）

## 目录结构

```
product-team-agents/
├── agents/                      # 智能体入口文件
│   ├── product-owner.md         # 产品负责人（主入口）
│   ├── requirement-analyst.md   # 需求分析师
│   ├── prd-writer.md            # PRD专家
│   ├── ui-designer.md           # UI设计师
│   └── prd-reviewer.md          # 评审专家
├── knowledge/                   # 工作手册
│   ├── product-owner-guide.md
│   ├── requirement-analyst-guide.md
│   ├── prd-writer-guide.md
│   ├── ui-designer-guide.md
│   ├── USER_PROFILE.md          # 用户偏好模板
│   └── PROJECT_RULES.md         # 项目规则模板
└── skills/                      # Skills 依赖说明
    └── README.md
```

## 输出示例

使用本框架后，你将获得：

```
项目名称-产品需求/
├── 需求分析/
│   ├── 00-进度追踪.md
│   ├── 01-功能模块清单.md
│   ├── 02-用户故事.md
│   ├── 03-业务流程.md
│   └── ...
├── PRD/
│   ├── 00-进度追踪.md
│   ├── 01-产品概述.md
│   ├── 04-功能模块-[模块名].md  # 每个模块独立文件
│   └── ...
├── UI/
│   ├── 00-进度追踪.md
│   ├── XX-页面-[页面名].md      # 每个页面独立文件
│   └── ...
└── 评审/
    └── 评审报告.md
```

## 环境要求

- [Qoder](https://qoder.ai) IDE

## License

MIT
