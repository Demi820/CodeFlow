# CodeFlow 代码库结构分析

e:/vscode/CodeFlow/
├── .clinerules             # Cline 工具的自定义规则配置文件
├── .dockerignore           # Docker 构建时忽略的文件和目录
├── .eslintrc.json          # ESLint 配置文件，用于代码风格检查
├── .git-blame-ignore-revs  # Git blame 时忽略的提交记录
├── .gitattributes          # 定义 Git 处理文件的方式 (例如行尾符)
├── .gitconfig              # 项目特定的 Git 配置
├── .gitignore              # Git 忽略的文件和目录
├── .npmrc                  # NPM 配置文件
├── .nvmrc                  # 指定项目使用的 Node.js 版本 (用于 NVM)
├── .prettierignore         # Prettier 格式化时忽略的文件
├── .prettierrc.json        # Prettier 格式化配置文件
├── .roomodes               # Roo 模式配置文件
├── .vscodeignore           # VS Code 扩展打包时忽略的文件
├── CHANGELOG.md            # 项目变更日志
├── CODE_OF_CONDUCT.md      # 社区行为准则
├── CONTRIBUTING.md         # 项目贡献指南
├── ellipsis.yaml           # Ellipsis.ai 配置文件 (可能用于 AI 功能)
├── esbuild.js              # esbuild 打包配置文件 (用于构建)
├── flake.lock              # Nix Flake 锁定文件 (用于可复现的开发环境)
├── flake.nix               # Nix Flake 定义文件 (用于声明开发环境)
├── jest.config.js          # Jest 测试框架配置文件
├── knip.json               # Knip 工具配置文件 (用于查找未使用的文件和依赖)
├── LICENSE                 # 项目许可证文件
├── package-lock.json       # NPM 依赖版本锁定文件
├── package.json            # NPM 项目配置文件 (依赖、脚本等)
├── PRIVACY.md              # 隐私政策文档
├── README.md               # 项目主说明文档
├── tsconfig.json           # TypeScript 编译器配置文件
├── .changeset/             # 版本管理和变更日志工具 (Changesets) 配置与数据
│   ├── changelog-config.js # Changesets 更新日志生成配置
│   ├── config.json         # Changesets 主要配置文件
│   └── README.md           # Changesets 工具说明
├── .git/                   # Git 版本控制系统目录 (通常隐藏)
├── .github/                # GitHub 相关配置 (Actions, Issue 模板等)
│   ├── CODEOWNERS          # 定义代码所有者，用于 PR 审核
│   ├── dependabot.yml      # Dependabot 配置 (自动更新依赖)
│   ├── pull_request_template.md # Pull Request 模板
│   ├── actions/            # 自定义 GitHub Actions
│   │   └── ai-release-notes/ # AI 生成发布说明相关的 Action
│   ├── ISSUE_TEMPLATE/     # Issue 模板配置
│   │   ├── bug_report.yml  # Bug 报告模板
│   │   └── config.yml      # Issue 模板选择器配置
│   ├── scripts/            # GitHub Actions 使用的脚本
│   │   ├── ai-release-notes.py # AI 生成发布说明的 Python 脚本
│   │   ├── get_prev_version_refs.py # 获取上个版本引用的脚本
│   │   ├── overwrite_changeset_changelog.py # 覆盖 Changeset 更新日志的脚本
│   │   ├── parse_changeset_changelog.py # 解析 Changeset 更新日志的脚本
│   │   └── release-notes-prompt.py # 发布说明 Prompt 生成脚本
│   └── workflows/          # GitHub Actions 工作流定义
│       ├── changeset-release.yml # Changeset 发布流程
│       ├── code-qa.yml       # 代码质量检查流程 (lint, test 等)
│       ├── codeql.yml        # CodeQL 安全扫描流程
│       ├── discord-pr-notify.yml # PR 通知到 Discord 的流程
│       ├── marketplace-publish.yml # 发布到 VS Code Marketplace 的流程
│       └── update-contributors.yml # 更新贡献者列表的流程
├── .husky/                 # Husky 配置目录 (Git Hooks 工具)
│   ├── pre-commit          # pre-commit Git Hook 脚本 (通常用于 lint 或 test)
│   └── pre-push            # pre-push Git Hook 脚本
├── .vscode/                # VS Code 编辑器特定配置
│   ├── extensions.json     # 推荐的 VS Code 扩展
│   ├── launch.json         # VS Code 调试配置
│   ├── settings.json       # VS Code 工作区设置
│   └── tasks.json          # VS Code 任务配置
├── ai_analysis/            # 存放 AI 分析结果的目录
│   ├── ai_model_integration.md # AI 模型集成分析文档
│   ├── ai_tools_integration_analysis.md # AI 工具集成分析文档
│   ├── codeflow_architecture_analysis.md # CodeFlow 架构分析文档
│   ├── mcp_module_analysis.md # MCP 模块分析文档
│   ├── project_analysis_generated.md # AI 生成的项目分析文档
│   ├── project_analysis_plan.md # 项目分析计划文档
│   ├── project_analysis.md # 项目分析文档
│   ├── project_structure_analysis_plan.md # 项目结构分析计划文档
│   └── tools_system_analysis.md # 工具系统分析文档
├── ai_prd/                 # AI 产品需求文档 (Product Requirement Document) 目录
├── assets/                 # 静态资源文件 (图片、图标等)
│   ├── docs/               # 文档相关资源
│   │   └── demo.gif        # 演示 GIF
│   ├── icons/              # 图标资源
│   │   └── rocket.png      # 火箭图标
│   └── images/             # 图片资源
│       ├── openrouter.png  # OpenRouter 图片
│       └── requesty.png    # Requesty 图片
├── audio/                  # 音频文件
│   ├── celebration.wav     # 庆祝音效
│   ├── notification.wav    # 通知音效
│   └── progress_loop.wav   # 进度循环音效
├── benchmark/              # 基准测试相关代码和配置
│   ├── .env.local.sample   # 本地环境变量示例
│   ├── Dockerfile          # Docker 配置文件 (用于构建测试环境)
│   ├── entrypoint.sh       # Docker 容器入口脚本
│   ├── package.json        # 基准测试项目的 NPM 配置
│   ├── README.md           # 基准测试说明文档
│   ├── tsconfig.json       # TypeScript 配置文件
│   ├── prompts/            # 基准测试使用的 Prompt 文件
│   │   ├── cpp.md          # C++ Prompt
│   │   ├── go.md           # Go Prompt
│   │   ├── java.md         # Java Prompt
│   │   ├── javascript.md   # JavaScript Prompt
│   │   ├── python.md       # Python Prompt
│   │   └── rust.md         # Rust Prompt
│   └── src/                # 基准测试源代码
│       ├── cli.ts          # 命令行接口实现
│       ├── runExercise.ts  # 执行测试练习的逻辑
│       └── utils.ts        # 工具函数
├── cline_docs/             # Cline 工具相关文档
│   └── settings.md         # 设置相关文档
├── e2e/                    # 端到端 (End-to-End) 测试相关代码和配置
│   ├── .env.local.sample   # 本地环境变量示例
│   ├── .vscode-test.mjs    # VS Code 测试运行器配置
│   ├── package.json        # E2E 测试项目的 NPM 配置
│   ├── tsconfig.json       # TypeScript 配置文件
│   ├── VSCODE_INTEGRATION_TESTS.md # VS Code 集成测试说明
│   └── src/                # E2E 测试源代码
├── locales/                # 扩展本体的本地化/国际化 (i18n) 资源根目录 (除英文外)
│   ├── ca/                 # 加泰罗尼亚语
│   ├── de/                 # 德语
│   ├── es/                 # 西班牙语
│   ├── fr/                 # 法语
│   ├── hi/                 # 印地语
│   ├── it/                 # 意大利语
│   ├── ja/                 # 日语
│   ├── ko/                 # 韩语
│   ├── pl/                 # 波兰语
│   ├── pt-BR/              # 巴西葡萄牙语
│   ├── tr/                 # 土耳其语
│   ├── vi/                 # 越南语
│   ├── zh-CN/              # 简体中文
│   └── zh-TW/              # 繁体中文
├── scripts/                # 项目辅助脚本
│   ├── find-missing-i18n-key.js # 查找缺失 i18n key 的脚本
│   ├── find-missing-translations.js # 查找缺失翻译的脚本
│   └── update-contributors.js # 更新贡献者列表的脚本
├── src/                    # VS Code 扩展核心后端源代码 (TypeScript)
│   ├── extension.ts        # 扩展主入口文件，负责初始化和激活扩展
│   ├── __mocks__/          # Jest 测试的 Mock 实现
│   ├── __tests__/          # 后端单元测试和集成测试
│   ├── activate/           # 扩展激活相关的逻辑
│   │   ├── handleTask.ts   # 处理任务逻辑
│   │   ├── handleUri.ts    # 处理 URI 激活逻辑
│   │   ├── humanRelay.ts   # Human Relay (人工中继) 功能相关
│   │   ├── index.ts        # 激活模块入口
│   │   ├── registerCodeActions.ts # 注册 Code Actions
│   │   ├── registerCommands.ts # 注册 VS Code 命令
│   │   └── registerTerminalActions.ts # 注册终端相关操作
│   ├── api/                # 与外部 AI 模型 API 交互的逻辑
│   │   ├── index.ts        # API 模块入口
│   │   ├── providers/      # 各种 AI 服务提供商的实现 (Anthropic, OpenAI, Gemini 等)
│   │   │   └── base-provider.ts # AI 提供商基类
│   │   └── transform/      # 处理不同 AI API 请求和响应格式的转换逻辑
│   ├── core/               # 扩展核心功能模块
│   │   ├── Cline.ts        # Cline 核心类，管理任务、消息、模式等
│   │   ├── CodeActionProvider.ts # 提供 Code Actions 的实现
│   │   ├── contextProxy.ts # 上下文代理，用于管理传递给 AI 的上下文信息
│   │   ├── EditorUtils.ts  # 编辑器相关的工具函数
│   │   ├── mode-validator.ts # 模式验证逻辑
│   │   ├── assistant-message/ # 处理 AI 助手消息的逻辑
│   │   ├── config/         # 配置管理 (设置、自定义模式等)
│   │   ├── diff/           # Diff 相关逻辑 (生成和应用 Diff)
│   │   ├── ignore/         # 处理 .rooignore 文件的逻辑
│   │   ├── mentions/       # 处理 @ 提及 (文件、符号等) 的逻辑
│   │   ├── prompts/        # 管理和构建发送给 AI 的 Prompt
│   │   ├── sliding-window/ # 滑动窗口管理，控制上下文长度
│   │   └── webview/        # 与前端 Webview 通信和管理的逻辑
│   ├── exports/            # 导出给其他扩展使用的 API
│   │   ├── api.ts          # 导出的 API 定义
│   │   ├── message-history.ts # 导出的消息历史相关功能
│   │   └── roo-code.d.ts   # 导出的 TypeScript 类型定义
│   ├── i18n/               # 后端国际化 (i18n) 配置和资源
│   │   ├── index.ts        # i18n 模块入口
│   │   ├── setup.ts        # i18n 初始化设置
│   │   └── locales/        # 语言资源文件 (包含英文 en)
│   ├── integrations/       # 与 VS Code 各部分的集成逻辑
│   │   ├── diagnostics/    # 问题诊断 (Diagnostics) 集成
│   │   ├── editor/         # 编辑器集成 (装饰器、Diff 视图等)
│   │   ├── misc/           # 其他集成 (导出 Markdown, 读取行等)
│   │   ├── terminal/       # 终端集成
│   │   ├── theme/          # 主题集成
│   │   └── workspace/      # 工作区集成
│   ├── services/           # 提供独立功能的后台服务
│   │   ├── browser/        # 浏览器控制服务 (可能用于 Web 相关的任务)
│   │   ├── checkpoints/    # 检查点/快照服务
│   │   ├── glob/           # 文件 Glob 模式匹配服务
│   │   ├── mcp/            # Model Context Protocol (MCP) 服务
│   │   ├── ripgrep/        # Ripgrep 搜索服务封装
│   │   ├── search/         # 代码搜索服务
│   │   ├── telemetry/      # 遥测数据收集服务
│   │   └── tree-sitter/    # Tree-sitter 代码解析服务封装
│   ├── shared/             # 前后端共享的类型、常量和工具函数
│   │   ├── ExtensionMessage.ts # 后端发送给前端的消息类型
│   │   ├── HistoryItem.ts  # 历史记录项类型
│   │   ├── mcp.ts          # MCP 相关共享定义
│   │   ├── modes.ts        # 模式相关共享定义
│   │   └── WebviewMessage.ts # 前端发送给后端的消息类型
│   └── utils/              # 后端工具函数
│       ├── cost.ts         # API 调用成本计算
│       ├── fs.ts           # 文件系统操作工具
│       ├── git.ts          # Git 相关操作工具
│       ├── path.ts         # 路径处理工具
│       ├── shell.ts        # Shell 命令执行工具
│       └── logging/        # 日志记录工具
└── webview-ui/             # 前端 Webview 界面代码 (React, TypeScript, Tailwind CSS)
    ├── .eslintrc.json      # 前端 ESLint 配置
    ├── .gitignore          # 前端 Git 忽略文件
    ├── .npmrc              # 前端 NPM 配置
    ├── components.json     # Shadcn UI 组件配置文件
    ├── index.html          # Webview HTML 入口文件
    ├── jest.config.cjs     # 前端 Jest 配置
    ├── package.json        # 前端 NPM 项目配置
    ├── tsconfig.json       # 前端 TypeScript 配置
    ├── vite.config.ts      # Vite 构建工具配置
    ├── .storybook/         # Storybook 配置目录 (UI 组件开发和展示)
    │   ├── main.ts         # Storybook 主配置
    │   ├── preview.ts      # Storybook 预览配置
    │   └── vscode.css      # Storybook 中模拟 VS Code 样式的 CSS
    ├── public/             # Vite 静态资源目录
    └── src/                # Webview 前端源代码
        ├── App.tsx         # React 应用根组件
        ├── index.css       # 全局 CSS 样式 (包含 Tailwind 指令和 VS Code 变量)
        ├── index.tsx       # React 应用入口文件 (渲染根组件)
        ├── preflight.css   # Tailwind CSS Preflight (基础样式重置)
        ├── setupTests.ts   # Jest 测试环境设置
        ├── types.d.ts      # 全局 TypeScript 类型定义
        ├── vite-env.d.ts   # Vite 环境变量类型定义
        ├── __mocks__/      # 前端 Jest Mock 实现
        ├── __tests__/      # 前端单元测试和组件测试
        ├── components/     # UI 组件目录
        │   ├── chat/       # 聊天界面相关组件
        │   ├── common/     # 通用 UI 组件 (代码块, Markdown, Tab 等)
        │   ├── history/    # 历史记录界面相关组件
        │   ├── human-relay/# Human Relay 相关组件
        │   ├── mcp/        # MCP 界面相关组件
        │   ├── prompts/    # Prompt 管理界面组件
        │   ├── settings/   # 设置界面相关组件
        │   ├── ui/         # 基础 UI 组件 (基于 Shadcn UI, 如 Button, Input 等)
        │   └── welcome/    # 欢迎界面组件
        ├── context/        # React Context API (状态管理)
        │   └── ExtensionStateContext.tsx # 扩展状态 Context
        ├── i18n/           # 前端国际化 (i18n) 配置和资源
        │   ├── setup.ts    # i18n 初始化
        │   ├── TranslationContext.tsx # 翻译 Context
        │   └── locales/    # 语言资源文件
        ├── lib/            # 前端库函数/工具函数 (Shadcn UI 生成)
        │   └── utils.ts    # Shadcn UI 工具函数
        ├── oauth/          # OAuth 认证相关
        │   └── urls.ts     # OAuth URL 定义
        ├── stories/        # Storybook stories 文件 (组件示例和文档)
        └── utils/          # 前端通用工具函数
            ├── clipboard.ts # 剪贴板操作
            ├── format.ts    # 格式化函数
            ├── highlight.ts # 代码高亮
            ├── TelemetryClient.ts # 遥测客户端
            └── vscode.ts    # 与 VS Code 后端通信的封装
