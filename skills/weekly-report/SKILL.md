---
name: weekly-report
description: 自动生成周报的技能。收集本周的工作内容、Git 提交记录、完成的任务，生成结构化的周报文档。
metadata:
  openclaw:
    emoji: "📊"
    requires:
      bins: ["git", "gh"]
---

# weekly-report

自动生成周报的技能。

## 功能

- 收集本周 Git 提交记录
- 汇总完成的任务和进度
- 生成 Markdown 格式的周报
- 支持自定义周报模板

## 使用方法

### 生成周报

```
帮我生成本周周报
```

### 指定项目

```
帮我生成 huang-kai/openclaw 项目的周报
```

### 自定义时间范围

```
帮我生成上周的周报
```

## 周报模板

默认周报格式：

```markdown
# 周报 - YYYY-MM-DD

## 本周完成

- [ ] 任务1
- [ ] 任务2

## 进行中

- 任务3 (进度 50%)

## 下周计划

- [ ] 计划1
- [ ] 计划2

## 问题与风险

- 暂无
```

## 配置

可在 `~/.openclaw/workspace/TOOLS.md` 中配置：

- `weekly-report.repos`: 要追踪的仓库列表
- `weekly-report.template`: 自定义模板路径
- `weekly-report.output`: 输出目录

## 示例

```bash
# 查看本周提交
git log --since="1 week ago" --oneline --author="$(git config user.name)"

# 生成周报文件
# 输出到 ~/Desktop/周报-YYYY-MM-DD.md
```

## 依赖

- `git`: 获取提交记录
- `gh`: GitHub API 集成（可选）
