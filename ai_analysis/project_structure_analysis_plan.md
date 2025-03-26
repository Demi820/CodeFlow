# CodeFlow 代码库结构分析计划

**目标:** 生成一份详细的代码库目录结构树 Markdown 文件，包含每个目录的功能描述。

**步骤:**

1.  **分析根目录结构:** 识别顶层配置文件、文档和关键子目录的作用。
2.  **深入分析 `src` 目录:** 理解 VS Code 扩展后端的核心逻辑。
    *   识别 `extension.ts` 作为入口点。
    *   分析 `activate`, `api`, `core`, `integrations`, `services`, `shared`, `utils` 等子目录的功能职责。
    *   识别测试 (`__tests__`, `__mocks__`) 和国际化 (`i18n`) 相关目录。
3.  **深入分析 `webview-ui` 目录:** 理解扩展前端界面的结构。
    *   识别 `src/App.tsx` 和 `src/index.tsx` 作为 React 应用入口。
    *   分析 `components` 目录下的各种 UI 组件模块 (chat, settings, history 等)。
    *   识别状态管理 (`context`)、国际化 (`i18n`)、路由、工具函数 (`utils`) 等。
    *   识别 Storybook (`stories`, `.storybook`) 和测试相关文件。
4.  **分析其他主要目录:** 理解辅助工具、测试、文档和资源等目录的功能。
    *   `.changeset`, `.github`, `.husky`, `.vscode`: 开发流程和工具配置。
    *   `assets`, `audio`: 静态资源。
    *   `benchmark`, `e2e`: 不同类型的测试。
    *   `locales`, `scripts`: 国际化资源和辅助脚本。
5.  **生成 Markdown 文件:**
    *   将分析结果整理成树状结构。
    *   为每个主要目录和子目录添加简洁明了的功能描述。
    *   将最终内容写入一个新的 Markdown 文件 `ai_analysis/project_structure_analysis.md`。

**预期输出 (Markdown 结构示例):**

```plaintext
e:/vscode/CodeFlow/
├── .changeset/             # 版本管理和变更日志工具 (Changesets) 配置与数据
├── .github/                # GitHub 相关配置 (Actions, Issue 模板等)
│   ├── actions/            # 自定义 GitHub Actions
│   └── workflows/          # GitHub Actions 工作流定义
├── src/                    # VS Code 扩展核心后端源代码 (TypeScript)
│   ├── extension.ts        # 扩展主入口文件
│   ├── api/                # 与外部 AI 模型 API 交互
│   │   └── providers/      # 各 AI 服务提供商实现
│   ├── core/               # 扩展核心功能模块 (Cline, 配置, Diff, Webview 通信等)
│   ├── integrations/       # 与 VS Code 编辑器、终端等集成
│   ├── services/           # 独立功能服务 (搜索, MCP, Tree-sitter 等)
│   └── webview-ui/         # 前端 Webview 界面代码 (React, TypeScript)
│       ├── src/            # Webview 前端源代码
│       │   ├── components/ # UI 组件
│       │   │   ├── chat/   # 聊天界面组件
│       │   │   └── settings/# 设置界面组件
│       │   └── utils/      # 前端工具函数
... (其他目录和文件)