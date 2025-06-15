---
tags:
  - git
  - 安装
  - windows
---
**文档目录**
- [**方法 1：官方安装程序（推荐）**](#**%E6%96%B9%E6%B3%95%201%EF%BC%9A%E5%AE%98%E6%96%B9%E5%AE%89%E8%A3%85%E7%A8%8B%E5%BA%8F%EF%BC%88%E6%8E%A8%E8%8D%90%EF%BC%89**)
	- [步骤1：下载安装程序](#%E6%AD%A5%E9%AA%A41%EF%BC%9A%E4%B8%8B%E8%BD%BD%E5%AE%89%E8%A3%85%E7%A8%8B%E5%BA%8F)
	- [步骤2：运行安装程序](#%E6%AD%A5%E9%AA%A42%EF%BC%9A%E8%BF%90%E8%A1%8C%E5%AE%89%E8%A3%85%E7%A8%8B%E5%BA%8F)
	- [步骤3：许可协议](#%E6%AD%A5%E9%AA%A43%EF%BC%9A%E8%AE%B8%E5%8F%AF%E5%8D%8F%E8%AE%AE)
	- [步骤4：安装位置](#%E6%AD%A5%E9%AA%A44%EF%BC%9A%E5%AE%89%E8%A3%85%E4%BD%8D%E7%BD%AE)
	- [步骤5：组件选择（关键步骤）](#%E6%AD%A5%E9%AA%A45%EF%BC%9A%E7%BB%84%E4%BB%B6%E9%80%89%E6%8B%A9%EF%BC%88%E5%85%B3%E9%94%AE%E6%AD%A5%E9%AA%A4%EF%BC%89)
	- [步骤6：开始菜单文件夹](#%E6%AD%A5%E9%AA%A46%EF%BC%9A%E5%BC%80%E5%A7%8B%E8%8F%9C%E5%8D%95%E6%96%87%E4%BB%B6%E5%A4%B9)
	- [步骤7：选择默认编辑器](#%E6%AD%A5%E9%AA%A47%EF%BC%9A%E9%80%89%E6%8B%A9%E9%BB%98%E8%AE%A4%E7%BC%96%E8%BE%91%E5%99%A8)
	- [步骤8：调整初始分支名称](#%E6%AD%A5%E9%AA%A48%EF%BC%9A%E8%B0%83%E6%95%B4%E5%88%9D%E5%A7%8B%E5%88%86%E6%94%AF%E5%90%8D%E7%A7%B0)
	- [步骤9：PATH环境配置（最重要步骤）](#%E6%AD%A5%E9%AA%A49%EF%BC%9APATH%E7%8E%AF%E5%A2%83%E9%85%8D%E7%BD%AE%EF%BC%88%E6%9C%80%E9%87%8D%E8%A6%81%E6%AD%A5%E9%AA%A4%EF%BC%89)
	- [步骤10：SSH客户端选择](#%E6%AD%A5%E9%AA%A410%EF%BC%9ASSH%E5%AE%A2%E6%88%B7%E7%AB%AF%E9%80%89%E6%8B%A9)
	- [步骤11：HTTPS传输后端](#%E6%AD%A5%E9%AA%A411%EF%BC%9AHTTPS%E4%BC%A0%E8%BE%93%E5%90%8E%E7%AB%AF)
	- [步骤12：换行符处理（关键配置）](#%E6%AD%A5%E9%AA%A412%EF%BC%9A%E6%8D%A2%E8%A1%8C%E7%AC%A6%E5%A4%84%E7%90%86%EF%BC%88%E5%85%B3%E9%94%AE%E9%85%8D%E7%BD%AE%EF%BC%89)
	- [步骤13：终端模拟器](#%E6%AD%A5%E9%AA%A413%EF%BC%9A%E7%BB%88%E7%AB%AF%E6%A8%A1%E6%8B%9F%E5%99%A8)
	- [步骤14：额外选项](#%E6%AD%A5%E9%AA%A414%EF%BC%9A%E9%A2%9D%E5%A4%96%E9%80%89%E9%A1%B9)
	- [步骤15：实验性功能](#%E6%AD%A5%E9%AA%A415%EF%BC%9A%E5%AE%9E%E9%AA%8C%E6%80%A7%E5%8A%9F%E8%83%BD)
	- [步骤16：完成安装](#%E6%AD%A5%E9%AA%A416%EF%BC%9A%E5%AE%8C%E6%88%90%E5%AE%89%E8%A3%85)
- [方法2：使用包管理器安装（高级用户）](#%E6%96%B9%E6%B3%952%EF%BC%9A%E4%BD%BF%E7%94%A8%E5%8C%85%E7%AE%A1%E7%90%86%E5%99%A8%E5%AE%89%E8%A3%85%EF%BC%88%E9%AB%98%E7%BA%A7%E7%94%A8%E6%88%B7%EF%BC%89)
	- [使用 Winget（Windows 11 内置）：](#%E4%BD%BF%E7%94%A8%20Winget%EF%BC%88Windows%2011%20%E5%86%85%E7%BD%AE%EF%BC%89%EF%BC%9A)
	- [使用 Chocolatey：](#%E4%BD%BF%E7%94%A8%20Chocolatey%EF%BC%9A)
- [安装后验证](#%E5%AE%89%E8%A3%85%E5%90%8E%E9%AA%8C%E8%AF%81)
- [首次使用设置](#%E9%A6%96%E6%AC%A1%E4%BD%BF%E7%94%A8%E8%AE%BE%E7%BD%AE)
	- [1. 解决中文乱码（如遇问题）：](#1.%20%E8%A7%A3%E5%86%B3%E4%B8%AD%E6%96%87%E4%B9%B1%E7%A0%81%EF%BC%88%E5%A6%82%E9%81%87%E9%97%AE%E9%A2%98%EF%BC%89%EF%BC%9A)
	- [2. 生成SSH密钥（连接GitHub/GitLab）：](#2.%20%E7%94%9F%E6%88%90SSH%E5%AF%86%E9%92%A5%EF%BC%88%E8%BF%9E%E6%8E%A5GitHub/GitLab%EF%BC%89%EF%BC%9A)
	- [3. 设置[[必备——VS Code代码编写工具]]为默认编辑器:(#3.%20%E8%AE%BE%E7%BD%AE%5B%5BVS%20Code%E5%B7%A5%E5%85%B7%5D%5D%E4%B8%BA%E9%BB%98%E8%AE%A4%E7%BC%96%E8%BE%91%E5%99%A8%EF%BC%9A)
- [常见问题解决](#%E5%B8%B8%E8%A7%81%E9%97%AE%E9%A2%98%E8%A7%A3%E5%86%B3)


### **方法 1：官方安装程序（推荐）**
#### 步骤1：下载安装程序
1. 打开浏览器访问 [Git 官方网站](https://git-scm.com/download/win)
2. 点击 "Download for Windows" 按钮（自动下载64位版本）
    - 若需32位版本，点击 "32-bit Git for Windows Setup"
#### 步骤2：运行安装程序
1. 双击下载的 `Git-2.xx.x-64-bit.exe` 文件 
2. 如出现安全警告，点击 "是" 继续
#### 步骤3：许可协议
1. 阅读许可协议
2. 勾选 "I accept the agreement"
3. 点击 "Next"
#### 步骤4：安装位置
1. 默认安装路径：`C:\Program Files\Git\`
2. 如需修改，点击 "Browse..." 选择新路径
3. 点击 "Next"
#### 步骤5：组件选择（关键步骤）
1. **必选组件**：
    - ✓ Git Bash Here（在右键菜单添加）
    - ✓ Git GUI Here（图形界面）
    - ✓ Git LFS（大文件支持）
    - ✓ Associate .git*（关联配置文件）
    - ✓ Associate .sh（关联Shell脚本）
2. **推荐选项**：
    - ✓ Add a Git Bash Profile to Windows Terminal（集成到终端）
    - ✓ Check daily for Git for Windows updates
3. 点击 "Next"
  #### 步骤6：开始菜单文件夹
4. 保持默认 "Git"
5. 点击 "Next"
#### 步骤7：选择默认编辑器
1. 推荐选择：
    - "Use Visual Studio Code as Git's default editor"（需已安装VSCode）
    - 或选择 "Notepad++"、"Vim" 等
    - 初学者可选 "Nano (simple)"
2. 点击 "Next"
#### 步骤8：调整初始分支名称
1. 推荐选择 "Let Git decide"（使用默认分支名 `master`）
2. 或选择 "Override" 输入 `main`（现代仓库常用）
3. 点击 "Next"
#### 步骤9：PATH环境配置（最重要步骤）
1. **必须选择**：
    - **Git from the command line and also from 3rd-party software**
    - （将Git添加到系统PATH，可在CMD/PowerShell中使用）
2. 不推荐：
    - "Use Git from Git Bash only"（仅限Git Bash使用）
    - "Use Git and optional Unix tools"（可能覆盖系统工具）
3. 点击 "Next"
#### 步骤10：SSH客户端选择
1. 保持默认 "Use bundled OpenSSH"
2. 点击 "Next"
#### 步骤11：HTTPS传输后端
1. 保持默认 "Use the OpenSSL library"
2. 点击 "Next"
#### 步骤12：换行符处理（关键配置）
1. **推荐选择**：
    - **Checkout Windows-style, commit Unix-style line endings**
    - （检出时转CRLF，提交时转LF）
2. 其他选项：
    - "Checkout as-is, commit as-is"（仅限纯Windows环境）
    - "Checkout as-is, commit Unix-style"（跨平台协作推荐）
3. 点击 "Next"
#### 步骤13：终端模拟器
1. 选择 "Use MinTTY"（Git Bash默认终端）
2. 不选 "Use Windows' default console window"（功能受限）
3. 点击 "Next"
#### 步骤14：额外选项
1. 勾选两项：
    - ✓ Enable file system caching（提升性能）
    - ✓ Enable Git Credential Manager（保存登录凭据）
2. 不选 "Enable symbolic links"（除非需要）
3. 点击 "Next"
#### 步骤15：实验性功能
1. 不勾选任何选项（除非明确需要）
2. 点击 "Install" 开始安装
#### 步骤16：完成安装
1. 等待进度条完成（约1-2分钟）
2. 取消勾选 "View Release Notes"
3. 点击 "Finish"

### 方法2：使用包管理器安装（高级用户）

#### 使用 Winget（Windows 11 内置）：
```powershell
# 打开 PowerShell (管理员)
winget install --id Git.Git -e --source winget
```

#### 使用 Chocolatey：
```powershell
# 打开 PowerShell (管理员)
Set-ExecutionPolicy Bypass -Scope Process -Force
[System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072
iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
choco install git -y
```
----

### 安装后验证

1. 打开 **命令提示符** 或 **PowerShell**：
```bash
git --version
# 应显示类似：git version 2.45.1.windows.1
```
  
2. 打开 **Git Bash**（开始菜单搜索）：
```bash
# 配置用户信息（必须）
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"

# 查看配置
git config --list
```
 
---

### 首次使用设置

#### 1. 解决中文乱码（如遇问题）：
```bash
git config --global core.quotepath false
echo "export LANG=zh_CN.UTF-8" >> ~/.bashrc
```
#### 2. 生成SSH密钥（连接GitHub/GitLab）：
```bash
ssh-keygen -t ed25519 -C "your.email@example.com"
# 连续按回车使用默认设置
cat ~/.ssh/id_ed25519.pub  # 复制输出内容到远程仓库设置
```
#### 3. 设置[[必备——VS Code代码编写工具]]为默认编辑器：
```bash
git config --global core.editor "code --wait"
```

---

### 常见问题解决

| 问题            | 解决方案                                                                |
| ------------- | ------------------------------------------------------------------- |
| `git` 命令不可用   | 1. 重启终端  <br>2. 检查环境变量：`PATH` 应包含 `C:\Program Files\Git\cmd`        |
| Git Bash 中文乱码 | 执行：`git config --global core.quotepath false`                       |
| 克隆速度慢         | 设置代理：`git config --global http.proxy http://proxy.example.com:8080` |
| 凭证保存失败        | 更新Git Credential Manager：`git update-git-for-windows`               |

> **提示**：安装完成后，在文件夹右键菜单中会出现 "Git Bash Here" 和 "Git GUI Here" 选项，方便快速操作。