pnpm 备忘清单
===

这个 [pnpm](https://pnpm.io/) 快速参考备忘单显示了它的常用命令与工作区使用清单。

入门与配置
----
<!--rehype:body-class=cols-2-->

### 安装与环境设置

命令 | 描述
:- | :-
`npm install -g pnpm` | 使用 npm 全局安装 pnpm
`corepack enable` | 通过 Corepack 启用 pnpm
`pnpm setup` | 初始化 pnpm 全局运行目录与 PATH
`pnpm -v` | 查看当前安装的 pnpm 版本
<!--rehype:class=auto-wrap-->

### 项目初始化与依赖管理

命令 | 描述
:- | :-
`pnpm init` | 初始化并创建 `package.json`
`pnpm install` 或 `pnpm i` | 安装项目所有依赖项
`pnpm add <pkg>` | 添加生产环境依赖项
`pnpm add -D <pkg>` | 添加开发环境依赖项 (`devDependencies`)
`pnpm add -g <pkg>` | 全局安装指定的软件包
`pnpm remove <pkg>` | 卸载指定的依赖包
`pnpm update` 或 `pnpm up` | 按照版本规则更新依赖包
<!--rehype:class=auto-wrap-->

日常开发与脚本
----
<!--rehype:body-class=cols-2-->

### 运行脚本

命令 | 描述
:- | :-
`pnpm dev` | 运行 `dev` 脚本
`pnpm build` | 运行 `build` 打包构建
`pnpm test` | 运行测试套件
`pnpm run <script>` | 运行自定义脚本
`pnpm exec <cmd>` | 在项目 node_modules 作用域内执行命令
`pnpm dlx <pkg>` | 类似于 `npx`，免安装临时运行 CLI 工具
<!--rehype:class=auto-wrap-->

### 依赖检查与审计

命令 | 描述
:- | :-
`pnpm list` 或 `pnpm ls` | 列出当前项目依赖树
`pnpm list --depth=0` | 仅列出一级直接依赖
`pnpm outdated` | 检查项目中已过期的依赖
`pnpm why <pkg>` | 追溯某个包被哪些上层依赖所引入
`pnpm audit` | 扫描项目依赖包的安全漏洞
`pnpm audit --fix` | 自动修复依赖漏洞
<!--rehype:class=auto-wrap-->

工作区 Monorepo
----

### 工作区命令

命令 | 描述
:- | :-
`pnpm -r <cmd>` | 递归在所有工作区子包中执行命令
`pnpm --filter <pkg> <cmd>` | 仅在指定子包中执行命令
`pnpm --filter <pkg>... <cmd>` | 在指定包及其所有上游依赖包中执行命令
`pnpm add <pkg> --filter <pkg_target>` | 将依赖单独添加到指定子项目中
`pnpm add <pkg> -w` | 将依赖添加到 Monorepo 根工作区
<!--rehype:class=auto-wrap-->

全局存储与缓存管理
----

### Store 维护

命令 | 描述
:- | :-
`pnpm store path` | 查看当前全局包存储目录路径
`pnpm store status` | 检查全局硬链接存储的完整性
`pnpm store prune` | 清理全局未被任何项目引用的孤立包缓存
<!--rehype:class=auto-wrap-->

另见
----

- [pnpm 官方文档](https://pnpm.io/)
- [npm 备忘清单](./npm.md)
