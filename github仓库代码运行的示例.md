#  举例
Github仓库 ：[ACE-Step音乐AI生成](https://github.com/ace-step/ACE-Step)
A Step Towards Music Generation Foundation Model
## 按[installation](https://github.com/ace-step/ACE-Step?tab=readme-ov-file#-installation)说明安装（windows）

1.  安装[[必备——git仓库管理工具]]（仓库管理）
2. 安装[[必备——python代码运行]] (代码运行)
3. 安装[conda](必备——conda环境配置.md) （虚拟环境管理，以Miniconda为例）

4. 将代码克隆到本地
```powershell
cd ### #进入你想安装代码的父目录，如cd c:\AI(安装目录路径中最好不带中文)
git clone https://github.com/ace-step/ACE-Step.git
cd ACE-Step
```

5. 创建虚拟环境
```powershell
conda create -n ace_step python=3.10 -y
```

6. 激活虚拟环境
```powershell
conda activate ace_step
```

7. 安装依赖项
（仅限 Windows）如果您使用的是 Windows 并计划使用 NVIDIA GPU，请先安装支持 CUDA 的 PyTorch：
```powershell
pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu126
```
安装 ACE-Step 及其核心依赖项:
```powershell
pip install -e .
```

8. 基本用法(GUI界面)
```powershell
acestep --port 7865
```
用浏览器打开：[[http://127.0.0.1:7865]]


