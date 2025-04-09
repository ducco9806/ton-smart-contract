# .devcontainer/Dockerfile

FROM ubuntu:22.04

# Cài gói cần thiết
RUN apt update && apt install -y \
    git curl cmake build-essential clang pkg-config \
    libssl-dev libreadline-dev zlib1g-dev \
    python3 python3-pip wget unzip

# Cài func
RUN git clone https://github.com/ton-blockchain/func.git && \
    cd func && cmake . && make && make install && cd .. && rm -rf func

# Cài fift
RUN git clone https://github.com/ton-blockchain/fift.git && \
    cd fift && cmake . && make && make install && cd .. && rm -rf fift

# Cài toncli (Python)
RUN pip3 install toncli

# Khởi tạo thư mục làm việc
WORKDIR /workspace
