# 使用 nvidia/cuda:11.8.0-devel-ubuntu20.04 作为基础镜像
FROM nvidia/cuda:11.6.1-devel-ubuntu20.04


# 设置工作目录
WORKDIR /home/sitian

# 更新系统包并安装 Python 3 和必需的工具
RUN apt-get update && apt-get install -y \
    python3 \
    python3-pip \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

# 复制 requirements 文件到镜像中
COPY langsplat_requirements.txt /app/requirements.txt

# 确保 pip 是最新版本
RUN pip3 install --no-cache-dir --upgrade pip

# 安装 Python 依赖项
RUN pip3 install --no-cache-dir -r /app/requirements.txt

