---
tags:
  - note
  - obsidian
  - 介绍
  - 安装
---
Obsidian 是一个非常受欢迎的 **本地知识管理工具**，适合写笔记、建立知识库、研究资料整理、写作、项目管理等，本文件夹下所有文档均用Obsidian编写。
下面我将分两部分详细介绍：

---

## 🧠 一、Obsidian 的主要功能详解

Obsidian 是一个基于 Markdown 的本地知识库管理软件，主打“**双向链接**”与“**知识图谱**”概念，被广泛应用于笔记、写作、研究和个人知识管理（PKM）。

### 🔹 1. Markdown 文件编辑

- 使用标准 `.md` 文件（可在任何编辑器中打开）
    
- 支持标题、粗体、斜体、列表、引用、表格、代码块等
    
- 支持实时预览和分栏查看（编辑+预览）
    

### 🔹 2. 双向链接和知识网络

- 使用 `[[文件名]]` 可在笔记间建立链接
    
- 自动建立反向链接（Backlinks），查看哪些笔记提到了当前笔记
    
- 可视化“知识图谱”（Graph View）：展示所有笔记间的连接关系
    

### 🔹 3. 标签和元数据支持

- 使用 `#标签` 给笔记分类
    
- 支持 YAML Frontmatter（如：日期、作者、状态等）
    

### 🔹 4. 强大的搜索与过滤

- 支持全文搜索、正则表达式
    
- 支持通过标签、链接、文件结构等过滤笔记
    

### 🔹 5. 插件系统（核心 + 社区）

- **核心插件**：日记、图谱视图、版本控制、工作区等
    
- **社区插件**：如任务管理（Tasks）、日历、时间轴、绘图、Anki 同步、Latex 支持等
    

### 🔹 6. 自定义主题和样式

- 使用 CSS 或现成的社区主题美化界面
    
- 支持暗色/亮色主题切换
    

### 🔹 7. 数据安全和可迁移性

- 完全本地保存，不强制使用云服务
    
- 可用 Git、Dropbox、iCloud 等方式自行同步数据
    

---

## 💻 二、Obsidian 安装指南（各系统）

### 🪟 Windows 安装

#### 方法 1：官网下载

1. 访问官网：  
    👉 [https://obsidian.md](https://obsidian.md)
    
2. 点击 `Download`，选择 `Windows (64-bit Installer)`
    
3. 下载 `.exe` 安装包并运行安装
    

#### 方法 2：使用 Windows 商店

- 打开 Microsoft Store，搜索 “Obsidian”，点击安装
    

---

### 🍎 macOS 安装

#### 方法 1：官网下载

1. 访问官网：  
    👉 [https://obsidian.md](https://obsidian.md)
    
2. 点击 `Download`，选择 `macOS (Universal)`
    
3. 下载 `.dmg` 文件，双击拖动到“应用程序”中即可
    

#### 方法 2：通过 Homebrew 安装（开发者/终端用户推荐）

bash

复制编辑

`brew install --cask obsidian`

---

### 🐧 Linux 安装

#### 方法 1：AppImage（通用方式）

1. 下载地址：  
    👉 [https://obsidian.md](https://obsidian.md) → 选择 `Linux AppImage`
    
2. 下载 `.AppImage` 文件
    
3. 给文件加执行权限：
    

bash

复制编辑

`chmod +x Obsidian-x.y.z.AppImage ./Obsidian-x.y.z.AppImage`

#### 方法 2：使用 Snap 安装

bash

复制编辑

`sudo snap install obsidian`

#### 方法 3：使用 Flatpak 安装

bash

复制编辑

`flatpak install flathub md.obsidian.Obsidian flatpak run md.obsidian.Obsidian`

---

### 📱 移动端（iOS / Android）

#### 📱 iOS（iPhone / iPad）

- 打开 App Store，搜索 “Obsidian”，点击下载安装
    
- 支持 iCloud 同步（可与 macOS 共享 Vault）
    

#### 🤖 Android

- 打开 Google Play 商店，搜索 “Obsidian”，点击下载安装
    
- 支持本地存储或通过第三方（如 Dropbox、Syncthing）同步
    

---

## 📁 关于 Vault（知识库）

Obsidian 的笔记存储在所谓的 **Vault（保险库）** 中，一个 Vault 就是一个文件夹：

- 你可以新建一个空文件夹作为 Vault
    
- 也可以把已有的 Markdown 文件夹导入为 Vault
    
- 一个 Vault 可以包含任意子文件夹、图片、PDF、附件等资源
    

---

## 🧩 推荐社区插件（可选）

|插件名称|功能说明|
|---|---|
|Obsidian Tasks|支持 GTD 和任务管理|
|Calendar|添加日历面板，与日记联动|
|Dataview|用查询语言动态展示笔记数据|
|Excalidraw|可手绘思维导图/图解内容|
|Advanced Tables|强化 Markdown 表格编辑体验|
|Zotero Integration|与文献管理工具 Zotero 联动|

---

## 📚 学习资源

- 官网教程：https://help.obsidian.md
    
- 中文教程站：https://publish.obsidian.md/chinese
    
- B站搜索 “Obsidian 教程” 有大量入门视频
    
- 推荐书籍：《卡片笔记写作法》、《第二大脑》等