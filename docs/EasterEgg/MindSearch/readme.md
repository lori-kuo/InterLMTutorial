# 【实战营彩蛋】MindSearch 快速部署（InternStudio 版）

选择 InternStudio 算力平台 50% A100 的 cuda 12.2 的开发机，并使用ssh vscode 远程连接到开发机。

<img width="1434" alt="image" src="https://github.com/user-attachments/assets/8d5b20bd-ca1d-4a87-ad38-47efeb48968f">

MindSearch（欢迎 Star）：https://github.com/InternLM/MindSearch 


## 1. 使用免费的搜索接口

### 1.1 激活环境

小助手提前帮大家安装好了环境，只需要一步一步按照下面的步骤便可以启动 MindSearch。

```shell
conda activate /share/pre_envs/mindsearch
```

### 1.2. 启动后端

打开新终端运行以下命令启动推理后端，使用入门岛中学到的方式使用 vscode 或者 ssh 将端口映射到本地 8002 端口。

```
conda activate /share/pre_envs/mindsearch
cd /share/demo/MindSearchDuck

python -m mindsearch.app --lang cn --model_format internstudio_server
```

### 1.3. 启动前端

打开新终端运行以下命令启动前端，使用入门岛中学到的方式使用 vscode 或者 ssh 将端口映射到本地 7860 端口。


```shell
conda activate /share/pre_envs/mindsearch
cd /share/demo/MindSearchDuck

python run.py
```

本地浏览器打开 http://localhost:7860 地址，开始 MindSearch 之旅。


## 2. 使用 Bing 的接口

### 2.1 激活环境

小助手提前帮大家安装好了环境，只需要一步一步按照下面的步骤便可以启动 MindSearch。

```shell
conda activate /share/pre_envs/mindsearch
```

### 2.2. 启动后端

打开新终端运行以下命令启动推理后端，使用入门岛中学到的方式使用 vscode 或者 ssh 将端口映射到本地 8002 端口。

```
export BING_API_KEY='YOU BING API Key'
conda activate /share/pre_envs/mindsearch
cd /share/demo/MindSearchBing

python -m mindsearch.app --lang cn --model_format internstudio_server
```

### 2.3. 启动前端

打开新终端运行以下命令启动前端，使用入门岛中学到的方式使用 vscode 或者 ssh 将端口映射到本地 7860 端口。


```shell
conda activate /share/pre_envs/mindsearch
cd /share/demo/MindSearchBing

python run.py
```

