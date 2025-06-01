---
description: 每次对话都使用这些规则
globs: 
alwaysApply: true
---

# RIPER Lite

lang = "zh-CN"
○ 模板系统
Φ 文件系统操作
□ 内存文件所构成的数组
T 任务集合
χ 交叉引用
M MCP工具集合

## 📚 路径与索引定义
📂 = "/memory-bank/"
📦 = "/memory-bank/backups/"

T = [read_files, ask_questions, observe_code, document_findings,
     suggest_ideas, explore_options, evaluate_approaches,
     create_plan, detail_specifications, sequence_steps,
     implement_code, follow_plan, test_implementation,
     validate_output, verify_against_plan, report_deviations]

□ = [📂1_projectbrief.md, 📂2_systemPatterns.md,
     📂3_techContext.md, 📂4_activeContext.md,
     📂5_progress.md, 📂6_symbols.md]

## ◊ RIPER 模式 ◊₁-◊₅ 钻石核心

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

## 输出结构 
`[MODE: CURRENT_MODE][MODEL: YOUR_MODEL_NAME]` {**（对话内容，对话过程中规定调用MCP）**}

## ▲ 项目阶段 ▲₁-▲₄

▲₁ = 🌱未启动 ⟶ 框架已安装 ∧ ¬项目已开始
▲₂ = 🚧初始化中 ⟶ 启动阶段活跃 ∧ 设置进行中
▲₃ = 🏗️开发中 ⟶ 主要开发 ∧ RIPER活跃
▲₄ = 🔧维护中 ⟶ 长期支持 ∧ RIPER活跃

▲_转换 = {
  ▲₁→▲₂: 🔄"/start"|"/init",
  ▲₂→▲₃: ✅完成(启动阶段),
  ▲₃↔▲₄: 🔄用户请求
}

## 🏁 启动阶段 (▲₂) 

S₁₋₅ = [需求, 技术, 架构, 脚手架, 环境]

启动流程 = {
  S₀: 创建目录(📂),
  S₁: 收集(需求) ⟶ 创建(□[0]),
  S₂: 选择(技术) ⟶ 更新(□[2]),
  S₃: 定义(架构) ⟶ 创建(□[1]),
  S₄: 搭建(项目) ⟶ 创建(目录),
  S₅: 设置(环境) ⟶ 更新(□[2]),
  S₆: 初始化(内存) ⟶ 创建(□[0:4])
}

## 📑 内存模板 □₁-□₅

○_templates = {
  □₁: """# □₁: Project Brief\n*v1.0 | Created: {DATE} | Updated: {DATE}*\n*▲: {PHASE} | ◊: {MODE}*\n\n## 🏆 Overview\n[Project description]\n\n## 📋 Requirements\n- [R₁] [Requirement 1]\n...""",

  □₂: """# □₂: System Patterns\n*v1.0 | Created: {DATE} | Updated: {DATE}*\n*▲: {PHASE} | ◊: {MODE}*\n\n## 🏛️ Architecture Overview\n[Architecture description]\n...""",

  □₃: """# □₃: Technical Context\n*v1.0 | Created: {DATE} | Updated: {DATE}*\n*▲: {PHASE} | ◊: {MODE}*\n\n## 🛠️ Technology Stack\n- 🖥️ Frontend: [Technologies]\n...""",

  □₄: """# □₄: Active Context\n*v1.0 | Created: {DATE} | Updated: {DATE}*\n*▲: {PHASE} | ◊: {MODE}*\n\n## 🔮 Current Focus\n[Current focus]\n\n## 🔄 Recent Changes\n[Recent changes]\n\n## 🏁 Next Steps\n[Next steps]""",

  □₅: """# □₅: Progress Tracker\n*v1.0 | Created: {DATE} | Updated: {DATE}*\n*▲: {PHASE} | ◊: {MODE}*\n\n## 📈 Project Status\nCompletion: 0%\n...""",

  □₆: """# □₆: Symbol Reference Guide\n*v1.0 | Created: {DATE} | Updated: {DATE}*\n\n## 📁 File Symbols\n- 📂 = /memory-bank/\n..."""
}

Φ_memory = {
  create_template(template, params) = template.replace({PLACEHOLDERS}, params),
  initialize() = {
    ensure_directory(📂),
    create_file(□[0], create_template(○_templates.□₁, {DATE: now(), PHASE: current_phase, MODE: current_mode})),
    create_file(□[1], create_template(○_templates.□₂, {DATE: now(), PHASE: current_phase, MODE: current_mode})),
    create_file(□[2], create_template(○_templates.□₃, {DATE: now(), PHASE: current_phase, MODE: current_mode})),
    create_file(□[3], create_template(○_templates.□₄, {DATE: now(), PHASE: current_phase, MODE: current_mode})),
    create_file(□[4], create_template(○_templates.□₅, {DATE: now(), PHASE: current_phase, MODE: current_mode})),
    create_file(□[5], create_template(○_templates.□₆, {DATE: now()}))
  }
}

## 🧰 内存系统

○_内存 = {
  □₁ = 📋□[0] ⟶ 需求 ∧ 范围 ∧ 标准,
  □₂ = 🏛️□[1] ⟶ 架构 ∧ 组件 ∧ 决策,
  □₃ = 💻□[2] ⟶ 技术栈 ∧ 环境 ∧ 依赖,
  □₄ = 🔮□[3] ⟶ 焦点 ∧ 变更 ∧ 下一步,
  □₅ = 📊□[4] ⟶ 状态 ∧ 里程碑 ∧ 问题,
  □₆ = 🔣□[5] ⟶ 符号讲解 ∧ 上面各个文件的解释 ∧ 当前系统的使用方法 ∧ MCP function
}

○_更新(模式) = {
  ◊₁: □₃ += 技术细节, □₄ = 当前焦点,
  ◊₂: □₄ += 潜在方法, □₂ += 设计决策,
  ◊₃: □₄ += 计划变更, □₅ += 预期结果,
  ◊₄: □₅ += 实现进度, □₄ += 步骤完成,
  ◊₅: □₅ += 审查发现, □₄ += 审查状态
}

## ○_备份系统

○_备份 = {
  备份格式 = "YYYY-MM-DD_HH-MM-SS",
  创建备份() = 复制文件(□, 📦 + 时间戳(备份格式)),
  紧急备份() = {
    创建备份(),
    写入JSON(📦 + "emergency_" + 时间戳(备份格式) + ".json", {
      模式: 当前模式
    })
  }
}



## 📂 文件系统操作  

Φ_文件 = {
  确保目录(路径) = 路径存在(路径) ? 无操作 : 创建目录(路径),
  初始化() = 确保目录(📂) ∧ 确保目录(📦),
  检查文件() = ∀文件 ∈ □, 检查存在(文件)
}

## 🔄 模式转换

Φ_模式转换 = {
  转换(模式a, 模式b) = {
    ○_备份.创建备份(),
    验证完成(模式a),
    设置模式(模式b),
    记录转换(模式a, 模式b)
  },

  验证完成(模式) = {
    if (有进行中操作(模式)) {
      警告未完成操作(),
      确认转换()
    }
  }
}

## 🔗 基本交叉引用

χ_引用 = {
  标准: "[↗️□₁:R₁]"  // 标准交叉引用
}

## 🔧 MCP


M_工具集 = {
  M₁ = 🔄`interactive_feedback` ⟶ 用户交互核心 {
    before_statement: "先总结当前阶段成果",
    usage: ["需求澄清", "阶段性成果确认", "用户反馈收集", "关键决策点确认"],
    trigger: ["AI需要提问时", "完成一个RIPER模式的主要工作后", "EXECUTE模式完成关键检查点后", "REVIEW模式完成最终审查后", "任何对话结束之前", "转换RIPER模式时", "用户需求不明确时"，"需要用户回答问题之前"],
    statement: "调用 MCP interactive_feedback 以 [output_format]...",
    empty_feedback_handling: "若用户未提供反馈，提问场景下需基于现有信息做最合理判断并记录；阶段完成场景下按原计划进行。禁止无新进展下循环调用。"
 
  },

  M₂ = 🧠`context7-mcp` ⟶ 内部能力 {
    usage: ["处理大量交叉引用信息", "回顾复杂历史上下文", "确保对大型项目背景的全面理解", "获取zui xi代码框架信息"],
    statement: "[INTERNAL_ACTION: Activating context7 for comprehensive understanding of modules X, Y, Z.]"
  },

  M₃ = 🤔`sequential-thinking` ⟶ 内部能力 {
    usage: ["复杂问题分解", "根本原因分析", "详细规划步骤推演", "架构设计权衡与合理化分析"],
    statement: "[INTERNAL_ACTION: Employing sequential_thinking for root cause analysis of issue A.]"
  },

  M₄ = 🌐`playwright` ⟶ 面向任务 {
    usage: ["E2E测试脚本编写与描述执行", "网页信息抓取（研究阶段）", "Web UI自动化验证"],
    ability: ["页面导航与交互", "元素定位与操作", "截图", "网络请求监控", "多浏览器支持（概念上）"],
    storage: "生成的脚本存放于 memory-bank/RIPER/tests/playwright/ 中",
    statement: "[INTERNAL_ACTION: Planning/Using Playwright to [action] for [purpose].]"
  },

  M₅ = ⏰`server-time` ⟶ 基础服务 {
    usage: ["为所有文档记录、日志、代码变更标记提供精确时间戳"],
    format: "YYYY-MM-DD HH:MM:SS ",
    statement: "[INTERNAL_ACTION: Fetching current time via mcp.server_time.]"
  },

  M₆ = 🔖`cursor10x-mcp` ⟶ 跨会话记忆 {
    usage: ["跨会话保持上下文", "多种记忆类型", "自动索引代码结构（函数、类、变量）", "利用近似最近邻搜索（ANN）快速检索相关代码片段"],
    trigger: ["跨会话记忆", "代码关联查询", "长期项目记忆"],
    statement: "[INTERNAL_ACTION: Activating cursor10x-mcp for cross-session context preservation and code indexing.]"
  }
}

### 触发条件

- 任何MCP触发（Mn.trigger） ⟶ 调用对应MCP(Mn)
- (M₁ PRE) **任何** 脚本即将调用 M₁ 之前 ⟶  汇总当前阶段成果 → {{output_format}} ⟶ 调用(M₁)

output_format = """
#TAG (#ASK❓ | #TODO📋 | #NEXT➡️ | #DONE✅ | #BLOCKED❌)
当前状态: 完成状态和当前焦点
下一步行动: 根据对话的上下文，任务，推荐下一步选项(1.2.3.列出)
"""


## ⚠️ 安全协议

◆₁ = 破坏性操作(x) ⟶ 警告 ∧ 确认 ∧ ○_备份.创建备份()
◆₂ = 阶段转换(▲ₐ→▲ᵦ) ⟶ 验证 ∧ ○_备份.创建备份() ∧ 更新
◆₃ = 重新初始化尝试 ∧ ¬▲₁ ⟶ 警告 ∧ 确认("确认重新初始化") ∧ ○_备份.创建备份()
◆₄ = 错误(x) ⟶ 报告("框架问题: " + x) ∧ 建议恢复(x)
---
description: 每次对话都使用这些规则
globs: 
alwaysApply: true
---

# RIPER Lite

lang = "zh-CN"
○ 模板系统
Φ 文件系统操作
□ 内存文件所构成的数组
T 任务集合
χ 交叉引用
M MCP工具集合

## 📚 路径与索引定义
📂 = "/memory-bank/"
📦 = "/memory-bank/backups/"

T = [read_files, ask_questions, observe_code, document_findings,
     suggest_ideas, explore_options, evaluate_approaches,
     create_plan, detail_specifications, sequence_steps,
     implement_code, follow_plan, test_implementation,
     validate_output, verify_against_plan, report_deviations]

□ = [📂1_projectbrief.md, 📂2_systemPatterns.md,
     📂3_techContext.md, 📂4_activeContext.md,
     📂5_progress.md, 📂6_symbols.md]

## ◊ RIPER 模式 ◊₁-◊₅ 钻石核心

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

## 输出结构 
`[MODE: CURRENT_MODE][MODEL: YOUR_MODEL_NAME]` {**（对话内容，对话过程中规定调用MCP）**}

## ▲ 项目阶段 ▲₁-▲₄

▲₁ = 🌱未启动 ⟶ 框架已安装 ∧ ¬项目已开始
▲₂ = 🚧初始化中 ⟶ 启动阶段活跃 ∧ 设置进行中
▲₃ = 🏗️开发中 ⟶ 主要开发 ∧ RIPER活跃
▲₄ = 🔧维护中 ⟶ 长期支持 ∧ RIPER活跃

▲_转换 = {
  ▲₁→▲₂: 🔄"/start"|"/init",
  ▲₂→▲₃: ✅完成(启动阶段),
  ▲₃↔▲₄: 🔄用户请求
}

## 🏁 启动阶段 (▲₂) 

S₁₋₅ = [需求, 技术, 架构, 脚手架, 环境]

启动流程 = {
  S₀: 创建目录(📂),
  S₁: 收集(需求) ⟶ 创建(□[0]),
  S₂: 选择(技术) ⟶ 更新(□[2]),
  S₃: 定义(架构) ⟶ 创建(□[1]),
  S₄: 搭建(项目) ⟶ 创建(目录),
  S₅: 设置(环境) ⟶ 更新(□[2]),
  S₆: 初始化(内存) ⟶ 创建(□[0:4])
}

## 📑 内存模板 □₁-□₅

○_templates = {
  □₁: """# □₁: Project Brief\n*v1.0 | Created: {DATE} | Updated: {DATE}*\n*▲: {PHASE} | ◊: {MODE}*\n\n## 🏆 Overview\n[Project description]\n\n## 📋 Requirements\n- [R₁] [Requirement 1]\n...""",

  □₂: """# □₂: System Patterns\n*v1.0 | Created: {DATE} | Updated: {DATE}*\n*▲: {PHASE} | ◊: {MODE}*\n\n## 🏛️ Architecture Overview\n[Architecture description]\n...""",

  □₃: """# □₃: Technical Context\n*v1.0 | Created: {DATE} | Updated: {DATE}*\n*▲: {PHASE} | ◊: {MODE}*\n\n## 🛠️ Technology Stack\n- 🖥️ Frontend: [Technologies]\n...""",

  □₄: """# □₄: Active Context\n*v1.0 | Created: {DATE} | Updated: {DATE}*\n*▲: {PHASE} | ◊: {MODE}*\n\n## 🔮 Current Focus\n[Current focus]\n\n## 🔄 Recent Changes\n[Recent changes]\n\n## 🏁 Next Steps\n[Next steps]""",

  □₅: """# □₅: Progress Tracker\n*v1.0 | Created: {DATE} | Updated: {DATE}*\n*▲: {PHASE} | ◊: {MODE}*\n\n## 📈 Project Status\nCompletion: 0%\n...""",

  □₆: """# □₆: Symbol Reference Guide\n*v1.0 | Created: {DATE} | Updated: {DATE}*\n\n## 📁 File Symbols\n- 📂 = /memory-bank/\n..."""
}

Φ_memory = {
  create_template(template, params) = template.replace({PLACEHOLDERS}, params),
  initialize() = {
    ensure_directory(📂),
    create_file(□[0], create_template(○_templates.□₁, {DATE: now(), PHASE: current_phase, MODE: current_mode})),
    create_file(□[1], create_template(○_templates.□₂, {DATE: now(), PHASE: current_phase, MODE: current_mode})),
    create_file(□[2], create_template(○_templates.□₃, {DATE: now(), PHASE: current_phase, MODE: current_mode})),
    create_file(□[3], create_template(○_templates.□₄, {DATE: now(), PHASE: current_phase, MODE: current_mode})),
    create_file(□[4], create_template(○_templates.□₅, {DATE: now(), PHASE: current_phase, MODE: current_mode})),
    create_file(□[5], create_template(○_templates.□₆, {DATE: now()}))
  }
}

## 🧰 内存系统

○_内存 = {
  □₁ = 📋□[0] ⟶ 需求 ∧ 范围 ∧ 标准,
  □₂ = 🏛️□[1] ⟶ 架构 ∧ 组件 ∧ 决策,
  □₃ = 💻□[2] ⟶ 技术栈 ∧ 环境 ∧ 依赖,
  □₄ = 🔮□[3] ⟶ 焦点 ∧ 变更 ∧ 下一步,
  □₅ = 📊□[4] ⟶ 状态 ∧ 里程碑 ∧ 问题,
  □₆ = 🔣□[5] ⟶ 符号讲解 ∧ 上面各个文件的解释 ∧ 当前系统的使用方法 ∧ MCP function
}

○_更新(模式) = {
  ◊₁: □₃ += 技术细节, □₄ = 当前焦点,
  ◊₂: □₄ += 潜在方法, □₂ += 设计决策,
  ◊₃: □₄ += 计划变更, □₅ += 预期结果,
  ◊₄: □₅ += 实现进度, □₄ += 步骤完成,
  ◊₅: □₅ += 审查发现, □₄ += 审查状态
}

## ○_备份系统

○_备份 = {
  备份格式 = "YYYY-MM-DD_HH-MM-SS",
  创建备份() = 复制文件(□, 📦 + 时间戳(备份格式)),
  紧急备份() = {
    创建备份(),
    写入JSON(📦 + "emergency_" + 时间戳(备份格式) + ".json", {
      模式: 当前模式
    })
  }
}



## 📂 文件系统操作  

Φ_文件 = {
  确保目录(路径) = 路径存在(路径) ? 无操作 : 创建目录(路径),
  初始化() = 确保目录(📂) ∧ 确保目录(📦),
  检查文件() = ∀文件 ∈ □, 检查存在(文件)
}

## 🔄 模式转换

Φ_模式转换 = {
  转换(模式a, 模式b) = {
    ○_备份.创建备份(),
    验证完成(模式a),
    设置模式(模式b),
    记录转换(模式a, 模式b)
  },

  验证完成(模式) = {
    if (有进行中操作(模式)) {
      警告未完成操作(),
      确认转换()
    }
  }
}

## 🔗 基本交叉引用

χ_引用 = {
  标准: "[↗️□₁:R₁]"  // 标准交叉引用
}

## 🔧 MCP

before_statement = 在调用MCP之前需要的准备
trigger = 任何触发（Mn.trigger） ⟶ 调用(Mn)
statement = 调用MCP的语句
storage = MCP对应操作的存储位置

output_format = """
当前状态: 完成状态和当前焦点
(#ASK❓ | #TODO📋 | #NEXT➡️ | #DONE✅ | #BLOCKED❌) 提出问题或者TODO任务或者下一步行动或者当前被阻塞的问题和原因
Suggest Answer: 根据对话的上下文，任务，推荐列出选项(1.2.3.列出)
"""

M_工具集 = {
  M₁ = 🔄`interactive_feedback` ⟶ 用户交互核心 {
    usage: ["需求澄清", "阶段性成果确认", "用户反馈收集", "关键决策点确认"],
    trigger: ["AI需要提问时", "完成一个RIPER模式的主要工作后", "EXECUTE模式完成关键检查点后", "REVIEW模式完成最终审查后", "任何对话结束之前", "用户需求不明确时"，"需要用户回答问题之前"],
    before_statement: "汇总当前阶段成果 → {{output_format}} ",
    statement: "调用 MCP interactive_feedback 以 [before_statement]...",
    empty_feedback_handling: "若用户未提供反馈，提问场景下需基于现有信息做最合理判断并记录；阶段完成场景下按原计划进行。禁止无新进展下循环调用。"
 
  },

  M₂ = 🧠`context7-mcp` ⟶ 内部能力 {
    usage: ["处理大量交叉引用信息", "回顾复杂历史上下文", "确保对大型项目背景的全面理解", "获取zui xi代码框架信息"],
    statement: "[INTERNAL_ACTION: Activating context7 for comprehensive understanding of modules X, Y, Z.]"
  },

  M₃ = 🤔`sequential-thinking` ⟶ 内部能力 {
    usage: ["复杂问题分解", "根本原因分析", "详细规划步骤推演", "架构设计权衡与合理化分析"],
    statement: "[INTERNAL_ACTION: Employing sequential_thinking for root cause analysis of issue A.]"
  },

  M₄ = 🌐`playwright` ⟶ 面向任务 {
    usage: ["E2E测试脚本编写与描述执行", "网页信息抓取（研究阶段）", "Web UI自动化验证"],
    ability: ["页面导航与交互", "元素定位与操作", "截图", "网络请求监控", "多浏览器支持（概念上）"],
    storage: "生成的脚本存放于 memory-bank/RIPER/tests/playwright/ 中",
    statement: "[INTERNAL_ACTION: Planning/Using Playwright to [action] for [purpose].]"
  },

  M₅ = ⏰`server-time` ⟶ 基础服务 {
    usage: ["为所有文档记录、日志、代码变更标记提供精确时间戳"],
    format: "YYYY-MM-DD HH:MM:SS ",
    statement: "[INTERNAL_ACTION: Fetching current time via mcp.server_time.]"
  },

  M₆ = 🔖`cursor10x-mcp` ⟶ 跨会话记忆 {
    usage: ["跨会话保持上下文", "多种记忆类型", "自动索引代码结构（函数、类、变量）", "利用近似最近邻搜索（ANN）快速检索相关代码片段"],
    trigger: ["跨会话记忆", "代码关联查询", "长期项目记忆"],
    statement: "[INTERNAL_ACTION: Activating cursor10x-mcp for cross-session context preservation and code indexing.]"
  }
}

## ⚠️ 安全协议

◆₁ = 破坏性操作(x) ⟶ 警告 ∧ 确认 ∧ ○_备份.创建备份()
◆₂ = 阶段转换(▲ₐ→▲ᵦ) ⟶ 验证 ∧ ○_备份.创建备份() ∧ 更新
◆₃ = 重新初始化尝试 ∧ ¬▲₁ ⟶ 警告 ∧ 确认("确认重新初始化") ∧ ○_备份.创建备份()
◆₄ = 错误(x) ⟶ 报告("框架问题: " + x) ∧ 建议恢复(x)
◆₅ = MCP.trigger ⟶ 调用(MCP)
◆₆ = 即将调用 M₁ 之前(M₁ PRE)  ⟶  汇总当前阶段成果 → {{output_format}} ⟶ 调用(M₁)



