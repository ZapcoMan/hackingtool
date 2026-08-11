<div align="center">

<img src="images/logo.svg" alt="HackingTool" width="600">

### AI 引导的授权安全测试一体化工具包

**21 个分类下精选 215 款工具** — 涵盖侦察、OSINT、Web、无线、钓鱼、
取证、后渗透等 — 并配备 **AI 层，可将自然语言转换为正确的工具和精确的命令**。

**面向** 渗透测试人员 · 红队人员 · 蓝队/SOC 和 DFIR 分析师 ·
OSINT 研究人员 · 漏洞赏金猎人 · CTF 选手 · 安全研究人员及
学生 — 所有人均**合法地在自己拥有或被授权测试的系统上工作**。

<a href="https://trendshift.io/repositories/869" target="_blank" rel="noopener noreferrer"><img src="https://trendshift.io/api/badge/repositories/869" alt="Z4nzu/hackingtool | Trendshift" width="250" height="55"/></a> <a href="https://trendshift.io/repositories/869" target="_blank" rel="noopener noreferrer"><img src="https://trendshift.io/api/badge/trendshift/repositories/869/daily?language=Python" alt="Z4nzu/hackingtool | Trendshift daily" width="250" height="55"/></a> <a href="https://trendshift.io/repositories/869" target="_blank" rel="noopener noreferrer"><img src="https://trendshift.io/api/badge/trendshift/repositories/869/weekly" alt="Z4nzu/hackingtool | Trendshift weekly" width="250" height="55"/></a>

<br/><br/>

[![License](https://img.shields.io/github/license/Z4nzu/hackingtool?style=flat-square&labelColor=0D1117&color=7B61FF)](LICENSE) [![Python](https://img.shields.io/badge/Python-3.10+-0D1117?style=flat-square&labelColor=0D1117&logo=python&logoColor=7B61FF)](https://www.python.org/) [![Stars](https://img.shields.io/github/stars/Z4nzu/hackingtool?style=flat-square&labelColor=0D1117&color=7B61FF)](https://github.com/Z4nzu/hackingtool/stargazers) [![Forks](https://img.shields.io/github/forks/Z4nzu/hackingtool?style=flat-square&labelColor=0D1117&color=7B61FF)](https://github.com/Z4nzu/hackingtool/network/members) [![Issues](https://img.shields.io/github/issues/Z4nzu/hackingtool?style=flat-square&labelColor=0D1117&color=7B61FF)](https://github.com/Z4nzu/hackingtool/issues) [![Last Commit](https://img.shields.io/github/last-commit/Z4nzu/hackingtool?style=flat-square&labelColor=0D1117&color=7B61FF)](https://github.com/Z4nzu/hackingtool/commits/master) [![Sponsor](https://img.shields.io/badge/Sponsor-%E2%9D%A4-DB61A2?style=flat-square&labelColor=0D1117&logo=githubsponsors&logoColor=DB61A2)](#support--sponsor)

<br/>

![](https://img.shields.io/badge/21_Categories-7B61FF?style=for-the-badge&labelColor=0D1117) &nbsp;![](https://img.shields.io/badge/215_Tools-7B61FF?style=for-the-badge&labelColor=0D1117) &nbsp;![](https://img.shields.io/badge/63_Tags-7B61FF?style=for-the-badge&labelColor=0D1117) &nbsp;![](https://img.shields.io/badge/AI--Guided-7B61FF?style=for-the-badge&labelColor=0D1117&logo=openai&logoColor=white) &nbsp;![](https://img.shields.io/badge/Linux_%7C_Kali_%7C_Parrot_%7C_macOS-7B61FF?style=for-the-badge&labelColor=0D1117&logo=linux&logoColor=white)

<br/>

<a href="#installation"><img src="https://img.shields.io/badge/Install_Now-7B61FF?style=for-the-badge&logo=rocket&logoColor=white" alt="Install Now"></a>&nbsp; <a href="docs/HOW-TO-USE.md"><img src="https://img.shields.io/badge/How_to_Use-30363D?style=for-the-badge&logo=gnometerminal&logoColor=white" alt="How to Use"></a>&nbsp; <a href="docs/TOOLS.md"><img src="https://img.shields.io/badge/Tool_Catalog-30363D?style=for-the-badge&logo=github&logoColor=white" alt="Tool Catalog"></a>&nbsp; <a href="#support--sponsor"><img src="https://img.shields.io/badge/%E2%9D%A4_Sponsor-DB61A2?style=for-the-badge&logo=githubsponsors&logoColor=white" alt="Sponsor"></a>

</div>

---

## 目录

- [为什么选择 hackingtool](#为什么选择-hackingtool)
- [工具分类](#工具分类)
- [安装](#安装)
  - [通过 pipx 从源码安装（推荐）](#通过-pipx-从源码安装推荐)
  - [开发环境安装](#开发环境安装)
  - [Docker](#docker)
  - [可选运行时](#可选运行时)
- [快速命令](#快速命令)
  - [命令参考](#命令参考)
- [功能特性](#功能特性)
  - [🔎 `/find` — 为你尚未拥有的需求找到工具](#-find--为你尚未拥有的需求找到工具)
  - [🎯 `/goal` — 规划目标，逐步执行](#-goal--规划目标逐步执行)
  - [🧠 智能推荐 — 用自然语言描述你的需求](#-智能推荐--用自然语言描述你的需求)
  - [🏷 标签与搜索](#-标签与搜索)
  - [▶ 后台面板（tmux）](#-后台面板tmux)
  - [⚙ 设置与 AI 层](#-设置与-ai-层)
  - [📋 无头（Headless）测试任务](#-无头headless测试任务)
- [文档](#文档)
- [贡献](#贡献)
- [支持与赞助](#支持与赞助)
- [社交媒体](#社交媒体)

---

## 为什么选择 hackingtool

- **🧠 AI 引导的工作流** — 描述你想要什么（如"查找 example.com 的子域名"），
  它会将你的意图映射到正确的工具，提供精确的已文档化命令，逐步规划目标，
  然后总结发现并起草测试报告。自带 API 密钥或运行本地模型 — 不会自动执行任何操作，
  也不会编造任何内容。
- **🗂 215 款精选工具，一个控制台** — 跨 21 个分类安装和运行，无需到处找 Git 仓库；
  固定的标签分类法（使用中 63 个标签）让每个工具都可被发现。
- **🔎 它知道自己缺什么** — `/find` 先搜索你的工具目录，再搜索
  GitHub API，展示真正维护中的项目并给出每个项目的排名理由。
- **🛡 默认安全** — 标准安装，**不用 `curl | bash`**，下载锁定版本 +
  SHA-256 校验，列表形式 `subprocess`，不强制 `sudo`，
  以及[带 SBOM 的签名发布](SECURITY.md#verifying-a-release)。
- **🎯 面向全频谱用户** — 红队、蓝队、OSINT、漏洞赏金、CTF/THM、
  取证/IR — 所有操作**仅限授权目标**。

<div align="center">
<img src="images/screenshots/1.png" alt="hackingtool console: banner with live system readout and the / command palette" width="900">
<br/>
<sub>控制台启动界面 — 实时系统信息读取，输入 <code>/</code> 打开命令面板。</sub>
</div>

---

## 工具分类

**21 个分类下共 215 款工具** — 完整列表（含链接和标签）见
**[docs/TOOLS.md](docs/TOOLS.md)**。

<div align="center">

| # | 分类 | 工具数 | | # | 分类 | 工具数 |
|:---:|---|:---:|---|:---:|---|:---:|
| 1 | 🛡 [匿名隐藏工具](docs/TOOLS.md#-anonymously-hiding-tools) | 5 | | 12 | 🔁 [逆向工程工具](docs/TOOLS.md#-reverse-engineering-tools) | 10 |
| 2 | 🔍 [信息收集工具](docs/TOOLS.md#-information-gathering-tools) | 26 | | 13 | ⚡ [DDoS 攻击工具](docs/TOOLS.md#-ddos-attack-tools) | 7 |
| 3 | 📚 [字典生成器](docs/TOOLS.md#-wordlist-generator) | 8 | | 14 | 🖥 [远程管理工具（RAT）](docs/TOOLS.md#-remote-administrator-tools-rat) | 4 |
| 4 | 📡 [无线攻击工具](docs/TOOLS.md#-wireless-attack-tools) | 17 | | 15 | 🧪 [XSS 攻击工具](docs/TOOLS.md#-xss-attack-tools) | 6 |
| 5 | 💉 [SQL 注入工具](docs/TOOLS.md#-sql-injection-tools) | 7 | | 16 | 🖼 [隐写术工具](docs/TOOLS.md#-steganography-tools) | 10 |
| 6 | 🎣 [钓鱼攻击工具](docs/TOOLS.md#-phishing-attack-tools) | 13 | | 17 | 🏢 [活动目录工具](docs/TOOLS.md#-active-directory-tools) | 10 |
| 7 | 🌐 [Web 攻击工具](docs/TOOLS.md#-web-attack-tools) | 23 | | 18 | ☁ [云安全工具](docs/TOOLS.md#-cloud-security-tools) | 7 |
| 8 | 🔧 [后渗透工具](docs/TOOLS.md#-post-exploitation-tools) | 15 | | 19 | 📱 [移动安全工具](docs/TOOLS.md#-mobile-security-tools) | 6 |
| 9 | 🕵 [取证工具](docs/TOOLS.md#-forensic-tools) | 12 | | 20 | ✨ [其他工具](docs/TOOLS.md#-other-tools) | 10 |
| 10 | 📦 [Payload 生成工具](docs/TOOLS.md#-payload-creation-tools) | 6 | | 21 | 🔑 [密码/哈希破解](docs/TOOLS.md#-password--hash-cracking) | 7 |
| 11 | 🧰 [漏洞利用框架](docs/TOOLS.md#-exploit-framework) | 6 | | | | |

</div>

<sub>另有 59 个条目已归档（上游不再维护或已失效），除非你通过 `/config` 设置
`show_archived true`，否则默认隐藏。应用内头部显示 22 个分类 / 217 款工具，
是因为它还计入了内置的更新/卸载菜单。</sub>

---

## 安装

需要 **Python 3.10+**，运行于 **Linux 或 macOS**（Kali、Parrot、Debian/Ubuntu、Arch 等）。
不支持 Windows — 程序会提示并退出。不使用 `curl | bash`：
以下所有路径均为标准、可验证的安装方式。

### 通过 pipx 从源码安装（推荐）

[pipx](https://pipx.pypa.io) 会将 hackingtool 安装到独立的隔离环境中，
并将 `hackingtool` 命令加入你的 PATH，因此可以从任意目录启动。

```bash
# 1 — 获取代码
git clone https://github.com/Z4nzu/hackingtool.git
cd hackingtool

# 2 — 安装到 PATH（隔离 venv，不影响系统 Python）
pipx install .

# 3 — 从任意位置运行
hackingtool
```

还没有 pipx？

```bash
# macOS
brew install pipx && pipx ensurepath

# Debian / Ubuntu / Kali
sudo apt install pipx && pipx ensurepath
```

执行 `pipx ensurepath` 后请打开一个新终端窗口，使 PATH 更改生效。
后续更新：`git pull && pipx install . --force`。卸载：
`pipx uninstall hackingtool`。

<details>
<summary>替代方案：<code>uv tool install .</code>（效果相同，使用 uv 替代 pipx）</summary>

```bash
git clone https://github.com/Z4nzu/hackingtool.git
cd hackingtool
uv tool install .        # 将 hackingtool 可执行文件安装到 PATH
hackingtool
```
</details>

<details>
<summary>替代方案：纯 venv + pip（不修改 PATH）</summary>

```bash
git clone https://github.com/Z4nzu/hackingtool.git
cd hackingtool
python3 -m venv .venv && . .venv/bin/activate
pip install .            # 或：pip install -e .   用于可编辑的开发安装
hackingtool
```

该命令仅在 venv 激活期间位于 PATH 中。
</details>

### 开发环境安装

[uv](https://docs.astral.sh/uv/) 一步创建虚拟环境并从 `pyproject.toml` / `uv.lock` 安装所有依赖：

```bash
git clone https://github.com/Z4nzu/hackingtool.git
cd hackingtool
uv sync
uv run hackingtool
```

还没有 uv？`pipx install uv`（或参阅
[uv 安装文档](https://docs.astral.sh/uv/getting-started/installation/)）。

**要贡献代码？** `make setup` 配置 pre-push 钩子，`make check` 运行完整检查
（lint + 测试 + 目录验证）。详见 [CONTRIBUTING.md](CONTRIBUTING.md)。

### Docker

拉取并运行已发布的镜像：

```bash
docker run -it --rm hardikzinzu/hackingtool:latest
```

或从检出的代码本地构建：

```bash
git clone https://github.com/Z4nzu/hackingtool.git && cd hackingtool
docker build -t hackingtool .
docker run -it --rm hackingtool
```

<!-- 隐藏，待这些分发渠道上线后恢复。当软件包发布到 PyPI 且 .deb 附加到 release 时恢复。

### pipx / pip 从 PyPI 安装

```bash
pipx install hackingtool
hackingtool
```

```bash
python3 -m venv .venv && . .venv/bin/activate
pip install hackingtool
hackingtool
```

### Debian / Ubuntu / Kali（.deb）

从 [最新 release](https://github.com/Z4nzu/hackingtool/releases/latest) 获取 `.deb`：

```bash
sudo apt install ./hackingtool_*.deb
hackingtool
```
-->

### 可选运行时

部分工具需要特定语言运行时来安装/运行；核心应用本身不需要。

| 依赖 | 版本 | 用于 |
|---|---|---|
| Go | 1.21+ | nuclei, ffuf, amass, httpx, katana, dalfox, gobuster, subfinder |
| Ruby | 任意 | haiti, evil-winrm |
| tmux | 任意 | 后台面板（`/run … &`、`/panes`、`/attach`） |
| Docker | 任意 | Mythic, MobSF（可选） |

---

## 快速命令

启动 `hackingtool` 后直接输入即可。只有三种输入方式：

| 输入 | 含义 | 示例 |
|---|---|---|
| `/…` | 执行命令 | `/search subdomain` |
| `@…` | 指定名称 | `@nmap`, `@tag:osint` |
| 其他内容 | 自然语言描述"我想做什么" | `crack a wifi handshake` |

<div align="center">
<img src="images/screenshots/4.png" alt="typing @ in the hackingtool console completes tool names" width="900">
<br/>
<sub><code>@</code> 补全工具名 — <code>@tag:</code> 补全标签，<code>/</code> 补全命令。</sub>
</div>

### 命令参考

| 命令 | 别名 | 功能 |
|---|---|---|
| `/run <工具> [参数] [&]` | `/open` | 打开工具菜单；尾部加 `&` 则在后台 tmux 面板中运行（参数即在此使用） |
| `/search <关键词>` | | 按名称、描述或标签搜索工具 |
| `/tags` | | 列出所有标签及其工具数量 |
| `/ai <目标>` | `/recommend`, `/r` | 为目标推荐工具 |
| `/goal <目标>` | | AI 规划目标并逐步执行，每步需确认 |
| `/find <需求>` | `/discover` | 为需求查找工具 — 先查目录，再查 GitHub（仅建议，不安装） |
| `/panes` | `/jobs` | 列出后台面板 |
| `/attach` | | 连接到后台会话（`Ctrl-b` `d` 返回） |
| `/kill <标签\|all>` | | 终止单个后台面板，或全部 |
| `/config [键 值]` | | 查看/修改设置；`/config test` 检查 AI 连接，`/config github` 检查 GitHub 令牌 |
| `/skill` | | 显示操作手册 |
| `/update` · `/uninstall` | `/remove` | 更新系统包或 hackingtool · 移除 hackingtool 及其工具 |
| `/clear` | `/cls` | 清屏 |
| `/back` | `/b` | 退出当前工具并返回 |
| `/help` | `/?`, `/h` | 快速参考卡片 |
| `/quit` | `/q`, `/exit` | 退出（也可用 `q`、`Ctrl-C`、`Ctrl-D`） |
| `@<工具>` | | 打开工具（不区分大小写，模糊匹配兜底） |
| `@tag:<标签>` | | 列出并选择带有该标签的工具 |

分类内：`1–N` 选择工具 · `97` 安装所有未安装的工具 ·
`98` 已归档工具 · `99` 返回。
工具内：`1` 安装 · `2` 运行 · `c` 询问针对你目标的确切命令 ·
`98` 项目页面 · `99` 返回。

<div align="center">
<img src="images/screenshots/5.png" alt="hackingtool /help quick reference card" width="900">
<br/>
<sub><code>/help</code> — 应用内的同一张参考卡片。</sub>
</div>

在非交互式终端（或未安装 `prompt_toolkit`）中，hackingtool 会回退到经典数字菜单，
其中 `/` 或 `s` 搜索，`t` 按标签过滤，`r` 或 `a` 推荐，`?` 帮助，`q` 退出。
使用 `hackingtool --classic` 可强制启用。

> **新用户？** [docs/HOW-TO-USE.md](docs/HOW-TO-USE.md) 逐步讲解了上述每项操作，
> 含编号步骤。

---

## 功能特性

### 🔎 `/find` — 为你尚未拥有的需求找到工具

先搜索 215 款精选工具，再搜索 GitHub 搜索 API，并对结果进行可解释的排名。
**仅建议** — 不会克隆、安装或运行任何东西 — 且**不发起任何模型调用**。

```
/find crack a wpa handshake

In your toolbox (vetted)
  • aircrack-ng (WiFi security suite)
  • Kismet (wireless detector / WIDS)
  • Reaver (WPS PIN attack)
  • WiGLE (wardriving map & API)
  • hashcat example hashes (WPA mode 22000)

Found on GitHub — NOT vetted by us

  wifiphisher/wifiphisher  14713★  GPL-3.0
    The Rogue Access Point Framework
    14713★ · trusted author (ships in our catalog) · active · matches: security, wifi
    git clone https://github.com/wifiphisher/wifiphisher
  …
```

按 `a` 保存结果：它会被写入 `~/.hackingtool/found.yaml` 作为
"已发现工具"条目 — 包含标题、标签、描述、链接，**不含安装或运行命令**，
因此已发现条目永远不会执行任何操作。下次启动时它会出现在你的菜单和
`/search` 中。

超出范围的请求（干扰、DoS、批量目标攻击、恶意软件）会在**发起任何网络请求之前**
被拒绝，并在存在授权替代方案时提供。防御性/DFIR 相关的描述永远不会被拒绝。

匿名使用时 GitHub 搜索限制为 10 次/分钟；配置一个**无范围、无权限**的令牌
可提升至 30 次/分钟 — 详见
[`/config github`](docs/HOW-TO-USE.md#7-add-a-github-token-for-find-config-github)。

### 🎯 `/goal` — 规划目标，逐步执行

```
/goal find live subdomains of example.com
```

hackingtool 会起草一个简短的实命令计划（含每步理由和未安装工具的安装提示），
要求你确认已**获得授权**测试目标，然后逐步执行：`[y]` 运行 · `[s]` 跳过 ·
`[e]` 编辑 · `[q]` 中止。每步以列表形式运行 — 绝不通过 shell — 每个目标会在
`~/.hackingtool/goals/` 下创建带时间戳的工作区，包含 `plan.json`、
UTC 时间戳 `run.log` 及每步的原始输出。

模型**仅调用一次**用于规划；工具输出永远不会回传给模型。
未配置模型时，`/goal` 退化为对同一目标的工具推荐。

### 🧠 智能推荐 — 用自然语言描述你的需求

纯文本输入（或 `/ai`）将意图映射到工具。模型只能返回固定分类法中的标签，
目录负责将标签解析为工具，因此绝不会凭空捏造工具；
模型不可达时，由标准库关键词匹配器代替回答。

<div align="center">
<img src="images/screenshots/3.png" alt="hackingtool /ai — pick a common task or describe your own" width="900">
<br/>
<sub><code>/ai</code> — 选择一个常见任务，或用自己的话描述需求。</sub>
</div>

### 🏷 标签与搜索

`/tags` 打印所有使用中的标签及其工具数量；`@tag:<名称>` 打开
带有该标签的工具；`/search <关键词>` 匹配名称、描述和标签。

<div align="center">
<img src="images/screenshots/2.png" alt="hackingtool /tags — every tag with its tool count" width="900">
<br/>
<sub><code>/tags</code> — 使用中的 63 个标签，每个标签后的工具数量。</sub>
</div>

### ▶ 后台面板（tmux）

长时间扫描不应阻塞你的控制台。安装 tmux 后，`/run <工具> … &` 会在一个
分离的 `hackingtool` 会话中打开带标签的窗口：

```
/run nmap -sV -oA scan 10.0.0.5 &
▶ started 'nmap' in background — /attach to view
```

`/panes` 列出面板，`/attach` 查看某个面板（`Ctrl-b` `d` 返回），
`/kill <标签>` 或 `/kill all` 终止面板，提示符下方的状态栏显示 `▶ N running`。
没有 tmux？程序会提示并以行内方式打开工具；使用
`/config background_runner off` 可完全禁用。

### ⚙ 设置与 AI 层

`/config` 打开全屏设置编辑器（`↑↓` 移动，`←→` 切换，`Enter` 编辑，
`t` 测试连接，`Esc` 关闭）；`/config <键> <值>` 从提示符直接设置单个键。
设置保存在 `~/.hackingtool/config.json`。

AI 层**可选择启用，自带密钥**：设置 `ai_base_url` + API 密钥后使用
OpenAI 兼容端点，否则使用本地 [Ollama](https://ollama.com)，再否则
不启用 — 所有功能退化为确定性的离线行为，不会猜测。
你的 API 密钥仅写入 `~/.hackingtool/.env`（权限 600），
绝不写入 `config.json`，也绝不回显。`/config test` 在探测失败时
报告真实失败原因。

### 📋 无头（Headless）测试任务

同一目录驱动一个非交互式编排器，将工具输出标准化为一份 `findings.json`：

```bash
hackingtool --engagement acme --targets example.com --pipeline recon
hackingtool --engagement acme --report          # 确定性 Markdown 报告
hackingtool --engagement acme --ai-summary      # 可选：对真实发现的快速分拣
hackingtool --engagement acme --ai-report       # 可选：叙事性报告草稿（report.draft.md）
```

超出范围的目标会在运行前被标记并记录，AI 通道只会总结已存在的发现。

---

## 文档

| 文档 | 内容 |
|---|---|
| [如何使用 hackingtool](docs/HOW-TO-USE.md) | 编号操作指南：首次运行、`/find`、`/goal`、`/config`、后台面板、无头模式 |
| [工具目录](docs/TOOLS.md) | 每款工具，按分类排列，含链接和标签 |
| [操作手册](src/hackingtool/skill/OPERATOR.md) | AI 层遵循的准则和规则（也可用 `/skill` 查看） |
| [SECURITY.md](SECURITY.md) | 披露策略、发布验证、威胁模型 |
| [CONTRIBUTING.md](CONTRIBUTING.md) | 以目录为先的工具添加方式，PR 必须通过的检查 |

---

## 贡献

欢迎新工具、修复和文档贡献 — **仅限授权安全测试用途**。

> **简单路径：** 大多数工具只需在 `src/hackingtool/catalog/` 中添加
> **一个 YAML 条目** — 无需编写 Python。标签来自固定分类法，
> 因此你的工具可即时被发现和搜索。

| 我想… | 操作 |
|---|---|
| 💡 建议工具 | 提交一个 [工具请求](.github/ISSUE_TEMPLATE/tool_request.md) Issue |
| ➕ 添加工具 | 添加目录条目（或编写自定义安装/运行逻辑的类），然后使用[模板](.github/PULL_REQUEST_TEMPLATE.md)提交 PR |
| 🐛 报告 Bug | 提交一个 [Bug 报告](.github/ISSUE_TEMPLATE/bug_report.md) Issue |
| 🔒 报告漏洞 | **私密报告** — 不要提交公开 Issue；参见 [SECURITY.md](SECURITY.md) |

提交 PR 前，运行 **`make check`**（lint + 测试 + 目录验证），
标题格式为 `[New Tool] 名称 — 分类`。完整指南 — 安全规则和
单条目目录操作指南 — 见 **[CONTRIBUTING.md](CONTRIBUTING.md)**。

<sub>📄 [贡献](CONTRIBUTING.md) · [安全](SECURITY.md) · [行为准则](CODE_OF_CONDUCT.md)</sub>

---

<!-- Star History — 后续启用。
     GitHub 现在限制了匿名的 star-history 数据，因此实时图表无法渲染。
     启用方法：打开 https://star-history.com/#Z4nzu/hackingtool&Date（用 GitHub
     令牌登录 — 这是你的仓库），下载图表图片，保存为
     images/star-history.png，然后取消注释下方代码块。

## Star History

<div align="center">
<a href="https://star-history.com/#Z4nzu/hackingtool&Date"><img src="images/star-history.png" alt="HackingTool Star History Chart" width="640"></a>
</div>

---
-->

## 支持与赞助

hackingtool 是免费且开源的。如果它在测试任务中为你节省了时间或帮助你学习，
请考虑赞助 — 资金将用于工具整理、AI 层开发以及保持安装安全和最新。

<a href="https://github.com/sponsors/Z4nzu"><img src="https://img.shields.io/badge/GitHub_Sponsors-EA4AAA?style=for-the-badge&logo=githubsponsors&logoColor=white" alt="Sponsor on GitHub"></a>&nbsp; <a href="https://buymeacoffee.com/hardikzinzu" target="_blank"><img src="https://img.shields.io/badge/Buy_Me_A_Coffee-1F2328?style=for-the-badge&logo=buymeacoffee&logoColor=FFDD00" alt="Buy Me A Coffee"></a>

⭐ 为仓库加星是免费的，还能帮助更多人发现这个项目。

## 社交媒体

[![Twitter](https://img.shields.io/badge/Twitter-Follow-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/_Zinzu07) [![GitHub](https://img.shields.io/badge/GitHub-Follow-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Z4nzu/)

> **仅限授权安全测试用途。**
> 感谢 hackingtool 中包含的所有工具的原始作者。

你最喜欢的工具没有列出？[在此建议](https://github.com/Z4nzu/hackingtool/issues/new?template=tool_request.md)
