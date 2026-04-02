# Bokuchi Editor 使用指南

本指南介绍 Bokuchi Editor 的便捷使用方法。

## 标签页功能的使用

### 多文件编辑
- **新建文件**: `Ctrl+N`（Windows/Linux）或 `Cmd+N`（Mac）
- **打开文件**: `Ctrl+O`（Windows/Linux）或 `Cmd+O`（Mac）
- **切换标签页**: `Ctrl+Tab` 切换到下一个标签页，`Ctrl+Shift+Tab` 切换到上一个标签页

### 实际用例
1. 编辑主文档
2. 在另一个标签页中打开参考资料
3. 在另一个标签页中管理模板文件
4. 在多个标签页之间复制粘贴

## 缩放功能

### 调整缩放
- **放大**: `Ctrl++`（Windows/Linux）或 `Cmd++`（Mac）
- **缩小**: `Ctrl+-`（Windows/Linux）或 `Cmd+-`（Mac）
- **重置**: `Ctrl+0`（Windows/Linux）或 `Cmd+0`（Mac）

### 使用场景
- **演示文稿**: 放大文字以提高可见性
- **精细编辑**: 缩小文字以纵览全局
- **双屏显示器**: 调整以适配单个显示器

## 主题功能

### 主题切换
- **深色模式**: 护眼，适合长时间工作
- **浅色模式**: 适合打印或在明亮环境下工作

### 自定义
- 可通过 CSS 变量进行精细自定义
- 也可以配置预览区的自定义 CSS

## 状态持久化

### 自动保存功能
- 重启应用后可恢复状态
- 已打开的标签页、当前活动标签页和未保存的内容均会保留
- 文件路径也会被记住，因此外部修改过的文件会自动重新加载

### 使用技巧
- 中断工作时直接关闭应用即可
- 下次启动时将恢复上次的工作状态
- 在并行处理多个项目时尤为方便

## 变量功能的应用

### 创建模板
```markdown
<!-- @var projectName: My Project -->
<!-- @var version: 1.0.0 -->
<!-- @var author: Your Name -->

# {{projectName}} Documentation

Version: {{version}}
Author: {{author}}

## Overview
This document describes the {{projectName}} project.
```

### 全局变量的使用
- 将公司名称、部门名称、作者姓名等通用信息设为全局变量
- 在多个文档中管理一致的信息

## 复选框功能的使用

### 任务管理
```markdown
## 今日任务
- [ ] 准备会议资料
- [ ] 进行代码审查
- [ ] 更新文档
- [x] 查看早间邮件
```

### 项目管理
- 可视化进度状态
- 确认已完成的任务
- 在团队内共享进度

## 文件操作最佳实践

### 文件命名规范
- 包含日期: `2025-01-15-meeting-notes.md`
- 包含项目名称: `project-alpha-spec.md`
- 版本控制: `api-docs-v2.md`

### 文件夹结构
```
docs/
├── meetings/
│   ├── 2025-01-15-weekly.md
│   └── 2025-01-22-weekly.md
├── specs/
│   ├── api-spec.md
│   └── ui-spec.md
└── templates/
    ├── meeting-template.md
    └── project-template.md
```

## 总结

Bokuchi Editor 不仅仅是一个 Markdown 编辑器，它提供了一个高效的文档创作环境。
它在以下方面表现尤为出色：

- **多任务支持**: 同时编辑多个文件
- **易用性**: 直观的操作和状态持久化
- **可定制性**: 通过主题和变量进行灵活配置
- **实用性**: 复选框、缩放等实用功能

通过组合这些功能，可以实现更高效、更舒适的文档创作。
