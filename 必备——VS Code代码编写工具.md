---
tags:
  - vscode
  - 介绍
  - 安装
  - windows
  - mac
  - linux
---
**文档目录**
- [📌 一、VSCode 有什么用？（核心功能和优势）](#%F0%9F%93%8C%20%E4%B8%80%E3%80%81VSCode%20%E6%9C%89%E4%BB%80%E4%B9%88%E7%94%A8%EF%BC%9F%EF%BC%88%E6%A0%B8%E5%BF%83%E5%8A%9F%E8%83%BD%E5%92%8C%E4%BC%98%E5%8A%BF%EF%BC%89)
- [📥 二、VSCode 详细安装步骤](#%F0%9F%93%A5%20%E4%BA%8C%E3%80%81VSCode%20%E8%AF%A6%E7%BB%86%E5%AE%89%E8%A3%85%E6%AD%A5%E9%AA%A4)
	- [步骤 0: 确认你的操作系统](#%E6%AD%A5%E9%AA%A4%200:%20%E7%A1%AE%E8%AE%A4%E4%BD%A0%E7%9A%84%E6%93%8D%E4%BD%9C%E7%B3%BB%E7%BB%9F)
	- [步骤 1: 下载安装包](#%E6%AD%A5%E9%AA%A4%201:%20%E4%B8%8B%E8%BD%BD%E5%AE%89%E8%A3%85%E5%8C%85)
	- [步骤 2: 运行安装程序](#%E6%AD%A5%E9%AA%A4%202:%20%E8%BF%90%E8%A1%8C%E5%AE%89%E8%A3%85%E7%A8%8B%E5%BA%8F)
		- [🖥️ Windows:](#%F0%9F%96%A5%EF%B8%8F%20Windows:)
		- [🍎 macOS:](#%F0%9F%8D%8E%20macOS:)
		- [🐧 Linux (以 .deb 包在 Ubuntu/Debian 为例):](#%F0%9F%90%A7%20Linux%20(%E4%BB%A5%20.deb%20%E5%8C%85%E5%9C%A8%20Ubuntu/Debian%20%E4%B8%BA%E4%BE%8B):)
	- [步骤 3: 首次启动与基本设置](#%E6%AD%A5%E9%AA%A4%203:%20%E9%A6%96%E6%AC%A1%E5%90%AF%E5%8A%A8%E4%B8%8E%E5%9F%BA%E6%9C%AC%E8%AE%BE%E7%BD%AE)
	- [📝 补充说明](#%F0%9F%93%9D%20%E8%A1%A5%E5%85%85%E8%AF%B4%E6%98%8E)

Visual Studio Code（简称 VSCode）是一款由微软开发的**免费、开源、跨平台（Windows, macOS, Linux）** 的源代码编辑器。它功能强大、轻量快速、扩展性极强，深受开发者喜爱，几乎可用于任何编程语言或开发任务。

## 📌 一、VSCode 有什么用？（核心功能和优势）

1. **核心代码编辑：**
    
    - 语法高亮：让不同代码元素（关键字、变量、字符串等）显示不同颜色，提高可读性。
        
    - 智能感知：强大的代码补全（IntelliSense），根据上下文、变量类型、导入的模块等提供精准的代码提示和自动完成。
        
    - 错误和警告检查：实时在代码编辑器中标记语法错误、潜在问题（如未使用的变量）、类型错误（配合语言扩展）等。
        
    - 代码片段：快速插入常用代码模板（如`for`循环、函数定义）。
        
    - 代码格式化：一键或保存时自动按照规则格式化代码，保持风格统一。
        
    - 代码折叠：折叠函数、循环等代码块，便于浏览大型文件。
        
    - 多光标编辑：同时在多个位置编辑相同或不同的文本，提高效率。
        
    - 强大的搜索和替换：
        
        - 在单个文件中搜索/替换。
            
        - 在整个项目文件夹中全局搜索/替换（支持正则表达式）。
            
        - 在搜索结果中直接预览和编辑。
            
2. **集成终端：**
    
    - 内置命令行终端（PowerShell, CMD, bash, zsh 等，取决于你的系统）。
        
    - 无需切换窗口，直接在编辑器下方运行命令、编译代码、执行脚本、使用版本控制命令（git）等。
        
    - 可同时打开多个终端标签页。
        
3. **内置 Git 支持：**
    
    - 可视化的源代码版本控制（Git）。
        
    - 直接在侧边栏查看文件状态（已修改、已暂存、未跟踪）。
        
    - 对比文件差异（Diff）。
        
    - 提交（Commit）、拉取（Pull）、推送（Push）、分支管理、解决合并冲突等常用操作，大部分可以通过界面完成。
        
4. **强大的调试功能：**
    
    - 内置调试器，支持断点、单步执行、查看变量值、调用堆栈等。
        
    - 需要安装相应语言的调试扩展（如 Python, C++, Node.js, Go 等）。
        
    - 提供图形化的调试界面，配置调试环境相对直观。
        
5. **无与伦比的扩展性：**
    
    - **核心优势！** VSCode 本身是一个功能优秀的编辑器，但通过 **扩展市场**，你可以将其打造成一个功能完备的 **IDE**。
        
    - 数以万计的免费扩展，涵盖：
        
        - 语言支持：为几乎所有主流编程语言（Python, Java, C/C++, JavaScript/TypeScript, Go, Rust, PHP, Ruby, SQL...）和标记语言（HTML, CSS, Markdown, LaTeX...）提供增强支持（语法高亮、智能感知、调试、格式化、Linting 等）。
            
        - 主题：大量颜色主题和文件图标主题，个性化你的编辑器外观。
            
        - 工具集成：连接数据库、Docker、远程开发（SSH, WSL, Containers）、测试框架、项目管理工具等。
            
        - 生产力工具：增强编辑体验（更好的代码片段、快捷键、自动补全等）。
            
        - ...几乎任何你能想到的功能都能找到扩展。
            
6. **跨平台：** 在 Windows、macOS 和 Linux 上提供几乎一致的体验。
    
7. **轻量级与高性能：** 相比大型 IDE（如 Visual Studio, Eclipse, IntelliJ IDEA），启动和运行速度通常更快，占用资源更少。
    
8. **远程开发：** 通过扩展，可以无缝地在远程服务器、容器（Docker）或 Windows Subsystem for Linux (WSL) 中进行开发，仿佛代码就在本地一样。
    
9. **可定制性：** 通过用户设置（`settings.json`）和键盘快捷键（`keybindings.json`）文件，几乎可以调整编辑器的每一个行为。
    
10. **开源免费：** 完全免费使用，代码开源在 GitHub 上。
    

**总结：** VSCode 是一个现代、高效、高度可定制的代码编辑器核心，通过其庞大的扩展生态系统，它可以胜任从简单脚本编写到复杂项目开发的广泛任务，是当今最流行的开发者工具之一。

---

## 📥 二、VSCode 详细安装步骤

### 步骤 0: 确认你的操作系统

- **Windows:** Windows 7, 8, 10, 11 (64-bit 推荐)
    
- **macOS:** macOS 10.11 (El Capitan) 或更高版本
    
- **Linux:** 大多数主流发行版（Debian, Ubuntu, Red Hat, Fedora, SUSE 等）都有官方支持的安装包（`.deb`, `.rpm`）和社区支持的包（如 Snap, Flatpak）。
    

### 步骤 1: 下载安装包

1. 打开 VSCode 官方网站：[https://code.visualstudio.com/](https://code.visualstudio.com/)
    
2. 网站会自动检测你的操作系统，并显示对应的大下载按钮（通常是蓝色的 "Download for ..."）。确认显示的版本符合你的系统。
    
    - 如果你想下载其他平台的版本，点击下载按钮旁边的下拉箭头 ▼ 进行选择。
        
    - **Windows 用户注意：** 通常会提供 `User Installer` (推荐给大多数用户，安装到用户目录) 和 `System Installer` (需要管理员权限，安装到系统目录) 两种选择。选择 `User Installer` 即可。
        
    - **Linux 用户注意：** 选择适合你发行版的包格式（`.deb` 用于 Debian/Ubuntu, `.rpm` 用于 Red Hat/Fedora/SUSE）或使用 Snap/Flatpak。
        

### 步骤 2: 运行安装程序

#### 🖥️ Windows:

1. 找到下载好的安装文件（通常是 `VSCodeUserSetup-x64-{version}.exe`）。
    
2. 双击运行它。
    
3. **用户账户控制 (UAC)** 可能会弹出提示，点击 **“是”**。
    
4. 打开安装向导，点击 **“下一步”**。
    
5. **许可协议：** 阅读协议，选择 **“我接受协议”**，然后点击 **“下一步”**。
    
6. **选择目标位置：** 默认安装位置通常是 `C:\Users\{你的用户名}\AppData\Local\Programs\Microsoft VS Code`。如果你想更改，点击 **“浏览”** 选择其他位置，否则直接点击 **“下一步”**。
    
7. **选择开始菜单文件夹：** 保持默认即可，点击 **“下一步”**。
    
8. **选择附加任务 (非常重要！)：**
    
    - **“创建桌面快捷方式”**：推荐勾选。
        
    - **“将‘通过 Code 打开’操作添加到 Windows 资源管理器文件上下文菜单”**：推荐勾选。这样在文件或文件夹上右键时，可以选择“通过 Code 打开”。
        
    - **“将‘通过 Code 打开’操作添加到 Windows 资源管理器目录上下文菜单”**：同上，推荐勾选。
        
    - **“将 Code 注册为受支持的文件类型的编辑器”**：推荐勾选。让 VSCode 成为默认打开代码文件的程序。
        
    - **“添加到 PATH (重启后生效)”**：**强烈推荐勾选！** 这将允许你在系统的命令行（CMD、PowerShell）或终端中直接输入 `code` 或 `code .` 命令来启动 VSCode 或打开当前文件夹。这是非常方便的功能。
        
9. 确认选择后，点击 **“下一步”**。
    
10. **准备安装：** 点击 **“安装”**。
    
11. 等待安装完成。
    
12. **安装完成：** 确保 **“启动 Visual Studio Code”** 被勾选，然后点击 **“完成”**。VSCode 将首次启动。
    

#### 🍎 macOS:

1. 找到下载好的文件（通常是 `VSCode-darwin-universal.zip` 或类似名称）。
    
2. 双击 `.zip` 文件进行解压缩（如果浏览器没有自动解压）。这会在你的下载文件夹（或指定位置）生成一个名为 `Visual Studio Code.app` 的应用程序。
    
3. 将 `Visual Studio Code.app` **拖拽**到你的 **“应用程序”** (`Applications`) 文件夹中。
    
4. **（重要）添加到 PATH：**
    
    - 打开 VSCode。
        
    - 按下 `Cmd + Shift + P` 打开命令面板。
        
    - 输入 `shell command`，在出现的列表中选择 **“Shell Command: Install 'code' command in PATH”**。
        
    - 执行此命令后，你就可以在终端（Terminal）中直接输入 `code` 或 `code .` 来启动 VSCode 或打开当前文件夹了。
        
5. **（可选）添加到 Dock：** 在“应用程序”文件夹中找到 `Visual Studio Code.app`，右键点击并选择 **“选项”** > **“在程序坞中保留”**。
    

#### 🐧 Linux (以 .deb 包在 Ubuntu/Debian 为例):

1. **方法一：使用图形界面**
    
    - 找到下载好的 `.deb` 文件（如 `code_x.x.x-xxxxxxxxxx_amd64.deb`）。
        
    - 双击该文件。它通常会使用默认的软件中心（如 Ubuntu Software）打开。
        
    - 点击 **“安装”** 按钮，输入你的用户密码进行验证。
        
    - 等待安装完成。
        
2. **方法二：使用终端 (推荐)**
    
    - 打开终端 (`Ctrl+Alt+T`)。
        
    - 导航到你下载 `.deb` 文件的目录，例如：
    
	```bash
cd ~/Downloads
	```

	- 使用`sudo dpkg`命令安装：

	```bash
sudo dpkg -i code_x.x.x-xxxxxxxxxx_amd64.deb
#将 `code_x.x.x-xxxxxxxxxx_amd64.deb` 替换为你实际下载的文件名
```
        
    - 如果报告依赖关系问题，运行以下命令修复：
	```bash
	sudo apt-get install -f
```
	- 安装完成后，你可以在应用菜单中找到 VSCode，或者直接在终端输入 `code` 启动。

 
3. **添加到 PATH：** 使用上述方法安装后，`code` 命令通常已经自动添加到 PATH。你可以在终端直接输入 `code` 或 `code .` 测试。


### 步骤 3: 首次启动与基本设置

1. **欢迎界面：** 首次启动会显示欢迎页面，提供学习资源、自定义选项等。
    
2. **选择颜色主题：**
    
    - 点击左侧活动栏最下方的齿轮图标 🛠 (管理) -> 命令面板 (`Ctrl+Shift+P` / `Cmd+Shift+P`)。
        
    - 输入 `color theme`，选择 **“Preferences: Color Theme”**。
        
    - 使用上下键预览不同的主题（如深色 `Dark (Visual Studio)`，浅色 `Light (Visual Studio)`，流行的 `Dark+ (default dark)`），按 `Enter` 键应用。
        
3. **安装扩展 (关键步骤！):**
    
    - VSCode 的强大在于扩展。点击左侧活动栏的 **方块图标** 或按 `Ctrl+Shift+X` / `Cmd+Shift+X` 打开扩展视图。
        
    - 在搜索框中输入你需要的语言或工具名称（如 `python`, `java`, `c++`, `prettier`, `chinese`）。
        
    - 找到官方或高评分的扩展（通常由 Microsoft 发布或 Verified 认证），点击 **“Install”** 按钮。
        
    - **常用必备扩展举例：**
        
        - **Chinese (Simplified) Language Pack for Visual Studio Code:** 中文语言包。
            
        - **Python:** Microsoft 官方 Python 支持（智能感知，调试，Linting 等）。
            
        - **Prettier - Code formatter:** 流行的代码格式化工具（支持 JS/TS/HTML/CSS/JSON 等）。
            
        - **ESLint:** JavaScript/TypeScript 代码质量和风格检查。
            
        - **GitLens:** 增强 Git 功能（代码作者信息、提交历史等）。
            
        - **Live Server:** 为 HTML/CSS/JS 提供实时预览。
            
        - **Docker:** 管理 Docker 容器和镜像。
            
        - **Remote - SSH:** 远程开发（通过 SSH 连接到服务器）。
            
        - **Remote - WSL:** 在 Windows 上无缝使用 WSL。
            
4. **打开文件夹或文件：**
    
    - **文件 > 打开文件夹...** (`Ctrl+K Ctrl+O` / `Cmd+K Cmd+O`): 打开一个项目文件夹。
        
    - **文件 > 打开文件...** (`Ctrl+O` / `Cmd+O`): 打开单个文件。
        
    - 在终端或文件资源管理器中使用 `code .` 命令打开当前文件夹。
        

### 📝 补充说明

- **更新：** VSCode 会自动检查更新并在有更新时在左下角显示一个提示（齿轮图标旁出现蓝色小圆点）。点击齿轮图标 -> “检查更新...” 或根据提示更新即可。Linux 用户通常可以通过包管理器更新。
    
- **卸载：**
    
    - **Windows:** 控制面板 -> 程序和功能 -> 找到 “Microsoft Visual Studio Code” -> 卸载。
        
    - **macOS:** 将 “应用程序” 文件夹中的 `Visual Studio Code.app` 拖到废纸篓。如果想彻底删除用户数据，还需删除 `~/Library/Application Support/Code` 和 `~/.vscode`。
        
    - **Linux (.deb):** 终端运行 `sudo apt-get remove code`。