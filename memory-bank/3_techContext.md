# □₃: Technical Context
*v1.0 | Created: 2024-12-19 | Updated: 2024-12-19*
*▲: 🚧初始化中 | ◊: 🔍研究模式*

## 🛠️ Technology Stack
- 🖥️ Frontend: Markdown文档系统
- 🧠 AI Engine: Claude Sonnet 4 (Anthropic)
- 🔧 Framework: RIPER Lite v1.0.3
- 📝 Language: 中文 (zh-CN)
- 🗂️ File System: 结构化内存文件 (.md)

## 🌐 Environment Setup
- **开发环境**: VSCode + Cursor IDE
- **工作目录**: `/Users/bigdan/Workspace/ai/rules/RIPER-lite`
- **内存目录**: `./memory-bank/`
- **备份目录**: `./memory-bank/backups/`

## 📦 Dependencies & Tools

### MCP工具集 (M)
- **M₁ interactive_feedback** - 用户反馈收集与处理
- **M₂ context7-mcp** - 交叉引用与历史上下文解析
- **M₃ sequential-thinking** - 复杂问题分解与深度分析
- **M₄ playwright** - E2E测试脚本与网页抓取
- **M₅ server-time** - 时间戳服务
- **M₆ cursor10x-mcp** - 跨会话记忆与代码索引

### 核心功能模块
- **符号解析器** - 处理◊▲□◆等几何符号
- **模式引擎** - 管理RIPER工作流程
- **内存管理器** - 维护结构化文档
- **备份系统** - 自动备份与恢复

## ⚙️ Configuration
- **语言设置**: zh-CN (中文)
- **版本**: RIPER Lite v1.0.3
- **符号集**: 几何符号 + 表情符号 + 下标
- **工作模式**: 五模式循环 (🔍💡📝⚙️🔎)

## 🔄 Integration Points
- **文件系统**: 直接读写 .md 文件
- **用户界面**: 命令行交互 (/init, /r, /i, /p, /e, /rev)
- **备份机制**: 自动时间戳备份
- **错误处理**: 异常捕获与恢复建议

## 📊 Performance Considerations
- **内存效率**: 轻量级文档结构
- **响应速度**: 符号化简洁表示
- **可维护性**: 模块化组件设计
- **扩展性**: MCP工具集成架构
