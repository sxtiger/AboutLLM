---
tags:
  - python
  - 安装
  - windows
  - mac
  - linux
---
**文档目录**
- [✅ 一、Windows 安装 Python](#%E2%9C%85%20%E4%B8%80%E3%80%81Windows%20%E5%AE%89%E8%A3%85%20Python)
	- [步骤：](#%E6%AD%A5%E9%AA%A4%EF%BC%9A)
- [✅ 二、macOS 安装 Python](#%E2%9C%85%20%E4%BA%8C%E3%80%81macOS%20%E5%AE%89%E8%A3%85%20Python)
	- [方法 1：使用 Homebrew（推荐）](#%E6%96%B9%E6%B3%95%201%EF%BC%9A%E4%BD%BF%E7%94%A8%20Homebrew%EF%BC%88%E6%8E%A8%E8%8D%90%EF%BC%89)
	- [方法 2：通过官网下载安装包](#%E6%96%B9%E6%B3%95%202%EF%BC%9A%E9%80%9A%E8%BF%87%E5%AE%98%E7%BD%91%E4%B8%8B%E8%BD%BD%E5%AE%89%E8%A3%85%E5%8C%85)
- [✅ 三、Linux 安装 Python](#%E2%9C%85%20%E4%B8%89%E3%80%81Linux%20%E5%AE%89%E8%A3%85%20Python)
	- [Ubuntu / Debian 系列](#Ubuntu%20/%20Debian%20%E7%B3%BB%E5%88%97)
	- [RedHat / CentOS / Fedora 系列](#RedHat%20/%20CentOS%20/%20Fedora%20%E7%B3%BB%E5%88%97)
	- [验证安装：](#%E9%AA%8C%E8%AF%81%E5%AE%89%E8%A3%85%EF%BC%9A)
- [✅ 安装完成后建议：](#%E2%9C%85%20%E5%AE%89%E8%A3%85%E5%AE%8C%E6%88%90%E5%90%8E%E5%BB%BA%E8%AE%AE%EF%BC%9A)
	- [1. 检查 pip（通常已内置）：](#1.%20%E6%A3%80%E6%9F%A5%20pip%EF%BC%88%E9%80%9A%E5%B8%B8%E5%B7%B2%E5%86%85%E7%BD%AE%EF%BC%89%EF%BC%9A)
	- [2. 安装一个常用库测试是否成功：](#2.%20%E5%AE%89%E8%A3%85%E4%B8%80%E4%B8%AA%E5%B8%B8%E7%94%A8%E5%BA%93%E6%B5%8B%E8%AF%95%E6%98%AF%E5%90%A6%E6%88%90%E5%8A%9F%EF%BC%9A)
- [📌 附加建议](#%F0%9F%93%8C%20%E9%99%84%E5%8A%A0%E5%BB%BA%E8%AE%AE)


安装 Python 的方法因操作系统不同而异，以下是在 **Windows**、**macOS** 和 **Linux** 下的安装步骤。

---

## ✅ 一、Windows 安装 Python

### 步骤：

1. **访问官网**  
   [Python 官网](https://www.python.org/downloads/)

2. **下载安装程序**  
   点击推荐版本（如 Python 3.x），下载 `.exe` 安装文件。

3. **运行安装程序**  
   双击运行下载的 `.exe` 文件。

4. **勾选 "Add Python to PATH"** ✅  
   一定要勾选这个选项，否则命令行无法使用 Python。

5. **点击 "Install Now"**  
   等待安装完成即可。

6. **验证安装是否成功**  
   打开命令提示符（Win + R → 输入 `cmd` 回车），输入：

   ```bash
   python --version
   ```

   显示版本号即安装成功。

---

## ✅ 二、macOS 安装 Python

### 方法 1：使用 Homebrew（推荐）

1. **安装 Homebrew（如未安装）**

   ```bash
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   ```

2. **使用 Homebrew 安装 Python**

   ```bash
   brew install python
   ```

3. **验证安装**

   ```bash
   python3 --version
   ```

### 方法 2：通过官网下载安装包

- 访问 [Python 官网 macOS 版](https://www.python.org/downloads/mac-osx/)
- 下载 `.pkg` 安装包并安装
- 安装后验证：

   ```bash
   python3 --version
   ```

---

## ✅ 三、Linux 安装 Python

### Ubuntu / Debian 系列

```bash
sudo apt update
sudo apt install python3 python3-pip
```

### RedHat / CentOS / Fedora 系列

```bash
sudo dnf install python3
```

### 验证安装：

```bash
python3 --version
```

---

## ✅ 安装完成后建议：

### 1. 检查 pip（通常已内置）：

```bash
pip3 --version
```

### 2. 安装一个常用库测试是否成功：

```bash
pip3 install requests
```

---

## 📌 附加建议

如果你打算用于：

- **学习编程**：推荐安装[[必备——VS Code代码编写工具]]
- **科学计算/数据分析**：推荐安装[[必备——conda环境配置]]
- **网页开发**：可考虑 `Flask` 或 `Django` 框架

---

