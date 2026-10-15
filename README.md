# Codex 完整使用教程（适合零基础）

> 原文来源：X 平台 @laowangbabababa（产品经理老王霸）  
> 发布时间：2026年7月  
> 本仓库整理自该长文教程，方便本地部署的 Codex 阅读与学习。

## 前言

Codex 这种东西，直觉告诉你应该是程序员用的。但最先玩转它的那批人，是产品经理、运营、自媒体博主、大学生、个体户老板——没几个会写代码的。

因为程序员用它，是从 80 分到 95 分。你不会写代码，是从 0 分直接到 60 分。那个跨越感，完全不一样。

黄仁勋讲得更直白：一个年薪五十万刀的工程师，一年用不了二十五万 token，那才不正常。token 不是成本，是生产资料。以前工厂烧煤，今天知识工作烧算力。你不用，别人用。

别再只把 AI 当聊天机器人了。ChatGPT 陪你唠嗑，Codex 替你干活。两个东西。

作者用 Codex，一个月收入 10W+，并把使用方法全部开源。从注册、安装到每种使用方式的页面拆解，全部配截图思路。不需要编程基础，跟着走一遍，让 AI 开始替你干活。

## 一、Codex 是什么

Codex 是 OpenAI 推出的 AI 编程 Agent。它跟普通 ChatGPT 对话不一样，Codex 能直接在你的电脑上创建文件、修改代码、运行命令、安装依赖、部署网站。

你说需求，它干完活，你审核结果。

用 Codex 能做这些事：

- 开发网站：帮我用 Next.js 做一个个人博客
- 修 bug：这个登录接口为什么会 500，帮我查一下
- 写脚本：写一个 Python 脚本，每天自动抓取微博热搜
- 部署上线：把这个项目部署到 Vercel
- 重构代码：把这段代码从 JavaScript 改成 TypeScript
- 写文档：给这个项目写 README 和 API 文档
- 数据处理：把这个 CSV 里的数据清洗一遍，输出统计图表
- 开发小程序：帮我初始化一个微信小程序项目

**Codex 不等于 ChatGPT**。ChatGPT 只能给你文字建议，Codex 能直接动手改你的项目文件、跑终端命令。

## 二、注册与订阅

Codex 不单独收费，包含在 ChatGPT 套餐里。你需要有一个 ChatGPT 付费账号。

### 1. 注册 Google 账号

打开 https://accounts.google.com/signup ，按提示填写信息。

注册时需要手机号验证，国内手机号 +86 开头可以正常收到验证码。注册完成后你就有了一个 Gmail 邮箱。

如果已经有 Google 账号，跳过这一步。

### 2. 注册 OpenAI 账号

打开 https://chatgpt.com/ ，用刚才注册的 Gmail 邮箱注册 OpenAI 账号。国内手机号也可以用来验证。

注意，OpenAI 对部分 IP 有限制。如果注册时提示不可用，换个网络环境再试。

### 3. 套餐选择

| 套餐 | 月费 | Codex 权限 | 适合谁 |
|------|------|------------|--------|
| Plus | $20/月 | 可用，有使用额度 | 个人学习、轻度开发，推荐先开这个 |
| Pro | $100-200/月 | 可用，额度很高 | 重度日常使用、专业开发者 |
| Team | $25/人/月 | 可用 | 小团队协作 |
| Business | 联系销售 | 可用 | 企业 |
| Enterprise | 联系销售 | 可用 | 大企业 |

### 4. 订阅方法（推荐安卓 Google Play）

ChatGPT Plus 最稳的订阅方式是通过安卓手机上的 Google Play 支付。

1. 准备一台安卓手机（没有的话可用模拟器，如 MuMu 或雷电）
2. 在手机上登录 Google 账号
3. 给 Google Play 添加支付方式（国内 Visa/MasterCard 或礼品卡）
4. 安装 ChatGPT App（官方绿色底白色线条图标）
5. 登录并订阅 Plus，价格约 $19.99/月

## 三、Codex 的四种使用方式

| 方式 | 是什么 | 适合谁 |
|------|--------|--------|
| Web 网页端 | 浏览器打开 chatgpt.com/codex | 新手入门、不想装任何东西 |
| 桌面 App | 下载安装 ChatGPT 桌面应用 | 需要读写本地文件、日常主力使用 |
| CLI 命令行 | 终端里运行 codex 命令 | 习惯命令行的开发者、在服务器上使用 |
| IDE 插件 | 在 VS Code、Cursor 或 Windsurf 里装扩展 | 已经在用这些编辑器的人 |

四种方式共用一个账号、共享额度，选一个最顺手的就行。

## 四、安装分步教学

### 1. Web 网页端（零安装）

直接打开 https://chatgpt.com/codex ，登录即可。

优点：不用装。缺点：不能直接访问本地文件夹，需要手动上传。

### 2. 桌面 App（推荐大多数人用）

**macOS：**
- 打开 App Store，搜索「ChatGPT」安装
- 需要 macOS 14 Sonoma 及以上

**Windows：**
- 打开 https://chatgpt.com/download 下载安装包
- 需要 Windows 10 及以上

打开后登录，看到 Codex 入口即成功。

### 3. CLI 命令行

**macOS / Linux：**
```bash
curl -fsSL https://chatgpt.com/codex/install.sh | sh
# 或
npm install -g @openai/codex
# 或 Homebrew
brew install codex
```

**Windows：**
```powershell
npm install -g @openai/codex
```

然后运行 `codex`，按提示用 ChatGPT 账号登录。

### 4. IDE 插件

在 VS Code 扩展市场搜索「Codex」或「OpenAI Codex」安装即可。

## 五、桌面 App 页面功能全解

桌面 App 左侧有四块主导航：新对话、搜索、已安排、插件。

### 主要区域说明（对照实际界面）

- **项目区**：按项目归类会话，同项目下共享上下文
- **会话标题**：建议改成任务名
- **内容区**：Codex 的回复与操作结果
- **附件列表**：本轮改动涉及的文件卡片
- **权限与模型区**：建议编程时开「完全访问」

实操建议：先建项目再开对话，改完文件后先看 Diff 和附件列表再 Accept。

其他页面包括：插件市场、已安排（定时任务）、账号菜单（用量与设置）、常规设置、MCP 服务器、连接（远程控制）、宠物（彩蛋）等。

## 六、CLI 命令行使用入门

```bash
codex                          # 进入交互模式
codex --workspace /path/to/project
codex 帮我创建一个 React 项目   # 一次性模式
```

常用命令：
- `/clear`：清空上下文
- `/model`：切换模型
- `/permissions`：管理权限
- `/cost`：查看用量

## 七、权限与安全设置（必看）

Codex 能操作文件和执行命令，权限非常重要。

1. **工作目录权限**：默认只能访问你指定的工作目录。不要用 `~/` 让它访问整个用户目录，给每个项目建独立文件夹。
2. **命令执行权限**：新手建议「每次询问」，熟悉后再调松。
3. **网络权限**：可设置白名单。
4. **Git 安全**：改之前先 commit；不要轻易让它 push；建议在独立分支操作。

## 八、第一次使用完整示范

场景：从零写一个网页计算器。

1. 启动 Codex（App / CLI / Web）
2. 指定空项目目录，如 `~/projects/my-calculator/`
3. 发指令：界面好看、支持键盘输入、生成 index.html
4. 看它分析需求、创建文件、显示 Diff
5. 审查并 Accept
6. 预览效果
7. 迭代修改（如改深色主题）

## 九、日常使用技巧

1. **写好 AGENTS.md**（类似 Karpathy 的做法）：在项目根目录放详细说明，当作给新同事的入职文档。
2. **指令要具体**：不要只说「修一下 bug」，要说清楚现象和组件。
3. **分步来**：别一口气提太多需求。
4. **用截图**：报错直接截图上传。
5. **不会了就问**：「接下来我应该做什么？」
6. **善用命令**：CLI 里用 `/help` 等快捷指令。

## 十、常见问题

**Q: Codex 和 Cursor 有什么区别？**  
Cursor 是 AI 编辑器，必须用它的编辑器。Codex 是 Agent，可在终端、网页、App、甚至 Cursor 里用。

**Q: Codex 和 Claude Code 有什么区别？**  
两者都是 coding agent。Codex 绑定 OpenAI 生态，Claude Code 绑定 Anthropic。

**Q: Plus 的额度够用吗？**  
日常开发一天几小时完全够。重度连续使用可能限速，先开 Plus 试一个月。

**Q: 生成的代码能直接上生产吗？**  
简单 CRUD、页面、脚本接近可用；复杂业务需要你 review。Codex 是加速器，不是替代思考。

**Q: 国内能用吗？**  
能。按 Gmail + Google Play 流程订阅，使用时需稳定访问 OpenAI 服务。

**Q: Codex 把代码搞坏了怎么办？**  
1. 改之前先 git commit  
2. 改动需手动 Accept / Reject  
3. 可直接说「撤销刚才的改动」

**Q: 能连数据库吗？**  
可以，建议用 .env，生产库要特别小心。

## 写在最后

跟完这篇，你应该能完成：Gmail / OpenAI 注册、Plus 订阅、至少一种 Codex 入口的安装、桌面 App 各页面对号入座、第一次完整跑通一个 demo。

更多文章可关注原作者公众号：老王霸 AI Lab

---

**本仓库用途**：供 Mac 本地部署的 Codex 阅读学习。你可以直接 clone 本仓库，然后让 Codex 以本目录为 workspace 进行学习与实践。

```bash
git clone https://github.com/Averyhank/codex-tutorial-laowang.git
cd codex-tutorial-laowang
codex
```

然后对 Codex 说：「请阅读 README.md，总结关键要点，并帮我实践其中的第一次使用示范。」
