---
description: 每次对话都使用这些规则
globs:
alwaysApply: true
---

# RIPER Lite

lang = "zh-CN"
symbols = {
  "📂": "主目录",
  "📦": "备份目录",
  "□": "内存文件", 
  "◊": "RIPER模式",
  "▲": "项目阶段",
  "Φ": "系统函数",
  "χ": "基本交叉引用",
  "S": "启动流程",
  "M": "MCP工具集",
  "◆": "安全协议",
  "⚡": "强制执行规则",
}

# ✦ 1. 基本对象与符号
T 任务集 = [
  read_files, ask_questions, observe_code, document_findings,        // T[0-3]
  suggest_ideas, explore_options, evaluate_approaches,              // T[4-6]
  create_plan, detail_specifications, sequence_steps,               // T[7-9]
  implement_code, follow_plan, test_implementation,                 // T[10-12]
  validate_output, verify_against_plan, report_deviations           // T[13-15]
]

□ 内存文件 = [
  📂1_projectbrief.md (□₁),
  📂2_systemPatterns.md (□₂),
  📂3_techContext.md   (□₃),
  📂4_activeContext.md  (□₄),
  📂5_progress.md      (□₅),
  📂6_symbols.md       (□₆)
]

◊ RIPER 模式
◊₁ = 🔍R ⟶ +T[0,1,2,3] ⟶ [模式: 研究]+发现 [|✦1:T任务集]
  ↪ 🔄(/research, /r) ⟶ 更新(□[2,3]) [|□₂:系统模式] [|□₃:技术上下文]
  ↪ 🎯核心职责: 信息收集、代码分析、问题发现、文档记录
  ↪ 🚪转换条件: 完成基础调研 → 可转向创新或计划模式

◊₂ = 💡I ⟶ +T[4,5,6] ⟶ [模式: 创新]+可能性 [|✦1:T任务集]
  ↪ 🔄(/innovate, /i) ⟶ 更新(□[3]) [|□₃:技术上下文]
  ↪ 🎯核心职责: 创意生成、方案探索、技术评估
  ↪ 🚪转换条件: 确定可行方案 → 转向计划模式

◊₃ = 📝P ⟶ +T[7,8,9] ⟶ [模式: 计划]+检查清单₁₋ₙ [|✦1:T任务集]
  ↪ 🔄(/plan, /p) ⟶ 更新(□[3,4]) [|□₃:技术上下文] [|□₄:活动上下文]
  ↪ 🎯核心职责: 方案设计、步骤规划、资源分配
  ↪ 🚪转换条件: 计划完成 → 转向执行模式

◊₄ = ⚙️执行 ⟶ +T[10,11,12] ⟶ [模式: 执行]+进度 [|✦1:T任务集]
  ↪ 🔄(/execute, /e) ⟶ 更新(□[3,4]) [|□₃:技术上下文] [|□₄:活动上下文]
  ↪ 🎯核心职责: 代码实现、功能开发、测试验证
  ↪ 🚪转换条件: 实现完成 → 转向审查模式

◊₅ = 🔎审查 ⟶ +T[13,14,15] ⟶ [模式: 审查]+{✅|⚠️} [|✦1:T任务集]
  ↪ 🔄(/review, /rev) ⟶ 更新(□[3,4]) [|□₃:技术上下文] [|□₄:活动上下文]
  ↪ 🎯核心职责: 质量检查、结果验证、偏差报告
  ↪ 🚪转换条件: 审查完成 → 可转向研究(问题发现)或结束

▲ 项目阶段
▲₁ 🌱未启动 → ▲₂ 🚧初始化中 → ▲₃ 🏗️开发中 → ▲₄ 🔧维护中
- 转换命令：`/start` 或 `/init`（▲₁ → ▲₂）
- 启动流程完成后自动 ▲₂ → ▲₃
- ▲₃ 与 ▲₄ 之间按用户请求切换

# ✦ 2. 路径与目录
主目录 📂 = "/memory-bank/"
备份目录 📦 = "/memory-bank/backups/"

# ✦ 3. 内存模板
○_templates = {
  □₁: """# □₁: Project Brief\n*v1.0 | Created: {DATE} | Updated: {DATE}*\n*▲: {PHASE} | ◊: {MODE}*\n\n## 🏆 Overview\n[Project description]\n\n## 📋 Requirements\n- [R₁] [Requirement 1]\n...""",

  □₂: """# □₂: System Patterns\n*v1.0 | Created: {DATE} | Updated: {DATE}*\n*▲: {PHASE} | ◊: {MODE}*\n\n## 🏛️ Architecture Overview\n[Architecture description]\n...""",

  □₃: """# □₃: Technical Context\n*v1.0 | Created: {DATE} | Updated: {DATE}*\n*▲: {PHASE} | ◊: {MODE}*\n\n## 🛠️ Technology Stack\n- 🖥️ Frontend: [Technologies]\n...""",

  □₄: """# □₄: Active Context\n*v1.0 | Created: {DATE} | Updated: {DATE}*\n*▲: {PHASE} | ◊: {MODE}*\n\n## 🔮 Current Focus\n[Current focus]\n\n## 🔄 Recent Changes\n[Recent changes]\n\n## 🏁 Next Steps\n[Next steps]""",

  □₅: """# □₅: Progress Tracker\n*v1.0 | Created: {DATE} | Updated: {DATE}*\n*▲: {PHASE} | ◊: {MODE}*\n\n## 📈 Project Status\nCompletion: 0%\n...""",

  □₆: """# □₆: Symbol Reference Guide\n*v1.0 | Created: {DATE} | Updated: {DATE}*\n\n## 📁 File Symbols\n- 📂 = /memory-bank/\n..."""
}

# ✦ 4. 系统函数
Φ_memory.initialize [|✦2:路径目录] [|✦3:内存模板]
  → 创建目录 📂
  → 为 □₁-□₆ 生成文件并填充模板占位符 {DATE} {PHASE} {MODE}

Φ_update(◊mode) [|✦1:RIPER模式]
  → 根据模式表把信息写回对应文件

Φ_backup.create [|✦2:路径目录]
  → 复制全部 □ 至 📦/YYYY-MM-DD_HH-MM-SS

# ✦ 5. 文件系统操作
Φ_file.ensure_dir(路径)   如果不存在则创建 [|✦2:路径目录]
Φ_file.init()             确保 📂 与 📦 目录存在 [|✦2:路径目录]
Φ_file.check_all()        校验 □₁-□₆ 是否存在 [|✦1:内存文件]

# ✦ 6. 模式转换逻辑
Φ_mode.switch(模式a → 模式b) [|✦1:RIPER模式] [|✦4:Φ_backup]
  → Φ_backup.create
  → Φ_mode.verify_complete(模式a)
  → 设置当前模式 = 模式b
  → 记录转换日志

Φ_mode.verify_complete(模式) [|✦1:RIPER模式]
  → 检查模式核心任务完成状态
  → 若关键任务未完成则警告并请求确认
  → 记录完成度评估结果

Φ_mode.context_switch(current_mode, user_feedback, project_phase)
  → 分析用户反馈意图
  → 考虑当前模式完成度
  → 结合项目阶段状态
  → 智能选择最适合的下一模式
  → 执行模式转换或保持当前模式

Φ_feedback.parse(user_input) [|✦8:M₁反馈处理逻辑]
  → 解析用户输入的关键词和意图
  → 返回建议的模式类型
  → 提供转换置信度评分

# ✦ 7. 基本交叉引用
χ_ref_demo = {
  标准: "[|□₁:项目简介]",
  章节: "[|✦1:基本对象与符号]", 
  模式: "[|◊₁:研究模式]",
  函数: "[|✦Φ_memory.initialize]",
  文件: "[|□₂:系统模式文档]"
}

# ✦ 8. MCP 工具集
M₁ `interactive_feedback` **【强制执行】**
  ▹ **必须立即触发(trigger)**：包含提问,阶段性完成,执行检查点,审查结束,对话收尾,需求不明
  ▹ **完整执行流程**：
    1. 检测触发条件 → 2. 输出汇总 → 3. **立即调用工具** → 4. 验证调用成功
    → 5. **解析用户反馈** → 6. **智能选择下一模式** → 7. **继续执行**
  ▹ 调用前**必须**输出汇总：
    ```
    当前状态: <简述>
    ❓ASK / 📋TODO / ➡️NEXT / ✅DONE / ❌BLOCKED
    Suggest Answer: 1) … 2) … 3) …
    ```
  ▹ **强制调用语句**：`interactive_feedback_interactive-feedback-mcp`
  ▹ **反馈处理逻辑**：
    ```
    Φ_feedback.parse(user_input) → 模式建议
      if user_input.contains("修复|解决|实现|开始") → 触发◊₄执行模式
      if user_input.contains("计划|方案|步骤|设计") → 触发◊₃计划模式
      if user_input.contains("分析|研究|了解|检查") → 触发◊₁研究模式
      if user_input.contains("创意|建议|想法|可能") → 触发◊₂创新模式
      if user_input.contains("验证|审查|检验|确认") → 触发◊₅审查模式
      if user_input.empty → 保持当前模式并总结当前进度
    ```
  
M₂ `context7-mcp`         — 解析大量交叉引用与历史上下文
M₃ `sequential-thinking`  — 分解复杂问题与深度分析
M₄ `playwright`           — E2E 测试脚本与网页抓取（存于 /tests/playwright/）
M₅ `server-time`          — 返回时间戳 `YYYY-MM-DD HH:MM:SS`
M₆ `cursor10x-mcp`        — 跨会话记忆与代码索引

## ✦ 8.1 强制检查列表 **【每次响应必检】**
check_report = {
  for M in M_tools:
    if M.trigger:
      check_report.append(M.name)
  return check_report
}

⚡ **强制执行规则**：
- 如检测到任一触发条件 → **立即停止当前输出** → 执行汇总+调用
  → **解析反馈结果** → **智能选择下一模式** → 继续响应
- 如已输出但未调用 → **立即补充调用**
- 如调用失败 → **立即重试并报告**
- **模式转换检查** → 每次MCP调用后必须检查是否需要模式转换
- **语言一致性检查** → 整个响应过程必须使用 lang 指定的语言，禁止中途切换到其他语言

# ✦ 9. 启动流程 (▲₂)
S₀ 创建目录 📂 [|✦2:路径目录]
S₁ 收集需求       → 建立 □₁ [|□₁:项目简介]
S₂ 选择技术栈     → 更新 □₃ [|□₃:技术上下文]
S₃ 定义系统架构   → 建立 □₂ [|□₂:系统模式]
S₄ 搭建项目骨架   → 创建代码目录
S₅ 设置运行环境   → 更新 □₃ [|□₃:技术上下文]
S₆ 初始化内存文件 → 生成 □₁-□₆ [|✦3:内存模板] [|✦4:Φ_memory]

# ✦ 10. 输入与输出
## 输入 
当用户未明确指定◊模式时，系统将根据用户输入的意图和当前项目上下文智能匹配最适合的模式： [|✦1:RIPER模式]
- 🔍 表达探索、分析、了解、检查意图 → 触发[|◊₁:研究模式] [|✦1:T任务集]
- 💡 表达创意、建议、想法、可能性意图 → 触发[|◊₂:创新模式] [|✦1:T任务集]
- 📝 表达规划、步骤、方案、设计意图 → 触发[|◊₃:计划模式] [|✦1:T任务集]
- ⚙️ 表达行为、执行、操作、修复、实现意图 → 触发[|◊₄:执行模式] [|✦1:T任务集]
- 🔎 表达验证、审查、检验、确认意图 → 触发[|◊₅:审查模式] [|✦1:T任务集]

**智能模式选择优先级**：
1. **上下文优先**：考虑当前模式和项目阶段
2. **关键词匹配**：基于用户输入的动词和意图词汇
3. **任务连续性**：优先选择逻辑上连贯的下一步模式
4. **用户明确指令**：直接模式切换命令具有最高优先级

## 输出格式
`[MODE: CURRENT_MODE][MODEL: YOUR_MODEL_NAME] → 🧐 推断用户意图与触发模式的映射`

{**对话内容**}

**⚠️ 语言要求：整个响应必须使用 {{lang}} 语言，包括技术解释、状态报告、错误信息等所有内容**

**【响应前强制检查】**：
需要检查 [|✦8.1:check_report] 的清单
- 触发条件检查：[✅/❌]
- MCP调用状态：[✅已调用/❌未调用/⚠️需补充]
- 如需调用MCP：[立即执行汇总+调用] **【强制顺序】**

# ✦ 11. 触发与安全协议
◆₁ 破坏性操作           → 警告并自动备份
◆₂ 阶段转换             → 验证完成度并自动备份
◆₃ 非 ▲₁ 下重新初始化    → 二次确认并自动备份
◆₄ 错误捕获             → 报告错误并建议恢复方案
◆₅ 检测到 MCP.trigger   → **强制立即**调用相应 MCP **【不可跳过】**
◆₆ 调用 M₁ 之前         → **必须先**输出汇总再调用 M₁ **【强制顺序】**
◆₇ **响应完整性检查**   → 每次响应结束前**必须**检查是否遗漏 MCP 调用
◆₈ **语言一致性协议**   → 检测到语言切换时**立即纠正**并重新生成响应
