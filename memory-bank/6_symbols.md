# □₆: Symbol Reference Guide
*v1.0 | Created: 2024-12-19 | Updated: 2024-12-19*

## 📁 File Symbols
- **📂** = /memory-bank/ (主目录)
- **📦** = /memory-bank/backups/ (备份目录)
- **□** = 内存文件 (Memory Files)
- **□₁** = projectbrief.md (项目简介)
- **□₂** = systemPatterns.md (系统模式)
- **□₃** = techContext.md (技术上下文)
- **□₄** = activeContext.md (活跃上下文)
- **□₅** = progress.md (进度跟踪)
- **□₆** = symbols.md (符号指南)

## ◊ RIPER Modes (工作模式)
- **◊₁** = 🔍R (研究模式) - 信息收集与分析
- **◊₂** = 💡I (创新模式) - 创意生成与探索
- **◊₃** = 📝P (计划模式) - 方案设计与规划
- **◊₄** = ⚙️E (执行模式) - 代码实现与开发
- **◊₅** = 🔎RV (审查模式) - 质量检查与验证

## ▲ Project Phases (项目阶段)
- **▲₁** = 🌱未启动 (Unstarted)
- **▲₂** = 🚧初始化中 (Initializing)
- **▲₃** = 🏗️开发中 (Development)
- **▲₄** = 🔧维护中 (Maintenance)

## Φ System Functions (系统函数)
- **Φ_memory.initialize** - 内存系统初始化
- **Φ_update(◊mode)** - 模式更新函数
- **Φ_backup.create** - 备份创建函数
- **Φ_mode.switch** - 模式切换函数
- **Φ_file.ensure_dir** - 目录确保函数

## M MCP Tools (工具集)
- **M₁** = interactive_feedback (交互反馈)
- **M₂** = context7-mcp (上下文解析)
- **M₃** = sequential-thinking (序列思维)
- **M₄** = playwright (自动化测试)
- **M₅** = server-time (时间服务)
- **M₆** = cursor10x-mcp (代码索引)

## ◆ Security Protocols (安全协议)
- **◆₁** = 破坏性操作警告
- **◆₂** = 阶段转换验证
- **◆₃** = 重新初始化确认
- **◆₄** = 错误捕获处理
- **◆₅** = MCP触发检测
- **◆₆** = 调用顺序强制
- **◆₇** = 响应完整性检查
- **◆₈** = 语言一致性协议

## χ Cross-Reference (交叉引用)
- **[|□₁:项目简介]** - 引用项目简介文档
- **[|✦1:基本对象]** - 引用章节内容
- **[|◊₁:研究模式]** - 引用特定模式
- **[|Φ_memory.initialize]** - 引用系统函数

## ⚡ Enforcement Rules (强制规则)
- **触发条件检查** - 每次响应前必检
- **MCP调用状态** - 强制执行调用
- **模式转换检查** - 自动验证转换
- **语言一致性** - 全程中文输出

## 🎯 Task Set (任务集)
- **T[0-3]** = 研究任务 (read, ask, observe, document)
- **T[4-6]** = 创新任务 (suggest, explore, evaluate)
- **T[7-9]** = 计划任务 (create, detail, sequence)
- **T[10-12]** = 执行任务 (implement, follow, test)
- **T[13-15]** = 审查任务 (validate, verify, report)

## 📋 Templates (模板集)

### 🎊 初始化成功模板 (initialization_success_template)
```
🎯 当前状态: [🚧初始化中][🔍研究模式] - {PROJECT_NAME} 系统初始化已完成
📊 进度摘要: {COMPLETED_FILES}/{TOTAL_FILES} 核心文件已创建 - {COMPLETION_RATE}% 完成
⚠️ 问题/阻塞: {ISSUES_OR_NONE}
❓ 用户决策点: 确认初始化结果并选择下一步行动

📋 建议选项:
  1) 验证系统 - 测试模式切换功能 ({MODE_COMMANDS})
  2) 开始开发 - 转入开发阶段 (▲₂ → ▲₃)
  3) 自定义配置 - 调整项目需求或技术栈

➡️ 推荐行动: 验证系统功能正常后转入开发阶段

## 🎊 {PROJECT_NAME} 初始化成功！

### ✅ 已完成的工作
1. **目录结构** - 创建了 `{MEMORY_DIR}/` 和 `{BACKUP_DIR}/` 目录
2. **核心文件** - 生成了完整的 {FILE_COUNT} 个内存文件 ({FILE_SYMBOLS})
3. **系统配置** - 建立了 RIPER 工作模式和项目阶段管理
4. **技术栈** - 配置了 MCP 工具集成和符号化表示系统

### 📁 内存文件系统概览
{MEMORY_FILES_LIST}

### 🚀 下一步选择
现在您可以：
- **测试系统** - 尝试模式切换命令 ({MODE_COMMANDS})
- **开始项目** - 转入开发阶段开始实际工作
- **查看文档** - 浏览创建的内存文件了解系统详情
- **自定义配置** - 根据具体需求调整项目设置

{PROJECT_NAME} 现在已准备就绪，可以为您的 AI 辅助开发提供结构化支持！🎯
```

### 📝 模板变量说明
- **{PROJECT_NAME}** - 项目名称 (如: RIPER Lite)
- **{COMPLETED_FILES}** - 已完成文件数量 (如: 6)
- **{TOTAL_FILES}** - 总文件数量 (如: 6)
- **{COMPLETION_RATE}** - 完成百分比 (如: 100)
- **{ISSUES_OR_NONE}** - 问题描述或"无"
- **{MODE_COMMANDS}** - 模式切换命令 (如: /r, /i, /p, /e, /rev)
- **{MEMORY_DIR}** - 内存目录路径 (如: memory-bank)
- **{BACKUP_DIR}** - 备份目录路径 (如: memory-bank/backups)
- **{FILE_COUNT}** - 文件数量 (如: 6)
- **{FILE_SYMBOLS}** - 文件符号列表 (如: □₁-□₆)
- **{MEMORY_FILES_LIST}** - 内存文件详细列表
