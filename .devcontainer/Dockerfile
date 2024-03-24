FROM ubuntu:latest

# 更新Ubuntu软件包并安装常用软件
RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get install -y curl wget vim git

# 安装nvm依赖项
RUN apt-get install -y build-essential libssl-dev

# 安装Rust
RUN curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh -s -- -y

# 将Rust的二进制文件添加到PATH环境变量中
ENV PATH /root/.cargo/bin:$PATH

# 设置工作目录
WORKDIR /app
