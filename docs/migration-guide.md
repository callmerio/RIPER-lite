![CursorRIPER♦○-lite](../res/github-header-sigma-lite.png)
# 迁移指南：从 CursorRIPER♦○ 到 CursorRIPER♦○ Lite

本指南帮助您从完整版的CursorRIPER♦○迁移到精简的lite版本。

## 移除的功能

lite版本移除了三个主要系统：

1. **上下文引用系统**
   - 所有@Files引用和上下文跟踪
   - 上下文命令（如!af、!ac等）
   - 上下文状态指示器
   - 模式-上下文映射

2. **CRUD权限系统**
   - 每个模式的权限矩阵
   - 操作类别和限制
   - 权限强制执行
   - 违规检测和处理
   - 权限命令（如!ckp、!pm等）

3. **代码保护系统**
   - 保护级别（PROTECTED、GUARDED等）
   - 保护注释语法
   - 保护扫描和管理
   - 保护命令（如!cp、!cg等）
   - protection.md内存文件

## 内存文件变更

- `protection.md`文件被完全移除
- `activeContext.md`被简化，移除了上下文引用
- 其他内存文件基本保持不变

## 迁移步骤

1. **设置目录结构**
   ```
   /memory-bank/
   /memory-bank/backups/
   ```

2. **替换规则文件**
   - 将`RIPERsigma-lite.mdc`复制到您的`.cursor/rules/`目录
   - 移除或禁用原始的`RIPERsigma1.0.3.mdc`文件
   - 移除任何上下文或保护相关的MDC文件

3. **更新内存文件**
   - 如果您使用的是完整版：
     - 保留`projectbrief.md`、`systemPatterns.md`、`techContext.md`的内容
     - 通过移除上下文引用部分来简化`activeContext.md`
     - 保留`progress.md`的内容
     - 您可以丢弃`protection.md`
   
   - 如果重新开始：
     - 为所有内存文件使用提供的模板文件

4. **更新工作实践**
   - 停止使用上下文引用命令（!af、!ac等）
   - 停止使用权限检查命令（!ckp、!pm等）
   - 停止使用保护命令（!cp、!cg等）
   - 继续使用模式转换命令（/r、/i、/p、/e、/rev）

## 模式转换

模式转换命令保持不变：

```
/research (或 /r) - 研究模式
/innovate (或 /i) - 创新模式
/plan (或 /p) - 计划模式
/execute (或 /e) - 执行模式
/review (或 /rev) - 审查模式
```

## Lite版本的优势

- **操作更简单**：需要记住的命令和概念更少
- **更低的Token使用量**：减少的框架开销意味着更多token用于您的实际工作
- **更容易上手**：新用户可以更快地学习系统
- **专注的RIPER工作流**：保持核心的研究-创新-计划-执行-审查工作流

## 何时使用完整版

在以下情况下，您可能想要坚持使用完整版：

- 您在复杂项目中严重依赖上下文引用
- 您需要严格的基于模式的权限强制执行
- 代码保护对您的工作流至关重要
- 您正在与已经采用完整框架的团队合作
