---
tags:
  - docker
  - 安装
  - 使用
  - windows
  - mac
  - linux
---
**文档目录**
- [[#什么是docker?|什么是docker?]]
	- [[#什么是docker?#核心概念解析：|核心概念解析：]]
	- [[#什么是docker?#Docker 的核心价值：|Docker 的核心价值：]]
	- [[#什么是docker?#与传统虚拟机（VM）对比：|与传统虚拟机（VM）对比：]]
	- [[#什么是docker?#典型应用场景：|典型应用场景：]]
	- [[#什么是docker?#简单示例：|简单示例：]]
	- [[#什么是docker?#生态系统扩展：|生态系统扩展：]]
- [[#Windows 安装 Docker|Windows 安装 Docker]]
	- [[#Windows 安装 Docker#系统要求：|系统要求：]]
	- [[#Windows 安装 Docker#步骤：|步骤：]]
- [[#macOS 安装 Docker|macOS 安装 Docker]]
	- [[#macOS 安装 Docker#系统要求：|系统要求：]]
	- [[#macOS 安装 Docker#步骤：|步骤：]]
- [[#Linux安装 Docker 的详细步骤（以 Ubuntu 为例）|Linux安装 Docker 的详细步骤（以 Ubuntu 为例）]]
	- [[#Linux安装 Docker 的详细步骤（以 Ubuntu 为例）#步骤 1：卸载旧版本（如有）|步骤 1：卸载旧版本（如有）]]
	- [[#Linux安装 Docker 的详细步骤（以 Ubuntu 为例）#步骤 2：安装依赖工具|步骤 2：安装依赖工具]]
	- [[#Linux安装 Docker 的详细步骤（以 Ubuntu 为例）#步骤 3：添加 Docker 官方 GPG 密钥|步骤 3：添加 Docker 官方 GPG 密钥]]
	- [[#Linux安装 Docker 的详细步骤（以 Ubuntu 为例）#步骤 4：设置稳定版仓库|步骤 4：设置稳定版仓库]]
	- [[#Linux安装 Docker 的详细步骤（以 Ubuntu 为例）#步骤 5：安装 Docker 引擎|步骤 5：安装 Docker 引擎]]
	- [[#Linux安装 Docker 的详细步骤（以 Ubuntu 为例）#步骤 6：验证安装|步骤 6：验证安装]]
	- [[#Linux安装 Docker 的详细步骤（以 Ubuntu 为例）#步骤 7：配置用户组（免 sudo）|步骤 7：配置用户组（免 sudo）]]
	- [[#Linux安装 Docker 的详细步骤（以 Ubuntu 为例）#**CentOS**安装：替换步骤 4 的仓库地址为 `https://download.docker.com/linux/centos`|**CentOS**安装：替换步骤 4 的仓库地址为 `https://download.docker.com/linux/centos`]]
- [[#部署容器的详细步骤（以 Nginx 为例）|部署容器的详细步骤（以 Nginx 为例）]]
	- [[#部署容器的详细步骤（以 Nginx 为例）#步骤 1：拉取镜像|步骤 1：拉取镜像]]
	- [[#部署容器的详细步骤（以 Nginx 为例）#步骤 2：运行容器|步骤 2：运行容器]]
	- [[#部署容器的详细步骤（以 Nginx 为例）#步骤 3：验证容器状态|步骤 3：验证容器状态]]
	- [[#部署容器的详细步骤（以 Nginx 为例）#步骤 4：测试访问|步骤 4：测试访问]]
	- [[#部署容器的详细步骤（以 Nginx 为例）#步骤 5：管理容器|步骤 5：管理容器]]
- [[#常用管理命令|常用管理命令]]

### 什么是docker?

Docker 是一种**开源的容器化平台**，用于快速构建、打包、部署和运行应用程序及其依赖环境。它通过“容器”（Container）技术，将应用与所需的环境（如库、配置文件等）打包成一个轻量级、可移植的独立单元，实现 **“一次构建，处处运行”**。

#### 核心概念解析：

1. **容器（Container）**
    
    - **轻量级虚拟化**：不同于传统虚拟机（VM）模拟完整操作系统，容器共享主机系统的内核，只虚拟化应用运行环境。
        
    - **隔离性**：每个容器拥有独立的文件系统、网络、进程空间，互不干扰。
        
    - **快速启停**：秒级启动，资源占用极低（远低于VM）。
        
2. **镜像（Image）**
    
    - **只读模板**：包含应用代码、运行时环境、系统工具等。镜像是容器的基础，通过分层存储（Layer）实现高效复用。
        
    - **镜像仓库**：Docker Hub 或私有仓库（如 Harbor）用于存储和共享镜像。
        
3. **Dockerfile**
    
    - **构建镜像的脚本**：用文本指令定义镜像内容（例如：`FROM ubuntu`, `COPY app.py`, `RUN pip install`）。
        
#### Docker 的核心价值：

- **环境一致性**  
    开发、测试、生产环境完全一致，避免“在我机器上能跑”的问题。
    
- **快速部署与扩展**  
    镜像秒级启动，结合编排工具（如 Kubernetes）实现自动化扩缩容。
    
- **资源高效利用**  
    容器无额外操作系统开销，单机可运行数十甚至上百容器。
    
- **微服务架构支撑**  
    每个微服务独立容器化，解耦部署和管理。
    

#### 与传统虚拟机（VM）对比：

|**特性**|**Docker 容器**|**虚拟机（VM）**|
|---|---|---|
|**虚拟化层级**|操作系统级（共享主机内核）|硬件级（Hypervisor 虚拟硬件）|
|**启动速度**|秒级|分钟级|
|**资源占用**|极低（MB 级内存）|高（GB 级内存 + 完整 OS）|
|**隔离性**|进程级隔离|完全隔离|
|**镜像大小**|通常为 MB ~ GB|通常为 GB ~ TB|

---

#### 典型应用场景：

1. **标准化开发环境**  
    `docker-compose up` 一键拉起数据库、中间件等依赖服务。
    
2. **持续集成/部署（CI/CD）**  
    构建镜像 → 测试镜像 → 推送仓库 → 生产环境部署。
    
3. **微服务架构**  
    每个服务独立容器化，通过 Docker 网络通信。
    
4. **云原生应用**  
    作为 Kubernetes 的底层容器运行时。
    

---

#### 简单示例：

1. **拉取镜像**：
```bash
docker pull nginx:latest
```
 
2. **运行容器**：
```bash
docker run -d -p 8080:80 --name my-nginx nginx
```
  
    - `-d`：后台运行
        
    - `-p 8080:80`：将主机 8080 端口映射到容器的 80 端口
        
    - 访问 `http://localhost:8080` 即可看到 Nginx 页面。
        

#### 生态系统扩展：

- **Docker Compose**：通过 YAML 文件定义多容器应用。
    
- **Docker Swarm / Kubernetes**：容器集群编排与管理。
    
- **容器安全工具**：Clair（镜像漏洞扫描）、Notary（镜像签名）。
    

> 💡 **总结**：Docker 通过容器化技术解决了应用交付的环境差异问题，成为现代 DevOps 和云原生架构的基石。它降低了运维复杂度，提升了资源利用率，是构建弹性、可扩展系统的关键工具。

###  Windows 安装 Docker

#### 系统要求：

- Windows 10/11 64位（专业版/企业版/教育版）
    
- 启用 Hyper-V 和 WSL 2（[微软官方文档](https://learn.microsoft.com/zh-cn/windows/wsl/install)）

#### 步骤：

1. **启用 WSL 2**：
	```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```
    重启电脑，然后安装 [WSL 2 内核更新包](https://aka.ms/wsl2kernel)。

2. **下载 Docker Desktop**：  
    访问 [Docker Desktop for Windows](https://www.docker.com/products/docker-desktop)，下载安装包。
    
3. **安装**：  
    双击安装包 → 勾选 _Enable WSL 2 Features_ → 按向导完成安装。
    
4. **启动验证**：  
    桌面双击 Docker 图标启动 → 打开 PowerShell：
```powershell
docker --version        # 显示版本号
docker run hello-world  # 测试运行
```

### macOS 安装 Docker

#### 系统要求：

- macOS 10.15 (Catalina) 或更高版本（Intel/Apple Silicon 均支持）

#### 步骤：

1. **下载 Docker Desktop**：  
    访问 [Docker Desktop for Mac](https://www.docker.com/products/docker-desktop)，选择对应芯片版本（Intel 或 Apple Silicon）。
    
2. **安装**：  
    双击下载的 `.dmg` 文件 → 拖拽 Docker 图标到 _Applications_ 文件夹。
    
3. **启动验证**：  
    在 _Applications_ 中双击 Docker 图标 → 打开终端：
```bash
docker --version
docker run hello-world
```
  
### Linux安装 Docker 的详细步骤（以 Ubuntu 为例）

#### 步骤 1：卸载旧版本（如有）
```bash
sudo apt-get remove docker docker-engine docker.io containerd runc
```
#### 步骤 2：安装依赖工具
```bash
sudo apt-get update
sudo apt-get install apt-transport-https ca-certificates curl gnupg lsb-release
```

#### 步骤 3：添加 Docker 官方 GPG 密钥
```bash
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
```

#### 步骤 4：设置稳定版仓库
```bash
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

#### 步骤 5：安装 Docker 引擎
```bash
sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io
```

#### 步骤 6：验证安装
```bash
sudo docker --version  # 显示版本号即成功
sudo docker run hello-world  # 运行测试容器
```
#### 步骤 7：配置用户组（免 sudo）
```bash
sudo groupadd docker  # 如果组已存在可忽略
sudo usermod -aG docker $USER
newgrp docker  # 刷新组权限
```
	注销后重新登录生效

#### **CentOS**安装：替换步骤 4 的仓库地址为 `https://download.docker.com/linux/centos`
---

### 部署容器的详细步骤（以 Nginx 为例）

#### 步骤 1：拉取镜像
```bash
docker pull nginx:latest  # 从 Docker Hub 下载官方镜像
```

#### 步骤 2：运行容器
```bash
docker run -d --name my-nginx -p 8080:80 nginx
```

- `-d`：后台运行
    
- `--name`：容器名称
    
- `-p 8080:80`：将主机 8080 端口映射到容器的 80 端口

#### 步骤 3：验证容器状态
```bash
docker ps  # 查看运行中的容器
```
应输出包含 `my-nginx` 的状态为 `Up`

#### 步骤 4：测试访问
- 浏览器打开：`http://localhost:8080`  
- 或终端验证：
```bash
curl localhost:8080  # 应返回 Nginx 欢迎页面 HTML
```

#### 步骤 5：管理容器
```bash
docker stop my-nginx    # 停止容器
docker start my-nginx   # 启动已停止的容器
docker rm my-nginx      # 删除容器（需先停止）
docker logs my-nginx    # 查看日志
```

---

### 常用管理命令

|命令|说明|
|---|---|
|`docker images`|查看本地镜像|
|`docker rmi <镜像ID>`|删除镜像|
|`docker exec -it my-nginx bash`|进入容器终端|
|`docker cp file.txt my-nginx:/path`|主机→容器文件复制|
|`docker build -t my-image .`|构建自定义镜像|

> **注意**：生产环境部署建议：
> 
> 1. 使用 `docker-compose.yml` 管理多容器
>     
> 2. 通过 `-v` 参数挂载数据卷持久化数据
>     
> 3. 设置资源限制：`--memory=1g --cpus=1`
>     

