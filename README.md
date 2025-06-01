![CursorRIPER♦○-lite](./res/github-header-sigma-lite.png)
# CursorRIPER♦○ Lite 中文版

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
![Version](https://img.shields.io/badge/version-1.0.0-green)

> 一个精简、超高效的AI提示框架，用于软件开发辅助。简化版本，无上下文引用、权限或代码保护功能。

## 📚 概述

CursorRIPER♦○ Lite 是 [CursorRIPER♦○ 框架](https://github.com/johnpeterman72/CursorRIPER.sigma) 的简化版本，保持了核心的RIPER工作流程，同时移除了几个高级功能以提高简洁性和效率。

简化版本排除了：
- 上下文引用系统（@files 功能）
- CRUD权限强制执行
- 代码保护系统

这使得框架更加轻量级，更易于使用，同时仍然为AI辅助开发提供结构化指导。

## 🌟 主要特性

- **符号化表示法**：使用几何符号（◊、▲、○、◆）、下标和表情符号实现极致简洁
- **RIPER工作流模式**：研究、创新、计划、执行、审查（🔍R、💡I、📝P、⚙️E、🔎RV）
- **结构化内存系统**：标准化文件模板
- **基于阶段的项目管理**：从初始化到维护跟踪项目进度
- **自动内存管理**：为项目上下文创建和维护结构化内存库

## 🧠 框架结构

### 模式 (◊)

```
◊₁ = 🔍R ⟶ 研究：收集信息并记录发现
◊₂ = 💡I ⟶ 创新：探索选项并提出想法
◊₃ = 📝P ⟶ 计划：创建规范并排序步骤
◊₄ = ⚙️E ⟶ 执行：根据计划实现代码
◊₅ = 🔎RV ⟶ 审查：根据需求验证输出
```

### 阶段 (▲)

```
▲₁ = 🌱未启动 ⟶ 框架已安装但未开始
▲₂ = 🚧初始化中 ⟶ 设置进行中
▲₃ = 🏗️开发中 ⟶ 主要开发工作
▲₄ = 🔧维护中 ⟶ 长期支持
```

### 内存文件 (□)

```
□₁ = 📋projectbrief.md ⟶ 需求、范围、标准
□₂ = 🏛️systemPatterns.md ⟶ 架构、组件、决策
□₃ = 💻techContext.md ⟶ 技术栈、环境、依赖
□₄ = 🔮activeContext.md ⟶ 焦点、变更、下一步
□₅ = 📊progress.md ⟶ 状态、里程碑、问题
```

## 🚀 快速开始

### 安装

1. 在您的项目中创建内存库目录：

```bash
mkdir -p /memory-bank/backups
```

2. 将 CursorRIPER♦○ Lite 框架 `.mdc` 文件复制到您的项目规则文件夹：`.cursor/rules/`

3. 使用AI助手初始化框架：

```
/start
```

### 使用方法

通过以下命令与AI助手切换模式：

```
/research (或 /r) - 研究模式
/innovate (或 /i) - 创新模式
/plan (或 /p) - 计划模式
/execute (或 /e) - 执行模式
/review (或 /rev) - 审查模式
```

## 📑 内存系统

框架自动维护五个关键内存文件：

1. **项目简介** (□₁)：定义需求、成功标准和范围
2. **系统模式** (□₂)：捕获架构、组件和设计决策
3. **技术上下文** (□₃)：记录技术栈、环境和依赖
4. **活跃上下文** (□₄)：跟踪当前焦点、最近变更和下一步
5. **进度跟踪** (□₅)：监控项目状态、功能、问题和里程碑

## ⚠️ 安全特性

- 破坏性操作前自动备份
- 关键操作的确认提示
- 阶段转换验证
- 错误恢复建议

## 🔣 符号参考

查看 [符号参考指南](./docs/symbol-reference-guide.md) 了解框架中使用的完整符号和表示法列表。

## 📖 文档

- [使用指南](./使用指南.md) - 详细的使用说明
- [符号参考指南](./docs/symbol-reference-guide.md) - 完整的符号说明
- [迁移指南](./docs/migration-guide.md) - 从完整版迁移的指南

## 🤝 贡献

欢迎贡献！请随时提交Pull Request。

## 📄 许可证

本项目采用MIT许可证 - 详见LICENSE文件。

---

*CursorRIPER♦○ Lite 中文版：AI辅助开发的精简符号化效率。*
