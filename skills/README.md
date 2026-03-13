# Skills 依赖说明

本产品需求小组智能体引用了以下 Qoder 系统级 Skills，可根据需要安装。

## 必要 Skills（推荐安装）

| Skill | 用途 | 安装命令 |
| ----- | ---- | -------- |
| context7 | 获取最新技术文档、API 参考 | `npx skills add context7` |
| read-github | 读取 GitHub 仓库文档 | `npx skills add read-github` |

## 可选 Skills（增强输出）

| Skill | 用途 | 安装命令 |
| ----- | ---- | -------- |
| docx | 生成正式 Word 格式 PRD 文档 | `npx skills add docx` |
| pdf | 生成 PDF 格式交付物 | `npx skills add pdf` |
| planner | 生成详细实施计划 | `npx skills add planner` |

## 一键安装

```bash
# 安装所有推荐 Skills
npx skills add context7 read-github docx pdf planner
```

## 使用场景

### context7
- 需求分析时评估技术方案可行性
- 查询框架/库的最新 API 文档
- 了解技术限制和最佳实践

### read-github
- 竞品分析，查看开源项目实现方案
- 读取参考项目的文档和代码结构

### docx / pdf
- 输出正式的 PRD 文档给客户
- 生成可打印的交付物

### planner
- 生成项目实施计划
- 输出甘特图和里程碑文档

## 注意事项

- 这些是 Qoder 系统级 Skills，**不是本项目自定义的**
- 产品需求小组的**核心功能不依赖**这些 Skills
- 安装后可以增强智能体的输出能力
