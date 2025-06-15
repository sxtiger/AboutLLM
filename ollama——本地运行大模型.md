---
tags:
  - ollama
  - 安装
  - windows
  - linux
  - mac
---
**文档目录**
- [基本原理图](#%E5%9F%BA%E6%9C%AC%E5%8E%9F%E7%90%86%E5%9B%BE)
- [ollama介绍](#ollama%E4%BB%8B%E7%BB%8D)
	- [🔧 一、核心功能](#%F0%9F%94%A7%20%E4%B8%80%E3%80%81%E6%A0%B8%E5%BF%83%E5%8A%9F%E8%83%BD)
	- [⚙️ 二、适用场景](#%E2%9A%99%EF%B8%8F%20%E4%BA%8C%E3%80%81%E9%80%82%E7%94%A8%E5%9C%BA%E6%99%AF)
	- [⚠️ 三、局限性](#%E2%9A%A0%EF%B8%8F%20%E4%B8%89%E3%80%81%E5%B1%80%E9%99%90%E6%80%A7)
	- [💎 总结](#%F0%9F%92%8E%20%E6%80%BB%E7%BB%93)
- [本地电脑上部署 Ollama](#%E6%9C%AC%E5%9C%B0%E7%94%B5%E8%84%91%E4%B8%8A%E9%83%A8%E7%BD%B2%20Ollama)
	- [**1. 系统要求**](#**1.%20%E7%B3%BB%E7%BB%9F%E8%A6%81%E6%B1%82**)
	- [**2. 安装步骤**](#**2.%20%E5%AE%89%E8%A3%85%E6%AD%A5%E9%AA%A4**)
		- [**macOS**](#**macOS**)
		- [**Linux**](#**Linux**)
		- [**Windows**](#**Windows**)
	- [**3. 验证安装**](#**3.%20%E9%AA%8C%E8%AF%81%E5%AE%89%E8%A3%85**)
	- [**4. 运行模型**](#**4.%20%E8%BF%90%E8%A1%8C%E6%A8%A1%E5%9E%8B**)
		- [**基础用法**](#**%E5%9F%BA%E7%A1%80%E7%94%A8%E6%B3%95**)
		- [**交互示例**](#**%E4%BA%A4%E4%BA%92%E7%A4%BA%E4%BE%8B**)
	- [**5. 常用命令**](#**5.%20%E5%B8%B8%E7%94%A8%E5%91%BD%E4%BB%A4**)
	- [**6. 通过 API 调用**](#**6.%20%E9%80%9A%E8%BF%87%20API%20%E8%B0%83%E7%94%A8**)
	- [**7. 自定义模型（可选）**](#**7.%20%E8%87%AA%E5%AE%9A%E4%B9%89%E6%A8%A1%E5%9E%8B%EF%BC%88%E5%8F%AF%E9%80%89%EF%BC%89**)
	- [**8. 常见问题**](#**8.%20%E5%B8%B8%E8%A7%81%E9%97%AE%E9%A2%98**)


## 基本原理图
![[大模型本地化部署.png]]

## ollama介绍
Ollama 是一个开源的大型语言模型（LLM）本地运行与管理框架，旨在简化大模型在个人设备上的部署和使用流程。它通过整合模型权重、配置和依赖环境，让用户无需复杂配置即可一键运行各类开源大模型（如 Llama、Mistral、DeepSeek 等）134。以下是其核心特点与定位的详细说明：

---

### 🔧 一、核心功能

1. **本地化运行与隐私保护**  
    Ollama 支持完全离线运行，所有模型和数据存储在本地，避免依赖云端服务，特别适合对数据隐私要求高的场景（如企业敏感数据、个人隐私任务）356。
    
2. **简化的模型管理**
    
    - **预构建模型库**：提供主流开源模型（如 Llama 3、Mistral、Gemma、DeepSeek-R1 等），支持 `ollama pull <模型名>` 快速下载27。
        
    - **自定义模型**：支持通过 `Modelfile` 修改提示词、采样参数，或导入微调后的 GGUF 格式模型48。
        
3. **跨平台与硬件适配**
    
    - 支持 Windows（需 WSL2）、macOS（原生优化 Apple Silicon）、Linux 系统17。
        
    - 自动检测硬件资源，支持 CPU 推理及 GPU 加速（NVIDIA CUDA / Apple Metal）48。
        
4. **丰富的交互方式**
    
    - **命令行交互**：`ollama run <模型名>` 直接对话25。
        
    - **API 服务**：内置 RESTful API（默认端口 `11434`），兼容 OpenAI 格式，方便集成 LangChain 等开发框架45。
        
    - **图形界面扩展**：可搭配 Open WebUI、Ollamac 等第三方工具实现类 ChatGPT 的交互体验28。
        

---

### ⚙️ 二、适用场景

- **开发者原型测试**：本地快速验证模型效果，无需申请 API Key 或支付云服务费用58。
    
- **隐私敏感任务**：医疗、金融等领域的数据处理，避免数据外传36。
    
- **教育/科研**：学生或研究者低成本运行模型实验，支持自定义微调34。
    
- **内容生成与编程辅助**：自动生成文本、代码、翻译等任务37。
    

---

### ⚠️ 三、局限性

1. **性能与模型支持**
    
    - 仅支持 GGUF 格式的量化模型（如 Llama.cpp 导出），不支持多模态或非 Transformer 架构模型46。
        
    - 吞吐量低于专业推理框架（如 vLLM），高并发场景表现较弱4。
        
2. **资源要求**
    
    - 7B 参数模型需至少 8GB RAM，13B 模型需 16GB，更大模型（如 70B）需 32GB 以上内存或高性能 GPU78。
        
    - Windows 依赖 WSL2，且 AMD GPU 支持不完善46。
        
3. **安全风险**
    
    - 默认开放本地端口 `11434`，若错误配置为公网访问可能引发未授权访问或模型窃取（需注意配置防火墙）6。
        
    - 历史漏洞（如 CVE-2024-37032）需及时更新版本6。
        

---

### 💎 总结

Ollama 是**平衡易用性与本地化需求的轻量级工具**，极大降低了个人开发者运行大模型的门槛。尽管其性能与功能无法替代企业级框架，但凭借开箱即用、隐私安全、生态丰富（如支持 DeepSeek、Llama 等 100+ 模型）等优势27，已成为本地探索大模型的首选方案之一。

## 本地电脑上部署 Ollama
### **1. 系统要求**

- **操作系统**：支持 macOS、Linux 或 Windows（Windows 需 Windows 10+ 且开启 WSL2）。
    
- **内存**：至少 8GB RAM（推荐 16GB+，模型越大需求越高）。
    
- **存储空间**：预留 10GB+ 空间（模型文件通常较大）。
    

---

### **2. 安装步骤**

#### **macOS**

1. **直接下载安装**：
    
    - 访问 [Ollama 官网](https://ollama.ai/)
        
    - 点击 "Download for macOS"，运行安装包。
        
    - 安装后会自动出现在菜单栏，后台服务默认启动。
        

#### **Linux**
```bash
# 一键安装脚本（支持 Ubuntu/Debian/CentOS/Arch 等）
curl -fsSL https://ollama.com/install.sh | sh
```

#### **Windows**

1. **启用 WSL2**（需管理员权限）：
```powershell
		wsl --install  # 自动安装 Ubuntu 发行版
		wsl --update   # 确保 WSL 版本为 2
```
2. **在 WSL 中安装 Ollama**：
    
    - 打开 WSL 终端（如 Ubuntu）。
        
    - 运行 Linux 安装命令：
```bash
curl -fsSL https://ollama.com/install.sh | sh
```
   
---

### **3. 验证安装**

- 打开终端（Windows 需 WSL 终端），运行：
```bash
ollama --version
```
  
---

### **4. 运行模型**

#### **基础用法**
```bash
# 下载并运行模型（首次运行自动下载）
ollama run llama3     # Meta 的 Llama 3
ollama run mistral    # Mistral 7B
ollama run phi3       # Microsoft Phi-3
```
#### **交互示例**
```bash
>>> 你好，你能做什么？
（模型会生成回答）
```

---

### **5. 常用命令**

| 命令                  | 说明                    |
| ------------------- | --------------------- |
| `ollama run <模型名>`  | 运行模型（自动下载）            |
| `ollama list`       | 查看已安装模型               |
| `ollama pull <模型名>` | 下载模型不运行               |
| `ollama rm <模型名>`   | 删除模型                  |
| `ollama serve`      | 启动 API 服务（默认端口 11434） |

---

### **6. 通过 API 调用**

启动服务后，可通过 HTTP 请求调用：
```bash
curl http://localhost:11434/api/generate -d '{
  "model": "llama3",
  "prompt": "为什么天空是蓝色的？"
}'
```

---

### **7. 自定义模型（可选）**

1. 创建 `Modelfile` 文件：
```dockerfile
FROM llama3
# 自定义参数（示例）
PARAMETER temperature 0.7
SYSTEM """
你是一个乐于助人的助手，用中文回答所有问题。
"""
```
   
2. 构建自定义模型：
```bash
ollama create my-model -f ./Modelfile
```
  
3. 运行自定义模型：
```bash
ollama run my-model
```
 
---

### **8. 常见问题**

- **模型下载慢**：更换网络或手动下载（模型存储在 `~/.ollama/models`）。
    
- **内存不足**：尝试更小的模型（如 `phi3` 或 `tinyllama`）。
    
- **Windows 报错**：确保 WSL2 已启用，且虚拟机平台功能已开启。


