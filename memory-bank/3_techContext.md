# □₃: Technical Context
*v1.0 | Created: 2024-12-19 | Updated: 2024-12-19*
*▲: 🚧初始化中 | ◊: 🔍研究*

## 🎯 技术选型咨询指南

### 📋 技术选型决策框架

#### 第一步：项目类型识别
- **🌐 Web应用**: 响应式网站、SPA、PWA
- **📱 移动应用**: 原生、混合、跨平台
- **🖥️ 桌面应用**: 跨平台桌面软件
- **🔌 API服务**: RESTful API、GraphQL、微服务
- **📊 数据处理**: 大数据、机器学习、实时分析
- **🎮 实时应用**: 游戏、聊天、协作工具
- **🤖 AI集成**: 智能应用、自动化工具

#### 第二步：技术需求评估
- **性能要求**: 并发用户数、响应时间、吞吐量
- **扩展性**: 水平扩展、垂直扩展需求
- **安全性**: 数据敏感度、合规要求
- **实时性**: 是否需要实时数据同步
- **离线支持**: 是否需要离线功能
- **国际化**: 多语言、多地区支持

#### 第三步：团队与资源评估
- **技术熟悉度**: 团队现有技能
- **学习曲线**: 新技术学习成本
- **开发时间**: 项目时间限制
- **预算约束**: 开发和运维成本
- **团队规模**: 开发人员数量
- **维护能力**: 长期维护资源

### 🛠️ 2024年主流技术栈推荐

#### 🖥️ 前端技术栈对比
| 框架 | 适用场景 | 学习曲线 | 生态系统 | 性能 |
|------|----------|----------|----------|------|
| **React** | 大型应用、企业级 | 中等 | 最丰富 | 优秀 |
| **Vue.js** | 中小型应用、快速开发 | 较低 | 丰富 | 优秀 |
| **Angular** | 企业级、复杂应用 | 较高 | 完整 | 优秀 |
| **Svelte** | 高性能、小型应用 | 较低 | 发展中 | 卓越 |
| **Next.js** | 全栈React、SEO重要 | 中等 | 丰富 | 优秀 |

#### ⚙️ 后端技术栈对比
| 技术栈 | 适用场景 | 性能 | 开发效率 | 生态 |
|--------|----------|------|----------|------|
| **Node.js** | 全栈JS、实时应用 | 良好 | 高 | 丰富 |
| **Python** | 数据科学、AI、快速原型 | 中等 | 高 | 最丰富 |
| **Java** | 企业级、高并发 | 优秀 | 中等 | 成熟 |
| **Go** | 微服务、高性能API | 卓越 | 高 | 发展中 |
| **TypeScript** | 类型安全、大型项目 | 良好 | 高 | 丰富 |

#### 🗄️ 数据库选择指南
| 类型 | 适用场景 | 示例 | 优势 |
|------|----------|------|------|
| **关系型** | 事务性应用、复杂查询 | PostgreSQL, MySQL | ACID、成熟 |
| **文档型** | 灵活数据、快速开发 | MongoDB, CouchDB | 灵活性 |
| **键值型** | 缓存、会话存储 | Redis, DynamoDB | 高性能 |
| **图数据库** | 关系复杂、社交网络 | Neo4j, ArangoDB | 关系查询 |

### 📝 技术选型问卷

为了给您提供最适合的技术建议，请回答以下问题：

#### 🎯 项目基本信息
1. **项目类型**: Web应用 / 移动应用 / 桌面应用 / API服务 / 其他
2. **项目规模**: 小型(1-3人) / 中型(4-10人) / 大型(10+人)
3. **预期用户数**: <1K / 1K-10K / 10K-100K / 100K+
4. **核心功能**: [请简述主要功能]

#### ⚡ 技术要求
5. **性能要求**: 低 / 中等 / 高 / 极高
6. **实时性需求**: 不需要 / 部分需要 / 强实时
7. **离线支持**: 不需要 / 基本支持 / 完全离线
8. **安全级别**: 一般 / 重要 / 极其重要

#### 👥 团队情况
9. **主要技术背景**: 前端 / 后端 / 全栈 / 其他
10. **熟悉的语言**: JavaScript / Python / Java / Go / 其他
11. **开发时间**: <1个月 / 1-3个月 / 3-6个月 / 6个月+
12. **学习新技术意愿**: 低 / 中等 / 高

## 🛠️ Technology Stack
- 🖥️ **Frontend**: [待选择技术栈]
- ⚙️ **Backend**: [待选择技术栈]
- 🗄️ **Database**: [待选择数据库]
- ☁️ **Cloud/Infrastructure**: [待选择云服务]
- 🔧 **DevOps**: [待选择工具链]

## 📦 Dependencies
### Core Dependencies
- [Dependency 1]: [Version] - [Purpose]
- [Dependency 2]: [Version] - [Purpose]

### Development Dependencies
- [Dev Dependency 1]: [Version] - [Purpose]
- [Dev Dependency 2]: [Version] - [Purpose]

## 🌍 Environment Configuration
### Development
- **Node Version**: [待定义]
- **Package Manager**: [待定义]
- **Database**: [待定义]
- **Environment Variables**: [待定义]

### Staging
- **Deployment Target**: [待定义]
- **Configuration**: [待定义]

### Production
- **Deployment Target**: [待定义]
- **Configuration**: [待定义]
- **Monitoring**: [待定义]

## 🔧 Development Tools
- **IDE/Editor**: [待定义]
- **Version Control**: Git
- **Package Manager**: [待定义]
- **Build Tools**: [待定义]
- **Testing Framework**: [待定义]
- **Linting/Formatting**: [待定义]

## 📋 Standards & Conventions
### Code Style
- **Naming Conventions**: [待定义]
- **File Organization**: [待定义]
- **Comment Standards**: [待定义]

### Git Workflow
- **Branch Strategy**: [待定义]
- **Commit Message Format**: [待定义]
- **PR/MR Process**: [待定义]

## 🧪 Testing Strategy
- **Unit Testing**: [待定义]
- **Integration Testing**: [待定义]
- **E2E Testing**: [待定义]
- **Performance Testing**: [待定义]

---
*Last updated by: RIPER Lite Framework*
*Technology decisions: 0*
