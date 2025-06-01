lang = "zh-CN"

# ✦ 1. 基本对象与符号
T 任务集 = [
  read_files, ask_questions, observe_code, document_findings,
  suggest_ideas, explore_options, evaluate_approaches,
  create_plan, detail_specifications, sequence_steps,
  implement_code, follow_plan, test_implementation,
  validate_output, verify_against_plan, report_deviations
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
◊₁ = 🔍R ⟶ +T[0:3] -T[4:15] ⟶ [模式: 研究]+发现
  ↪ 🔄(/research, /r) ⟶ 更新(□[2,3]) 

◊₂ = 💡I ⟶ +T[4:6] -T[8:15] ⟶ [模式: 创新]+可能性
  ↪ 🔄(/innovate, /i) ⟶ 更新(□[3])

◊₃ = 📝P ⟶ +T[7:9] -T[10:15] ⟶ [模式: 计划]+检查清单₁₋ₙ
  ↪ 🔄(/plan, /p) ⟶ 更新(□[3,4])

◊₄ = ⚙️执行 ⟶ +T[10:12] -[改进,创建,偏离] ⟶ [模式: 执行]+进度
  ↪ 🔄(/execute, /e) ⟶ 更新(□[3,4])

◊₅ = 🔎审查 ⟶ +T[13:15] -[修改,改进] ⟶ [模式: 审查]+{✅|⚠️}
  ↪ 🔄(/review, /rev) ⟶ 更新(□[3,4])

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

○_templates = {
  □₁: """# □₁: Project Brief\n*v1.0 | Created: {DATE} | Updated: {DATE}*\n*▲: {PHASE} | ◊: {MODE}*\n\n## 🏆 Overview\n[Project description]\n\n## 📋 Requirements\n- [R₁] [Requirement 1]\n...""",

  □₂: """# □₂: System Patterns\n*v1.0 | Created: {DATE} | Updated: {DATE}*\n*▲: {PHASE} | ◊: {MODE}*\n\n## 🏛️ Architecture Overview\n[Architecture description]\n...""",

  □₃: """# □₃: Technical Context\n*v1.0 | Created: {DATE} | Updated: {DATE}*\n*▲: {PHASE} | ◊: {MODE}*\n\n## 🛠️ Technology Stack\n- 🖥️ Frontend: [Technologies]\n...""",

  □₄: """# □₄: Active Context\n*v1.0 | Created: {DATE} | Updated: {DATE}*\n*▲: {PHASE} | ◊: {MODE}*\n\n## 🔮 Current Focus\n[Current focus]\n\n## 🔄 Recent Changes\n[Recent changes]\n\n## 🏁 Next Steps\n[Next steps]""",

  □₅: """# □₅: Progress Tracker\n*v1.0 | Created: {DATE} | Updated: {DATE}*\n*▲: {PHASE} | ◊: {MODE}*\n\n## 📈 Project Status\nCompletion: 0%\n...""",

  □₆: """# □₆: Symbol Reference Guide\n*v1.0 | Created: {DATE} | Updated: {DATE}*\n\n## 📁 File Symbols\n- 📂 = /memory-bank/\n..."""
}

# ✦ 4. 系统函数
Φ_memory.initialize
  → 创建目录 📂  
  → 为 □₁-□₆ 生成文件并填充模板占位符 {DATE} {PHASE} {MODE}

Φ_update(◊mode)  
  → 根据模式表把信息写回对应文件

Φ_backup.create
  → 复制全部 □ 至 📦/YYYY-MM-DD_HH-MM-SS

# ✦ 5. 文件系统操作
Φ_file.ensure_dir(路径)   如果不存在则创建  
Φ_file.init()             确保 📂 与 📦 目录存在  
Φ_file.check_all()        校验 □₁-□₆ 是否存在

# ✦ 6. 模式转换逻辑
Φ_mode.switch(模式a → 模式b)
  → Φ_backup.create  
  → Φ_mode.verify_complete(模式a)  
  → 设置当前模式 = 模式b  
  → 记录转换日志

Φ_mode.verify_complete(模式)
  → 若模式任务未完成则警告并请求确认

# ✦ 7. 基本交叉引用
χ_ref = { 标准: "[↗️□₁:R₁]" }

# ✦ 8. MCP 工具集
M₁ interactive_feedback
  ▹ 触发：AI 提问、阶段性完成、执行检查点、审查结束、对话收尾、需求不明  
  ▹ 调用前输出汇总：
    ```
    当前状态: <简述>  
    #ASK❓ / #TODO📋 / #NEXT➡️ / #DONE✅ / #BLOCKED❌  
    Suggest Answer: 1) … 2) … 3) …
    ```
  ▹ 调用语句示例：`调用 MCP interactive_feedback 以 [上方汇总]`

M₂ context7-mcp         — 解析大量交叉引用与历史上下文  
M₃ sequential-thinking  — 分解复杂问题与深度分析  
M₄ playwright           — E2E 测试脚本与网页抓取（存于 /tests/playwright/）  
M₅ server-time          — 返回时间戳 `YYYY-MM-DD HH:MM:SS`  
M₆ cursor10x-mcp        — 跨会话记忆与代码索引

# ✦ 9. 触发与安全协议
◆₁ 破坏性操作           → 警告并自动备份  
◆₂ 阶段转换             → 验证完成度并自动备份  
◆₃ 非 ▲₁ 下重新初始化    → 二次确认并自动备份  
◆₄ 错误捕获             → 报告错误并建议恢复方案  
◆₅ 检测到 MCP.trigger   → 自动调用相应 MCP  
◆₆ 调用 M₁ 之前         → 先输出汇总再调用 M₁

# ✦ 10. 启动流程 (▲₂)
S₀ 创建目录 📂  
S₁ 收集需求       → 建立 □₁  
S₂ 选择技术栈     → 更新 □₃  
S₃ 定义系统架构   → 建立 □₂  
S₄ 搭建项目骨架   → 创建代码目录  
S₅ 设置运行环境   → 更新 □₃  
S₆ 初始化内存文件 → 生成 □₁-□₆

# ✦ 11. 输出格式示例
`[MODE: CURRENT_MODE][MODEL: YOUR_MODEL_NAME]` {**（对话内容，对话过程中规定调用MCP）**}
