# DSH 扁平代码风格插件

规则：尽可能在 main/主执行流程直接编写代码；不生成过于简单且少于 5 行的辅助函数，不为凑行数填充代码。必要的框架回调等允许保留。

解压后，在本文件所在目录打开终端执行（需已安装可用的 DSH 和 pnpm）：

    npx @deepseek-ai/dsh plugin --profile web add .

桌面版先彻底退出应用，将 web 改为 desktop。安装后重启并新建会话。

卸载：

    npx @deepseek-ai/dsh plugin --profile web remove dsh-flat-code-style

桌面版同样将 web 改为 desktop，并先退出应用。

验证：新会话要求生成“读取 CSV、删除缺失值并绘制折线图”的 Python 代码，检查是否直接在主流程完成，无不必要的短辅助函数。

这是提示词约束，不是强制代码检查器。已做 JavaScript 语法和模拟注册检查，未在用户实际 DSH 版本内进行安装测试。

此包采用官方 npm 风格 bundle 结构。ZIP 用于解压安装，未确认 .dsh 单文件导入规范，请勿仅改后缀后导入。

接口依据：
https://github.com/deepseek-ai/deepseek-harness/blob/master/packages/core/system-prompt/README.md
https://github.com/deepseek-ai/deepseek-harness/blob/master/apps/cli/reference/README.md
https://github.com/deepseek-ai/deepseek-harness/blob/master/packages/bundle/base/cordis.patch.yml
